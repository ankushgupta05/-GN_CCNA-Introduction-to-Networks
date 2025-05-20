Here are the correct answers for **14.4.5 Check Your Understanding – Port Numbers**:

---

### **Question 1**

**Assume a host with IP address 10.1.1.10 wants to request web services from a server at 10.1.1.254. Which of the following would display the correct socket pair?**

✅ **10.1.1.10:1099, 10.1.1.254:80**

> When a client initiates a web request:

* It uses a **random ephemeral (high-numbered)** source port (e.g., 1099).
* It connects to the server's **well-known port 80** (for HTTP).
* Format: **ClientIP\:SourcePort, ServerIP\:DestinationPort**

---

### **Question 2**

**Which port group includes port numbers for FTP, HTTP, and TFTP applications?**

✅ **Well-known ports**

> **Well-known ports (0–1023)** are reserved for common protocols like:

* FTP (Port 21)
* HTTP (Port 80)
* TFTP (Port 69)

---

### **Question 3**

**Which Windows command would display the protocols in use, the local address and port numbers, the foreign address and port numbers, and the connection state?**

✅ **Netstat**

> **`netstat`** (network statistics) displays:

* Protocols in use
* Local/foreign IP addresses and port numbers
* Connection states (e.g., ESTABLISHED, LISTENING)

---

Let me know if you'd like all quiz sets compiled into a markdown or PDF document for study purposes!
