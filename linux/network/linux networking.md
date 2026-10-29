## Overview of Linux Networking

Linux networking encompasses the tools and configurations that enable Linux systems to communicate over various networks. This communication is facilitated through a set of protocols and command-line tools, allowing for effective management and security of network connections.

## Key Components of Linux Networking

### Protocols

Linux networking relies on several essential protocols:

- [[TCP - IP]]: The fundamental suite for data transmission.
- [[DHCP]]: Automatically assigns IP addresses to devices on the network.
- [[IPv4 - IPv6]]: Addressing schemes that identify devices on a network.

### Tools

Linux provides various command-line tools for network management:

- [[ip]] - A versatile tool for configuring network interfaces and routing.
- [[ifconfig]] - Displays and configures network interfaces.
- [[netstat]]  - Print network connections, routing tables, interface statistics, masquerade connections, and multicast memberships
- [[ss]] - another utility to investigate sockets (remplacement for aging netstat)
- [[nmap]] - A powerful port scanner for identifying open ports and services on remote systems.
- [[tcpdump]] - Captures and displays network traffic for analysis. (better alternative tshark or wireshark for GUI)

## Network Configuration and Management

### Configuration

Network configuration involves setting up network interfaces, routing, and DNS. Key aspects include:

- [[Network Interfaces]]: Represent physical or virtual network cards.
- Routing: Directs data packets between networks using routing tables.
- [[DNS]]: Resolves domain names to IP addresses for easier navigation.
- [[Firewall]]: Monitors network traffic and allows or blocks connections according to rules.
- [[port]]: A port is a numbered endpoint on a computer that helps network traffic reach the right app or service.

### Management

Effective network management includes monitoring and troubleshooting network performance. Common practices involve:

- Using tools like netstat and tcpdump for traffic analysis.
- Implementing firewalls to protect against unauthorized access.

## Conclusion

Linux networking is a critical aspect of system administration, providing the necessary infrastructure for communication between devices. Mastery of its components and tools is essential for effective network management and security.