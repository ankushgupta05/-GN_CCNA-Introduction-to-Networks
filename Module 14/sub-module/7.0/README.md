Certainly! Here's the full set of questions with **all options** shown, the **correct answer marked**, and **brief explanations**:

---

### **Question 1**

**Why is UDP desirable for protocols that make a simple request and reply transactions?**

* ⭕ Flow Control
* ✅ **Low overhead**
* ⭕ Reliability
* ⭕ Same-order delivery

> **Explanation:** UDP is fast and efficient because it doesn't establish a connection, provide reliability, or sequence data. This **low overhead** makes it suitable for simple request-response protocols like DNS.

---

### **Question 2**

**Which UDP datagram reassembly statement is true?**

* ✅ **UDP does not reassemble the data.**
* ⭕ UDP reassembles the data in the order that it was received.
* ⭕ UDP reassembles the data using control bits.
* ⭕ UDP reassembles the data using sequence numbers.

> **Explanation:** Unlike TCP, **UDP does not handle data reassembly**. If the data is too large for a single datagram, IP-level fragmentation and reassembly are used, not by UDP itself.

---

### **Question 3**

**Which of the following would be valid source and destination ports for a host connecting to a DNS server?**

* ⭕ Source: 53, Destination: 49152
* ⭕ Source: 1812, Destination: 49152
* ✅ **Source: 49152, Destination: 53**
* ⭕ Source: 49152, Destination: 1812

> **Explanation:**

* Port **53** is the **well-known DNS port**.
* Clients initiate requests from an **ephemeral port** (like 49152) to the **server's port 53**.
* So the valid socket pair is: **49152 (source) → 53 (destination)**.

---

Let me know if you want this added to a markdown/table format for your notes!
