Here is the **14.8.3 Module Quiz – Transport Layer** with **all options**, the **correct answer marked**, and an **explanation** for each:

---

### ✅ **Question 1**

**Which transport layer feature is used to establish a connection-oriented session?**

* ⭕ UDP ACK flag
* ✅ **TCP 3-way handshake**
* ⭕ UDP sequence number
* ⭕ TCP port number

**Explanation:**
TCP uses a 3-way handshake to establish a reliable, connection-oriented session.

---

### ✅ **Question 2**

**What is the complete range of TCP and UDP well-known ports?**

* ⭕ 0 to 255
* ✅ **0 to 1023**
* ⭕ 256 - 1023
* ⭕ 1024 - 49151

**Explanation:**
Ports 0–1023 are reserved for well-known services such as HTTP (80), FTP (21), and DNS (53).

---

### ✅ **Question 3**

**What is a socket?**

* ⭕ The combination of the source and destination IP address and source and destination Ethernet address
* ✅ **The combination of a source IP address and port number or a destination IP address and port number**
* ⭕ The combination of the source and destination sequence and acknowledgment numbers
* ⭕ The combination of the source and destination sequence numbers and port numbers

**Explanation:**
A socket identifies the communication endpoint using an IP address and port number.

---

### ✅ **Question 4**

**How does a networked server manage requests from multiple clients for different services?**

* ⭕ The server sends all requests through a default gateway.
* ✅ **Each request has a combination of source and destination port numbers, coming from a unique IP address.**
* ⭕ The server uses IP addresses to identify different services.
* ⭕ Each request is tracked through the physical address of the client.

**Explanation:**
Ports allow the server to distinguish between different services and clients.

---

### ✅ **Question 5**

**What happens if part of an FTP message is not delivered to the destination?**

* ⭕ The message is lost because FTP does not use a reliable delivery method.
* ⭕ The FTP source host sends a query to the destination host.
* ✅ **The part of the FTP message that was lost is re-sent.**
* ⭕ The entire FTP message is re-sent.

**Explanation:**
FTP uses TCP, which retransmits lost segments, not the entire message.

---

### ✅ **Question 6**

**What type of applications are best suited for using UDP?**

* ✅ **Applications that are sensitive to delay**
* ⭕ Applications that need reliable delivery
* ⭕ Applications that require retransmission of lost segments
* ⭕ Applications that are sensitive to packet loss

**Explanation:**
UDP is faster and ideal for real-time apps (like VoIP) where delays are more critical than occasional data loss.

---

### ✅ **Question 7**

**Network congestion has resulted in the source learning of the loss of TCP segments. What is one way TCP addresses this?**

* ✅ **The source decreases the amount of data that it transmits before it receives an acknowledgement from the destination.**
* ⭕ The source decreases the window size to decrease the rate of transmission from the destination.
* ⭕ The destination decreases the window size.
* ⭕ The destination sends fewer acknowledgement messages in order to conserve bandwidth.

**Explanation:**
TCP uses congestion control to reduce the data flow until acknowledgments confirm successful delivery.

---

### ✅ **Question 8**

**Which two operations are provided by TCP but not by UDP?** *(Choose two)*

* ⭕ Identifying the applications
* ✅ **Acknowledging received data**
* ⭕ Identifying individual conversations
* ✅ **Retransmitting any unacknowledged data**
* ⭕ Reconstructing data in the order received

**Explanation:**
TCP provides acknowledgment and retransmission, which are not available in UDP.

---

### ✅ **Question 9**

**What is the purpose of using a source port number in a TCP communication?**

* ⭕ To notify the remote device that the conversation is over
* ⭕ To assemble the segments that arrived out of order
* ✅ **To keep track of multiple conversations between devices**
* ⭕ To inquire for a nonreceived segment

**Explanation:**
Source ports allow the device to manage multiple sessions with different applications.

---

### ✅ **Question 10**

**Which two flags in the TCP header are used in a TCP three-way handshake?** *(Choose two)*

* ✅ **ACK**
* ⭕ FIN
* ⭕ PSH
* ⭕ RST
* ✅ **SYN**
* ⭕ URG

**Explanation:**
SYN and ACK flags are exchanged during the three-way handshake to establish a TCP connection.

---

### ✅ **Question 11**

**What TCP mechanism enhances performance by allowing continuous sending of segments while receiving acknowledgments?**

* ⭕ Three-way handshake
* ⭕ Socket pair
* ⭕ Two-way handshake
* ✅ **Sliding window**

**Explanation:**
The sliding window allows more efficient transmission by sending multiple segments before waiting for ACKs.

---

### ✅ **Question 12**

**What does a client do when establishing communication with a server using UDP?**

* ⭕ The client sets the window size for the session.
* ⭕ The client sends an ISN to the server to start the 3-way handshake.
* ✅ **The client randomly selects a source port number.**
* ⭕ The client sends a synchronization segment to begin the session.

**Explanation:**
UDP is connectionless, so the client simply chooses a source port and sends data directly.

---

### ✅ **Question 13**

**Which two services or protocols use UDP for fast transmission and low overhead?** *(Choose two)*

* ⭕ FTP
* ✅ **DNS**
* ⭕ HTTP
* ⭕ POP3
* ✅ **VoIP**

**Explanation:**
DNS and VoIP use UDP to reduce delay and avoid overhead, favoring speed over reliability.

---

### ✅ **Question 14**

**Which number or set of numbers represents a socket?**

* ⭕ 01-23-45-67-89-AB
* ⭕ 21
* ✅ **192.168.1.1:80**
* ⭕ 10.1.1.15

**Explanation:**
A socket is represented by an IP address and a port number (e.g., IP\:Port).

---

### ✅ **Question 15**

**What is a responsibility of transport layer protocols?**

* ⭕ Providing network access
* ✅ **Tracking individual conversations**
* ⭕ Determining the best path to forward a packet
* ⭕ Translating private IP addresses to public IP addresses

**Explanation:**
Transport layer tracks sessions (conversations) between applications on source and destination hosts.

---

Let me know if you'd like this exported as a table or markdown file!
