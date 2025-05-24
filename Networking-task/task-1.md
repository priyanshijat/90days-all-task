## 📘 What is a Networking Model?
A *network model* is like a guide or blueprint that explains how data moves from one computer to another.

---

## 🧱 OSI Model (Open Systems Interconnection)

The *OSI model* has 7 layers and it is a way to understand **how computers talk to each other** over a network  .

## 🧩 The 7 Layers (Top to Bottom):

1. **Application Layer** - The software you use (eg., browser, email). 

2. **Presentation Layer** – Translates data (e.g., encryption, file formats).
3. **Session Layer** – Manages the conversation (start, keep alive, end).
4. **Transport Layer** – Breaks data into smaller parts and ensures correct delivery.
5. **Network Layer** – Finds the best route for the data (like GPS).
6. **Data Link Layer** – Ensures safe travel of data across the physical connection.
7. **Physical Layer** – Actual wires, signals, and hardware (like roads).
   

> **Example**: Sending a letter – writing it, translating it, packaging it, choosing a route, and delivering it.


## Layer 7:  Application Layer

* Converts data into formats that are readable by the Application Layer; also handles

    1) character encoding

    2) data compression

    3) encryption/decryption

* **Protocols**:

    * SSL ensures secure communication between devices by encrypting data, maintaining its integrity, and providing authentication.
    * TLS improves encryption, authentication, and overall security. TLS is widely used for secure web browsing, replacing SSL.
* **Example**: Watching a YouTube video where data is compressed and formatted correctly for display.

## Layer6: Presentation Layer
* Protocol Data Unit: Data

* It acts as a translator of data between a networking service and an application

* Converts data into formats that are readable by the Application Layer; also handles

  * character encoding
  * data compression
  * encryption/decryption
* **Protocols**:

  * SSL ensures secure communication between devices by encrypting data, maintaining its integrity, and providing authentication.
  * TLS improves encryption, authentication, and overall security. TLS is widely used for secure web browsing, replacing SSL.
* **Example**: Watching a YouTube video where data is compressed and formatted correctly for display.


## Layer 5:   Session Layer
* Responsible for establishing and managing active communication sessions between two devices.
* Protocol Data Unit: Data
* Enables two-way data exchanges, either one at a time or simultaneously, and helps in recovering from interruptions by using checkpoints.
* **Protocols**:

   * PPTP (Point-to-Point Tunneling Protocol)

   * RPCP (Remote Procedure Call Protocol) 
   *  SDP (Sockets Direct Protocol)
* **Example**: Maintaining your secure online banking session until you log out.

## Layer 4:   Transport Layer
* Protocol Data Unit: Segment, Datagram
* **Purpose**: Ensures complete and error-free data delivery between devices.
* **Protocols**: TCP (Transmission Control Protocol), UDP (User Datagram Protocol).
* **Example**: Streaming a movie on Netflix. TCP ensures all parts of the movie arrive in sequence.


## Layer 3:   Network Layer
* Protocol Data Unit: Packet
* Responsible for routing and forwarding packets across multiple networks.
* **Protocols**: IP (Internet Protocol), ICMP (Internet Control Message Protocol), OSPF (Open Shortest Path First).
* **Example**: When you visit www.example.com, IP addresses guide the data packets to the correct server location.

## Layer 2:   Data Link Layer
* Protocol Data Unit: Frame
* Handles reliable node-to-node data transmission and manages error detection.
* **Protocols**: Ethernet, Wi-Fi (IEEE 802.11), ARP (Address Resolution Protocol)
* **Example**: When your Wi-Fi router assigns a MAC address to your laptop, ensuring that your data packets don't collide with others.

## Layer 1:   Physical Link Layer
* Protocol Data Unit: Bit, Symbol
* Responsible for transmission and reception of raw bit streams over a physical medium.
* **Technologies**: Ethernet cables, fiber optics, radio frequencies
* **Example**: Connecting your laptop to the internet using a LAN cable or Wi-Fi signals.


## 💻 TCP/IP Model (Used on the Internet)

The *TCP/IP model* is the *real-world version* of how data moves online. It has *4 layers*:

### 🧩 The 4 Layers (Top to Bottom):

1. **Application Layer** – User-facing apps like WhatsApp, email, browser.
2. **Transport Layer** – Ensures all data arrives correctly (uses TCP or UDP).
3. **Internet Layer** – Finds and follows the best route (uses IP).
4. **Network Access Layer** – Deals with actual hardware and cables.


## 1. Application Layer
* The top layer of the TCP/IP model.

* Equivalent to OSI Application, Presentation, and Session Layers

* Responsible for end-to-end communication and error-free delivery of data.
* **Protocols**:

   * HTTP (Hypertext Transfer Protocol) and HTTPS (Hypertext Transfer Protocol Secure) - manage communications between web browsers and servers
   * SSH (Secure Shell) - sets up a secure encrypted session over a TCP/IP connection
   * NTP (Network Time Protocol) - used to synchronize the clocks on our computer to one standard time source

## 2. Transport Layer
* Same as OSI Transport Layer.

* Exchange data receipt acknowledgments and retransmit missing packets to ensure that packets arrive in order and without error.

* Determines how data will be transmitted, includes

   * checking the correct ports
   * the integrity of the data
   * and basically delivering our packets.
* **Protocols**:

   * TCP (Transmission Control Protocol) - reliable data delivery
   * UDP (User Datagram Protocol) - unreliable data delivery

## 3. Internet Layer
* It has same functionality as the OSI Network layer.
* Responsible for the logical transmission of data over the entire network.
* **Protocols**:
   * IP (Internet Protocol) - Helps route packets from one machine to another.
   * ICMP (Internet Control Message Protocol) - Helps tell us what is going on, such as error messages and debugging information.

## 4. Network Access Layer
* This layer specifies how to send data across a physical piece of hardware.
* Equivalent to Physical & Data Link Layers.
* **Examples**: Data travelling through Ethernet, fiber, etc....

## This All About OSI and TCP/IP Model.
---


