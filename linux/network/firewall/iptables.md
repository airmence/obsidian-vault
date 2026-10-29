iptables is a Linux command-line tool that lets an administrator set up IPv4 packet-filtering rules in the kernel firewall (Netfilter). Rules are organized into tables and chains, and iptables must be run as root (with elevated privileges).

## Overview of iptables

iptables is a command-line utility used in Linux for configuring the kernel firewall, specifically for managing IPv4 packet-filtering rules. It operates within the Netfilter framework, allowing system administrators to define how network traffic is handled.

### Key Features

- Packet Filtering: iptables allows for the inspection, modification, forwarding, and dropping of IP packets.
- Rule Organization: Rules are organized into tables and chains, where each table serves a specific purpose.
- Root Privileges Required: iptables must be executed with elevated privileges, typically by the root user.

## Structure of iptables

### Tables and Chains

iptables uses several tables, each containing chains of rules:

|Table Name|Purpose|
|---|---|
|filter|Default table for packet filtering|
|nat|Used for Network Address Translation|
|mangle|For specialized packet alteration|
|raw|Bypasses connection tracking|
|security|For security-related rules|

### Chain Types

Each table contains built-in chains:

- INPUT: Rules for incoming packets.
- OUTPUT: Rules for outgoing packets.
- FORWARD: Rules for packets being routed through the system.

## Basic Commands

Here are some common commands used with iptables:

- List Rules: `sudo iptables -L`
- Add Rule: `sudo iptables -A INPUT -s [source] -j [target]`
- Delete Rule: `sudo iptables -D INPUT [line number]`
- Save Rules: `sudo iptables-save > /etc/iptables/rules.v4`
- Restore Rules: `sudo iptables-restore < /etc/iptables/rules.v4`

## Conclusion

iptables is a powerful tool for managing network traffic on Linux systems. Understanding its structure and commands is essential for effective firewall management.