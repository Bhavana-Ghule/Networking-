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

## 5. Session Layer

Purpose:

Establishes, manages, and terminates communication sessions.
Controls dialogue between two communicating devices.

## 4. Transport Layer

Purpose:

Provides reliable end-to-end communication.
Performs segmentation and reassembly of data.
Handles error detection and flow control.

Data Unit: Segment

Protocols

TCP
UDP
3. Network Layer

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
2. Data Link Layer

Purpose:

Uses MAC addresses for communication.
Detects errors.
Converts packets into frames.

Data Unit: Frame

Device

Switch
1. Physical Layer

Purpose:

Transmits raw binary data (0s and 1s) over the physical medium.
Defines cables, connectors, voltage, and transmission methods.

Data Unit: Bits

Devices

Hub
Repeater
Cables
