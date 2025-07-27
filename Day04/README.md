 **TCP vs UDP (Comparison Table)**

| Feature                       | TCP (Transmission Control Protocol)                                | UDP (User Datagram Protocol)           |
| ----------------------------- | ------------------------------------------------------------------ | -------------------------------------- |
| **Connection Type**           | Connection-oriented                                                | Connectionless                         |
| **Reliability**               | Reliable (ensures delivery via acknowledgments and retransmission) | Unreliable (no delivery guarantees)    |
| **Speed**                     | Slower (more overhead due to connection setup and error checking)  | Faster (minimal overhead)              |
| **Error Checking**            | Yes (checksum, acknowledgment, retransmission)                     | Yes (checksum only, no retransmission) |
| **Ordering of Data**          | Maintains order of packets                                         | No guarantee of order                  |
| **Use Cases**                 | Email (SMTP), Web browsing (HTTP/HTTPS), File transfers (FTP)      | Streaming (video/audio), VoIP, DNS     |
| **Header Size**               | 20–60 bytes                                                        | 8 bytes                                |
| **Flow Control & Congestion** | Yes                                                                | No                                     |
| **Establishing Connection**   | Handshake (3-way handshake)                                        | No handshake required                  |

---

**What is a Subnet?**

* A **subnet** (short for *subnetwork*) is a smaller, logical division of an IP network.
* It allows network administrators to break a large network into smaller, more manageable parts.
* Subnetting improves network performance and security.
* Subnets are defined by a **subnet mask**, which specifies which portion of an IP address is the network vs. the host.

  **Example:**

  * IP Address: `192.168.1.0`
  * Subnet Mask: `255.255.255.0`
  * Here, the first 3 octets (`192.168.1`) define the network, and the last one (`.0-.255`) defines the host range.

---

**What is a Network?**

* A **network** is a collection of computers, servers, and other devices that are connected together to share resources (like files, internet, printers).
* Types of networks:

  * **LAN (Local Area Network):** Small geographic area (e.g., home, office)
  * **WAN (Wide Area Network):** Larger area (e.g., internet)
  * **MAN (Metropolitan Area Network):** City-scale
* Networks use protocols (like TCP/IP) for communication.

---

**What is a MAC ID (MAC Address)?**

* **MAC (Media Access Control) Address** is a unique identifier assigned to a network interface card (NIC) for communications at the data link layer (Layer 2).
* Format: `XX:XX:XX:XX:XX:XX` (6 bytes/48 bits in hexadecimal)
* It is **hardware-based** and typically **does not change**.
* Used **within local networks** to identify devices.
* Example: `00:1A:2B:3C:4D:5E`

---

**What is an IP Address?**

* An **IP (Internet Protocol) address** is a unique address that identifies a device on a network.
* It enables devices to send and receive data across networks.
* There are two types:

  * **IPv4:** 32-bit (e.g., `192.168.1.1`)
  * **IPv6:** 128-bit (e.g., `2001:0db8:85a3::8a2e:0370:7334`)
* IP addresses can be:

  * **Static:** Manually assigned and doesn't change
  * **Dynamic:** Assigned by DHCP and can change over time

---

**Difference Between IPv4 and IPv6**

| Feature            | IPv4 (Internet Protocol v4)   | IPv6 (Internet Protocol v6)                          |
| ------------------ | ----------------------------- | ---------------------------------------------------- |
| **Address Length** | 32 bits                       | 128 bits                                             |
| **Address Format** | Decimal (e.g., `192.168.1.1`) | Hexadecimal (e.g., `2001:0db8:85a3::8a2e:0370:7334`) |
| **Address Space**  | \~4.3 billion addresses       | 340 undecillion addresses                            |
| **Header Size**    | 20 bytes                      | 40 bytes                                             |
| **Security**       | Optional (IPSec optional)     | Mandatory support for IPSec                          |
| **NAT Support**    | Yes (widely used)             | Not needed (due to vast address space)               |
| **Configuration**  | Manual or via DHCP            | Auto-configuration available                         |
| **Deployment**     | Widely used                   | Gradually being adopted                              |


