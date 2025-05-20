Here are the correct answers for **14.5.6 Check Your Understanding – TCP Communication Process**:

---

### **Question 1**

**Which of the following would be valid source and destination ports for a host connecting to an email server?**

✅ **Source: 49152, Destination: 25**

> * **49152** is in the **ephemeral port range** (used by the client).
> * **Port 25** is the **well-known port** for **SMTP** (email sending).
>   → The client initiates the connection using a random high-numbered **source port** and connects to the **server's destination port 25**.

---

### **Question 2**

**Which control bit flags are used during the three-way handshake?**

✅ **SYN and ACK**

> * The **TCP three-way handshake** involves:

1. **SYN** from the client
2. **SYN-ACK** from the server
3. **ACK** from the client

---

### **Question 3**

**How many exchanges are needed to end both sessions between two hosts?**

✅ **Four exchanges**

> **TCP session termination** uses a **four-step** process:

1. Host A sends **FIN**
2. Host B responds with **ACK**
3. Host B sends **FIN**
4. Host A responds with **ACK**

---

Let me know if you want all quizzes bundled in a document or table format!
