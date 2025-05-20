Here are the answers for your questions, along with explanations where helpful:

---

### Question 1

**Which protocol or service uses UDP for client-to-server communication and TCP for server-to-server communication?**

* ⭕ FTP
* ✅ **DNS**
* ⭕ SMTP
* ⭕ HTTP

*Explanation:* DNS queries from clients typically use UDP for speed, but DNS zone transfers between servers use TCP.

---

### Question 2

**What kind of port must be requested from IANA in order to be used with a specific application?**

* ✅ **registered port**
* ⭕ dynamic port
* ⭕ source port
* ⭕ private port

*Explanation:* Registered ports are assigned by IANA for specific applications.

---

### Question 3

**Order the TCP termination process steps:**

Steps and options:

* client sends FIN.
* server sends ACK.
* client sends SYN.
* client sends ACK.

Correct order:

1. **client sends FIN.** (C)
2. **server sends ACK.** (D)
3. **server sends FIN.** (not listed but logically next step)
4. **client sends ACK.** (B)

Since “server sends FIN” is missing from the options, assuming the question expects only partial steps, the known termination steps are:

* Step 1: client sends FIN (C)
* Step 2: server sends ACK (D)
* Step 3: server sends FIN (not listed)
* Step 4: client sends ACK (B)

---

### Question 4

**Which two types of applications are best suited for UDP? (Choose two.)**

* ⭕ applications that need the reordering of segments
* ✅ applications that handle reliability themselves
* ✅ applications that can tolerate some data loss, but require little or no delay
* ⭕ applications that need data flow control
* ⭕ applications that require reliable delivery

---

### Question 5

**What does a client do when it has UDP datagrams to send?**

* ⭕ It queries the server to see if it is ready to receive data.
* ⭕ It sends a simplified three-way handshake to the server.
* ⭕ It sends to the server a segment with the SYN flag set to synchronize the conversation.
* ✅ It just sends the datagrams.

---

### Question 6

**What important information is added to the TCP/IP transport layer header to ensure communication and connectivity with a remote network device?**

* ⭕ destination and source logical network addresses
* ⭕ timing and synchronization
* ⭕ destination and source physical addresses
* ✅ destination and source port numbers

---

### Question 7

**What is a characteristic of UDP?**

* ⭕ UDP only passes data to the network when the destination is ready to receive the data.
* ⭕ UDP datagrams take the same path and arrive in the correct order at the destination.
* ✅ Applications that use UDP are always considered unreliable.
* ⭕ UDP reassembles the received datagrams in the order they were received.

---

### Question 8

**What are three responsibilities of the transport layer? (Choose three.)**

* ✅ multiplexing multiple communication streams from many users or applications on the same network
* ⭕ formatting data into a compatible form for receipt by the destination devices
* ✅ meeting the reliability requirements of applications, if any
* ✅ identifying the applications and services on the client and server that should handle transmitted data
* ⭕ conducting error detection of the contents in frames
* ⭕ directing packets towards the destination network

---

### Question 9

**Which two characteristics are associated with UDP sessions? (Choose two.)**

* ⭕ Unacknowledged data packets are retransmitted.
* ✅ Destination devices receive traffic with minimal delay.
* ⭕ Transmitted data segments are tracked.
* ✅ Received data is unacknowledged.
* ⭕ Destination devices reassemble messages and pass them to an application.

---

### Question 10

**Which two fields are included in the TCP header but not in the UDP header? (Choose two.)**

* ⭕ source port
* ✅ window
* ⭕ destination port
* ✅ sequence number
* ⭕ checksum

---

### Question 11

**A PC is downloading a large file from a server. The TCP window is 1000 bytes. The server is sending the file using 100-byte segments. How many segments will the server send before it requires an acknowledgment from the PC?**

* ⭕ 1000 segments
* ⭕ 100 segments
* ⭕ 1 segment
* ✅ **10 segments**

*Explanation:* Window size is 1000 bytes, segment size 100 bytes, so 1000/100 = 10 segments before ACK needed.

---

If you'd like, I can help create a summary table or provide more explanation for any of these!
Here are the answers for your new set of questions with explanations where helpful:

---

### Question 12

**In what two situations would UDP be better than TCP as the preferred transport protocol? (Choose two.)**

* ✅ when a faster delivery mechanism is needed
* ⭕ when destination port numbers are dynamic
* ⭕ when delivery overhead is not an issue
* ⭕ when applications need to guarantee that a packet arrives intact, in sequence, and unduplicated
* ✅ when applications do not need to guarantee delivery of the data

---

### Question 13

**What are two roles of the transport layer in data communication on a network? (Choose two.)**

* ✅ identifying the proper application for each communication stream
* ✅ providing the interface between applications and the underlying network over which messages are transmitted
* ⭕ providing frame delimiting to identify bits making up a frame
* ✅ tracking the individual communication between applications on the source and destination hosts
* ⭕ performing a cyclic redundancy check on the frame for errors

---

### Question 14

**Which factor determines TCP window size?**

* ⭕ the amount of data to be transmitted
* ⭕ the amount of data the source is capable of sending at one time
* ✅ the amount of data the destination can process at one time
* ⭕ the number of services included in the TCP segment

---

### Question 15

**Which OSI layer provides the interface between the applications used to communicate and the underlying network over which messages are transmitted?**

* ⭕ presentation
* ⭕ session
* ✅ application
* ⭕ transport

