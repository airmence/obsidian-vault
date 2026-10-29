## Definition of a Network Port

A network port is a virtual point in a computer network where network connections begin and end. It is a software-based construct managed by an operating system, allowing computers to differentiate between various types of network traffic. This enables multiple services to operate simultaneously over a single physical connection.

## Functionality of Network Ports

### Key Functions

- Multiplexing: Ports allow a single computer to run multiple network services at the same time.
- Service Identification: They help the operating system forward incoming data to the correct application or service.

### How Ports Work

- Addressing: Each network communication requires an IP address and a port number. The IP address identifies the device, while the port number identifies the specific service on that device.
- Socket Creation: Applications create a socket, which is a combination of an IP address and a port number, to establish a network connection.

## Commonly Used Port Numbers

|Port Number|Protocol|Purpose|
|---|---|---|
|20|FTP|File Transfer Protocol (data transfer)|
|21|FTP|File Transfer Protocol (control)|
|22|SSH|Secure Shell (secure remote access)|
|25|SMTP|Simple Mail Transfer Protocol (email)|
|80|HTTP|Hypertext Transfer Protocol (web traffic)|
|443|HTTPS|Secure HTTP (encrypted web traffic)|
|53|DNS|Domain Name System (name resolution)|
|123|NTP|Network Time Protocol (time synchronization)|

## Importance of Network Ports

Network ports are crucial for efficient communication in modern networks. They enable devices to handle various types of traffic, such as web browsing, email, and file transfers, all through a single connection. Understanding how ports function is essential for network administrators, developers, and anyone involved in network management.

you can see more by printing the file **==🔵/etc/services==**