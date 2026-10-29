## Overview

Linux firewall tools are easiest to understand in layers:

1. Netfilter is the kernel networking framework that provides packet-processing hooks and related features.
2. nftables and iptables are ways to define packet-filtering rules that the kernel applies.
3. UFW and firewalld are higher-level managers that make firewall configuration easier.

These names do not all represent four separate firewall engines. UFW and firewalld can configure the underlying packet-filtering system for you. Netfilter provides the kernel infrastructure used by these tools. netfilter.org1

## At a glance

| Name          | Category                                                | Main interface                                    | Notes                                                                                                                                            |
| ------------- | ------------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| Netfilter     | Kernel networking framework                             | None directly; configured through userspace tools | Provides hooks and features used for filtering, connection tracking, NAT, and logging.                                                           |
| [[nftables]]  | Kernel packet-filtering framework and userspace toolset | `nft`                                             | Modern Netfilter rule system; supports IPv4 and IPv6, including combined rulesets.                                                               |
| [[iptables]]  | Older Netfilter rule system and command-line tools      | `iptables`, `ip6tables`, and related commands     | Still used by existing scripts and software. Depending on the system, it may use either the legacy backend or an nftables compatibility backend. |
| [[UFW]]       | Firewall manager / frontend                             | `ufw`                                             | Simplifies common firewall tasks. It can configure iptables or nftables, depending on the distribution and setup.                                |
| [[firewalld]] | Firewall manager / service                              | `firewall-cmd`, optionally `firewall-config`      | Manages rules dynamically using concepts such as zones and services. Its current default backend is nftables.                                    |

## Kernel framework: Netfilter

Netfilter is the part of the Linux kernel that provides points—called _hooks_—where network packets can be examined and acted on. Rules can accept, drop, or otherwise process traffic as packets pass through the networking stack. Netfilter also provides related facilities such as connection tracking and NAT. netfilter.org1

Netfilter is not normally configured by typing a `netfilter` command. Instead, tools such as `nft` and `iptables` send rules to the kernel.

## Rule systems

### nftables

nftables is the modern rule system in the Netfilter subsystem. Its command-line tool is named `nft`. It replaces the older collection of tools—`iptables`, `ip6tables`, `arptables`, and `ebtables`—with a more unified system and syntax. netfilter.org1

Useful concepts:

- Table: A container for firewall objects and rules.
- Chain: A group of rules evaluated at a point in packet processing.
- Rule: A condition that matches traffic and an action to take, such as accepting or dropping it.
- Set: A reusable collection of values, such as IP addresses or ports.
- Family: The kind of traffic a table handles. The `inet` family can cover IPv4 and IPv6 in one ruleset.

Unlike the traditional iptables layout, nftables does not automatically create standard tables and chains: they exist when a configuration creates them. [Debian](https://wiki.debian.org/nftables)

Common inspection commands:

bash

```
sudo nft list rulesetsudo nft list tables
```

### iptables

iptables is the older rule system and command-line interface for configuring Netfilter. Related commands include `ip6tables` for IPv6 and, historically, `arptables` and `ebtables` for other traffic types. ubuntu.com1

A key detail: the command named `iptables` does not tell you which backend is active. On some systems, it uses the legacy iptables implementation; on others, it uses an iptables-nft compatibility layer that translates iptables-style commands into nftables rules. The active backend depends on the distribution and system configuration. ubuntu.com1

Check the version/backend indicator and inspect the active nftables rules with:

bash

```
iptables --versionsudo nft list ruleset
```

If the version output includes `(nf_tables)`, the iptables command is using the nftables backend. If it includes `(legacy)`, it is using the legacy backend.

## Firewall managers

### UFW

UFW stands for Uncomplicated Firewall. It is a frontend intended to make common firewall tasks straightforward—for example, allowing SSH or blocking incoming connections by default. It is popular on Ubuntu systems.

UFW is a manager, not a separate kernel packet-filtering engine. Depending on the distribution and configuration, it may program iptables or nftables rules. Ubuntu documents UFW as a frontend for both. [ubuntu.com](https://documentation.ubuntu.com/security/security-features/network/firewall/)

Example commands:

bash

```
sudo ufw status verbosesudo ufw allow 22/tcpsudo ufw enable
```

Before enabling a firewall on a remote machine, make sure you have allowed the port you use to connect—often SSH on TCP port 22—or you could lock yourself out.

### firewalld

firewalld is a firewall management service. It provides concepts such as zones, which represent different trust levels or network contexts, and services, which group the ports and protocols used by common applications. Rules can be changed dynamically through tools such as `firewall-cmd`. Red Hat1

Its current default backend is nftables. The `firewalld` service creates and manages its own rules; it is not a separate packet-filtering engine. [firewalld.org](https://firewalld.org/documentation/man-pages/firewalld.conf.html)

Common commands:

bash

```
sudo firewall-cmd --statesudo firewall-cmd --get-active-zonessudo firewall-cmd --list-all
```

## How they fit together

A typical arrangement looks like this:

text

```
UFW or firewalld        ↓ configuresnftables or iptables        ↓ sends rules toNetfilter in the Linux kernel        ↓ processesnetwork packets
```

There are variations. For example, UFW may call iptables-style tools, and those tools may use the nftables compatibility backend. The exact path depends on the distribution and configuration. ubuntu.com1

## Choosing one

- Choose UFW for a straightforward host firewall managed with simple allow/deny rules, especially if you already use it on Ubuntu.
- Choose firewalld if you want zones, named services, and dynamic management through a service-oriented interface.
- Choose nftables directly if you want detailed control over the ruleset and are comfortable managing chains, hooks, and priorities.
- Use iptables when you need compatibility with existing scripts or software that expects iptables commands. For a new ruleset, nftables is generally the newer interface.

In general, use one primary manager for the firewall rules on a machine. Running multiple tools that independently change rules can make the effective policy confusing. Some advanced setups deliberately combine them, but that requires understanding how their rules interact.

## Important distinction

“Using the `iptables` command” does not necessarily mean the kernel is running the old iptables backend. On many systems, the command may instead program nftables through a compatibility layer. To understand what is really active, check the backend reported by `iptables --version` and inspect the ruleset with `nft list ruleset`.