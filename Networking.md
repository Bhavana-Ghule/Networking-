# Networking Notes

## What is Networking?

Networking is the process of connecting two or more computers or devices so that they can communicate, share data, and share resources.

## Types of Networks

- LAN (Local Area Network)
- MAN (Metropolitan Area Network)
- WAN (Wide Area Network)
- PAN (Personal Area Network)

---

# OSI Model

## 7. Application Layer
Provides an interface between the user and the network.

### Common Protocols
- HTTP
- HTTPS
- FTP
- SMTP
- DNS

---

## 6. Presentation Layer

Responsible for:
- Data formatting
- Encryption and decryption
- Compression
- Making data readable
  
Purpose:

Converts data into a readable format.
Encrypts and decrypts data.
Compresses and decompresses data.

----

## 5. Session Layer

Purpose:

Establishes, manages, and terminates communication sessions.
Controls dialogue between two communicating devices.

---

## 4. Transport Layer

Purpose:

Provides reliable end-to-end communication.
Performs segmentation and reassembly of data.
Handles error detection and flow control.

Data Unit: Segment
Protocols
TCP
UDP

---

### 3. Network Layer

Purpose:

Provides logical addressing (IP Address).
Determines the best path for data using routing.
Converts segments into packets.

Data Unit: Packet
Protocols
IP
ICMP
Device
Router

----

## 2. Data Link Layer

Purpose:

Uses MAC addresses for communication.
Detects errors.
Converts packets into frames.

Data Unit: Frame
Device
Switch

---

## 1. Physical Layer

Purpose:

Transmits raw binary data (0s and 1s) over the physical medium.
Defines cables, connectors, voltage, and transmission methods.

Data Unit: Bits
Devices
Hub
Repeater
Cables

----

# 🌐 IP Addressing

An **IP (Internet Protocol) Address** is a unique numerical address assigned to every device connected to a network. It allows devices to communicate with each other over a network.

---

# IPv4 (Internet Protocol Version 4)

IPv4 is the fourth version of the Internet Protocol and is the most widely used addressing scheme.

## Format

```text
192.168.1.10
```

## Features

- 32-bit address
- Consists of **4 octets**
- Each octet contains **8 bits**
- Each octet ranges from **0–255**
- Total possible addresses: **2³² ≈ 4.3 Billion**

### Structure

```text
Octet     Octet     Octet     Octet
 8 Bit     8 Bit     8 Bit     8 Bit

192       .168      .1        .10
```

---

# IPv6 (Internet Protocol Version 6)

IPv6 was introduced to overcome the shortage of IPv4 addresses.

## Format

```text
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

## Features

- 128-bit address
- Consists of **8 hexadecimal blocks**
- Each block contains **16 bits**
- Uses hexadecimal values (0-9, A-F)
- Total addresses: **2¹²⁸ ≈ 3.4 × 10³⁸**

### Structure

```text
Hexet : Hexet : Hexet : Hexet : Hexet : Hexet : Hexet : Hexet
 xxxx : xxxx : xxxx : xxxx : xxxx : xxxx : xxxx : xxxx