---

### Question 16

**What is an example of network communication that uses the client-server model?**

* ⭕ A workstation initiates an ARP to find the MAC address of a receiving host.
* ✅ A workstation initiates a DNS request when the user types [www.cisco.com](http://www.cisco.com) in the address bar of a web browser.
* ⭕ A user uses eMule to download a file that is shared by a friend after the file location is determined.
* ⭕ A user prints a document by using a printer that is attached to a workstation of a coworker.

---

### Question 17

**Which application layer protocol uses message types such as GET, PUT, and POST?**

* ⭕ DHCP
* ⭕ DNS
* ⭕ SMTP
* ✅ HTTP
* ⭕ POP3

---

### Question 18

**A manufacturing company subscribes to certain hosted services from its ISP. The services that are required include hosted world wide web, file transfer, and e-mail. Which protocols represent these three key applications? (Choose three.)**

* ✅ SMTP
* ✅ FTP
* ⭕ DHCP
* ⭕ DNS
* ⭕ SNMP
* ✅ HTTP

---

### Question 19

**In what networking model would eDonkey, eMule, BitTorrent, Bitcoin, and LionShare be used?**

* ⭕ client-based
* ✅ peer-to-peer
* ⭕ master-slave
* ⭕ point-to-point

---

### Question 20

**What is a common protocol that is used with peer-to-peer applications such as WireShare, Bearshare, and Shareaza?**

* ⭕ SMTP
* ⭕ Ethernet
* ⭕ POP
* ✅ Gnutella

---

### Question 21

**Which applications or services allow hosts to act as client and server at the same time?**

* ✅ P2P applications
* ⭕ client/server applications
* ⭕ email applications
* ⭕ authentication services

---

### Question 22

**Which networking model is being used when an author uploads one chapter document to a file server of a book publisher?**

* ✅ client/server
* ⭕ point-to-point
* ⭕ peer-to-peer
* ⭕ master-slave

---

If you want, I can prepare these answers in a formatted table or explain any question in more detail!
Here are the answers for your next set of questions with explanations:

---

### Question 23

**Which three protocols operate at the application layer of the TCP/IP model? (Choose three.)**

* ⭕ UDP
* ✅ POP3
* ✅ DHCP
* ⭕ TCP
* ⭕ ARP
* ✅ FTP

---

### Question 24

**The application layer of the TCP/IP model performs the functions of what three layers of the OSI model? (Choose three.)**

* ✅ presentation
* ⭕ network
* ⭕ data link
* ⭕ physical
* ✅ session
* ✅ application
* ⭕ transport

---

### Question 25

**What is true about the Server Message Block protocol?**

* ⭕ SMB messages cannot authenticate a session.
* ✅ Clients establish a long term connection to servers.
* ⭕ Different SMB message types have a different format.
* ⭕ SMB uses the FTP protocol for communication.

---

### Question 26

**What is the function of the HTTP GET message?**

* ✅ to request an HTML page from a web server
* ⭕ to retrieve client email from an email server using TCP port 110
* ⭕ to upload content to a web server from a web client
* ⭕ to send error information from a web server to a web client

---

### Question 27

**What is a key characteristic of the peer-to-peer networking model?**

* ✅ resource sharing without a dedicated server
* ⭕ network printing using a print server
* ⭕ social networking without the Internet
* ⭕ wireless networking

---

### Question 28

**What is an advantage of SMB over FTP?**

* ⭕ Only SMB establishes two simultaneous connections with the client, making the data transfer faster.
* ✅ SMB clients can establish a long-term connection to the server.
* ⭕ Only with SMB can data transfers occur in both directions.
* ⭕ SMB is more reliable than FTP because SMB uses TCP and FTP uses UDP.

---

### Question 29

**Which three layers of the OSI model provide similar network services to those provided by the application layer of the TCP/IP model? (Choose three.)**

* ⭕ physical layer
* ✅ presentation layer
* ✅ session layer
* ✅ application layer
* ⭕ transport layer
* ⭕ data link layer

---

### Question 30

**Which scenario describes a function provided by the transport layer?**

* ⭕ A student is playing a short web-based movie with sound. The movie and sound are encoded within the transport layer header.
* ⭕ A corporate worker is accessing a web server located on a corporate network. The transport layer formats the screen so the web page appears properly no matter what device is being used to view the web site.
* ✅ A student has two web browser windows open in order to access two web sites. The transport layer ensures the correct web page is delivered to the correct browser window.
* ⭕ A student is using a classroom VoIP phone to call home. The unique identifier burned into the phone is a transport layer address used to contact another network device on the same network.

---

### Question 31

**A PC that is communicating with a web server has a TCP window size of 6,000 bytes when sending data and a packet size of 1,500 bytes. Which byte of information will the web server acknowledge after it has received four packets of data from the PC?**

* ⭕ 3001
* ⭕ 1500
* ✅ 6001
* ⭕ 3000

**Explanation:**
4 packets × 1500 bytes = 6000 bytes received. TCP acknowledges the next expected byte, which is byte number 6001.

---

### Question 32

**A client creates a packet to send to a server. The client is requesting SMTP service. What number will be used as the destination port number in the sending packet?**

* ⭕ 110
* ⭕ 443
* ✅ 25
* ⭕ 161

---

If you want me to organize this into a neat table or want further explanation, just ask!
