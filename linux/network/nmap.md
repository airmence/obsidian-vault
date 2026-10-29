Nmap (Network Mapper) is a free, open-source tool for network discovery and security auditing, created by Gordon Lyon (Fyodor). It scans networks to discover hosts, services, open ports, and running applications, and can detect operating systems and vulnerabilities.

## Overview of Nmap

Nmap, short for Network Mapper, is a free and open-source tool designed for network discovery and security auditing. It was created by Gordon Lyon, also known as Fyodor. Nmap is widely used by system administrators, developers, and security professionals to assess network infrastructure.

## Key Features

Nmap offers a variety of features that make it a powerful tool for network analysis:

- Host Discovery: Identifies active devices on a network.
- Port Scanning: Detects open ports and the services running on them.
- Service Version Detection: Determines the version of services running on open ports.
- Operating System Detection: Identifies the operating system of remote hosts.
- Vulnerability Detection: Assesses potential vulnerabilities in network services.

## Scanning Methods

Nmap supports multiple scanning techniques, including:

|Scanning Method|Description|
|---|---|
|TCP Connect Scan|Establishes a full TCP connection to the target.|
|SYN Scan|Uses SYN packets to identify open ports stealthily.|
|UDP Scan|Scans for open UDP ports.|
|ICMP Ping Scan|Checks if hosts are reachable via ICMP echo requests.|
|FIN Scan|Sends FIN packets to probe for open ports.|

## Installation

Nmap can be installed on various operating systems using the following commands:

- Ubuntu/Debian: `sudo apt install nmap`
- CentOS/RHEL/Fedora: `sudo yum install nmap`
- macOS: `brew install nmap

## Usage Examples

Here are some basic commands to get started with Nmap:

1. Ping a Host: `nmap -sn 192.168.1.10`
2. Scan for Open Ports: `nmap 192.168.1.10`
3. Service Version Detection: `nmap -sV 192.168.1.10`
4. Full TCP Port Scan: `nmap -p- 192.168.1.10`

Nmap is an essential tool for network administrators and security professionals, providing critical insights into network configurations and potential vulnerabilities.