```

---

# IPv4 Address Classes

## Class A

| Property | Value |
|----------|-------|
| Range | 0.0.0.0 – 126.255.255.255 |
| Default Mask | 255.0.0.0 (/8) |
| Network Bits | 8 |
| Host Bits | 24 |
| Hosts | 16,777,214 |

### Format

```text
N.H.H.H
```

---

## Class B

| Property | Value |
|----------|-------|
| Range | 128.0.0.0 – 191.255.255.255 |
| Default Mask | 255.255.0.0 (/16) |
| Network Bits | 16 |
| Host Bits | 16 |
| Hosts | 65,534 |

### Format

```text
N.N.H.H
```

---

## Class C

| Property | Value |
|----------|-------|
| Range | 192.0.0.0 – 223.255.255.255 |
| Default Mask | 255.255.255.0 (/24) |
| Network Bits | 24 |
| Host Bits | 8 |
| Hosts | 254 |

### Format

```text
N.N.N.H
```

> **Note**
>
> A Class C network contains **256 addresses**, but only **254 are usable**.
>
> - 1 Network Address
> - 1 Broadcast Address

---

## Class D

| Property | Value |
|----------|-------|
| Range | 224.0.0.0 – 239.255.255.255 |
| Purpose | Multicast |

---

## Class E

| Property | Value |
|----------|-------|
| Range | 240.0.0.0 – 255.255.255.255 |
| Purpose | Research & Experimental |

---

# Special IP Addresses

## Broadcast Address

```text
255.255.255.255
```

Used to send packets to **all devices** in a network.

---

## Loopback Address
```text
127.0.0.1
```
Also called **localhost**.
Used to test the TCP/IP stack on the local machine.

---

# Network & Host Representation

```text
Class A → N.H.H.H
Class B → N.N.H.H
Class C → N.N.N.H
Class D → Multicast
Class E → Experimental
```
# 🌍 Types of IP Addresses

An IP address can be classified into different types based on its accessibility and assignment.

---

# Public IP Address

A **Public IP Address** is a globally unique IP address assigned by an **Internet Service Provider (ISP)**. It allows devices to communicate over the Internet.

## Features

- Globally unique
- Accessible from anywhere on the Internet
- Assigned by an ISP
- Required for hosting public services such as websites and mail servers

### Example

```text
8.8.8.8
142.250.183.110
```

### Uses

- Web Servers
- Cloud Servers
- Email Servers
- Internet Communication

---

# Private IP Address

A **Private IP Address** is used for communication within a private network (LAN). These addresses are **not routable** over the Internet.

## Private IP Ranges

| Class | Range |
|--------|--------------------------------|
| Class A | 10.0.0.0 – 10.255.255.255 |
| Class B | 172.16.0.0 – 172.31.255.255 |
| Class C | 192.168.0.0 – 192.168.255.255 |

### Example

```text
192.168.1.10
10.0.0.25
172.16.5.100
```

### Uses

- Home Networks
- Office Networks
- Schools
- Organizations

> **Note:** Private IP addresses require **NAT (Network Address Translation)** to access the Internet.

---

# Static IP Address

A **Static IP Address** is manually configured and remains the same unless changed by the administrator.

## Features

- Permanent IP address
- Does not change automatically
- More stable for hosting services

### Advantages

- Easy DNS configuration
- Suitable for servers
- Reliable remote access
- Better for CCTV and Web Hosting

### Disadvantages

- Manual configuration required
- Higher cost
- Less secure if exposed directly to the Internet

---

# Dynamic IP Address

A **Dynamic IP Address** is automatically assigned by a **DHCP (Dynamic Host Configuration Protocol) Server**.

## Features

- Assigned automatically
- Changes periodically
- Most common for home users

### Advantages

- Automatic configuration
- Easy management
- Better IP utilization
- Lower maintenance

### Disadvantages

- IP address may change
- Not suitable for hosting services without Dynamic DNS

---

# DHCP (Dynamic Host Configuration Protocol)

DHCP is responsible for automatically assigning IP addresses to devices connected to a network.

## DHCP Provides

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

### DHCP Process (DORA)

1. **Discover** – Client searches for a DHCP Server.
2. **Offer** – DHCP Server offers an available IP address.
3. **Request** – Client requests the offered IP address.
4. **Acknowledge** – DHCP Server confirms the assignment.

```text
Client
   │
   ├── Discover ─────────►
   │◄────── Offer ────────
   ├── Request ──────────►
   │◄── Acknowledge ──────
```
---

# Comparison

| Feature | Static IP | Dynamic IP |
|----------|-----------|------------|
| Assignment | Manual | Automatic |
| Changes | Never | Changes Automatically |
| Configuration | Administrator | DHCP Server |
| Cost | Higher | Lower |
| Best For | Servers | Home Users |

---

# Summary

- **Public IP** → Accessible over the Internet.
- **Private IP** → Used inside local networks.
- **Static IP** → Manually assigned and permanent.
- **Dynamic IP** → Automatically assigned by DHCP.
- **DHCP** → Automatically manages IP configuration for network devices.
