Here's a quick summary and **Check Your Understanding** based on sections **13.2.1 to 13.2.5** about **Ping** and **Traceroute**:

---

### ✅ **Key Concepts Recap:**

#### 🔹 **Ping**

* Uses **ICMP Echo Request** and **Echo Reply** to test connectivity.
* Tests:

  * **Loopback (127.0.0.1 / ::1)**: Checks if IP stack is installed.
  * **Default Gateway**: Verifies local network connectivity.
  * **Remote Host**: Verifies end-to-end internetwork connectivity.

#### 🔹 **Traceroute (tracert)**

* Identifies each hop between source and destination.
* Uses increasing **TTL (IPv4)** or **Hop Limit (IPv6)** values.
* Routers send back **ICMP Time Exceeded** messages until the destination replies.
* Useful to locate delays or failures in a path.

---

### 📝 **Check Your Understanding Questions**

---

#### **Question 1**

Which of the following ping results confirms that TCP/IP is properly installed and functioning on a host?

**A.** Ping to default gateway
**B.** Ping to a remote host
**C.** Ping to 127.0.0.1
**D.** Ping to a DNS server

**✅ Correct Answer: C. Ping to 127.0.0.1**

> This loopback address confirms IP is installed and functioning locally.

---

#### **Question 2**

You ping a remote host and get no reply. What are two possible explanations? (Choose two.)

☐ The remote host is off
☐ Your computer is off
☐ A firewall is blocking ICMP
☐ The local gateway is not configured
☐ You mistyped the hostname

**✅ Correct Answers:**

* ✅ **The remote host is off**
* ✅ **A firewall is blocking ICMP**

---

#### **Question 3**

What does the **traceroute** utility help identify?

**A.** DNS resolution issues
**B.** Physical layer cable errors
**C.** Path of routers between source and destination
**D.** MAC addresses of remote hosts

**✅ Correct Answer: C. Path of routers between source and destination**

> Traceroute shows each hop (router) along the path to the destination.

---

#### **Question 4**

Which field in IPv4 and IPv6 headers does **traceroute** manipulate to get information about each hop?

**A.** Version
**B.** TTL / Hop Limit
**C.** Header Checksum
**D.** Destination Address

**✅ Correct Answer: B. TTL / Hop Limit**

---

Let me know if you'd like this as a table format for a report or README!
