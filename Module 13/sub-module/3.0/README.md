Here are the **correct answers** to the **13.3.4 Module Quiz - ICMP** along with **all options** for each question:

---

### **Question 1**

**Q:** A technician is troubleshooting a network where it is suspected that a defective node in the network path is causing packets to be dropped. The technician only has the IP address of the end point device and does not have any details of the intermediate devices. What command can the technician use to identify the faulty node?

* 🔘 **tracert** ✅
* 🔘 ping
* 🔘 ipconfig /flushdns
* 🔘 ipconfig /displaydns
  **Answer:** `tracert` helps identify intermediate routers where packets may be failing.

---

### **Question 2**

**Q:** A user who is unable to connect to the file server contacts the help desk. The helpdesk technician asks the user to ping the IP address of the default gateway that is configured on the workstation. What is the purpose for this ping command?

* 🔘 To obtain a dynamic IP address from the server
* 🔘 To request that gateway forward the connection request to the file server
* 🔘 **To test that the host has the capability to reach hosts on other networks** ✅
* 🔘 To resolve the domain name of the file server to its IP address

---

### **Question 3**

**Q:** What is a function of the tracert command that differs from the ping command when they are used on a workstation?

* 🔘 The tracert command reaches the destination faster.
* 🔘 **The tracert command shows the information of routers in the path.** ✅
* 🔘 The tracert command sends one ICMP message to each hop in the path.
* 🔘 The tracert command is used to test the connectivity between two devices.

---

### **Question 4**

**Q:** Which ICMP message is used by the traceroute utility during the process of finding the path between two end hosts?

* 🔘 Redirect
* 🔘 Ping
* 🔘 **Time exceeded** ✅
* 🔘 Destination unreachable

---

### **Question 5**

**Q:** Which utility uses the Internet Control Messaging Protocol (ICMP)?

* 🔘 RIP
* 🔘 DNS
* 🔘 **Ping** ✅
* 🔘 NTP

---

### **Question 6**

**Q:** Which protocol is used by IPv4 and IPv6 to provide error messaging?

* 🔘 **ICMP** ✅
* 🔘 NDP
* 🔘 ARP
* 🔘 DHCP

---

### **Question 7**

**Q:** A network administrator is testing network connectivity by issuing the ping command on a router. Which symbol will be displayed to indicate that a time expired during the wait for an ICMP echo reply message?

* 🔘 !
* 🔘 **.** ✅
* 🔘 U
* 🔘 \$
  **Explanation:** `.` indicates a timeout in ping replies on Cisco routers.

---

### **Question 8**

**Q:** Which two things can be determined by using the ping command? (Choose two.)

* ⬜ The number of routers between the source and destination device
* ⬜ The IP address of the router nearest the destination device
* ✅ **The average time it takes a packet to reach the destination and for the response to return to the source**
* ✅ **The destination device is reachable through the network**
* ⬜ The average time it takes each router in the path between source and destination to respond

---

### **Question 9**

**Q:** A user calls to report that a PC cannot access the internet. The network technician asks the user to issue the command `ping 127.0.0.1`. The user reports that the result is four positive replies. What conclusion can be drawn based on this test?

* 🔘 The PC can access the network. The problem exists beyond the local network.
* 🔘 The IP address obtained from the DHCP server is correct.
* 🔘 The PC can access the Internet. However, the web browser may not work.
* 🔘 **The TCP/IP implementation is functional.** ✅
  **Explanation:** Pinging `127.0.0.1` tests the local TCP/IP stack.

---

### **Question 10**

**Q:** Which command can be used to test connectivity between two devices using echo request and echo reply messages?

* 🔘 netstat
* 🔘 ipconfig
* 🔘 ICMP
* 🔘 **ping** ✅

---

### **Question 11**

**Q:** What field content is used by ICMPv6 to determine that a packet has expired?

* 🔘 TTL field
* 🔘 CRC field
* 🔘 **Hop Limit field** ✅
* 🔘 Time Exceeded field

---

### **Question 12**

**Q:** Which protocol provides feedback from the destination host to the source host about errors in packet delivery?

* 🔘 ARP
* 🔘 BOOTP
* 🔘 DNS
* 🔘 **ICMP** ✅

---

### **Question 13**

**Q:** A network administrator can successfully ping the server at [www.cisco.com](http://www.cisco.com), but cannot ping the company web server located at an ISP in another city. Which tool or command would help identify the specific router where the packet was lost or delayed?

* 🔘 ipconfig
* 🔘 netstat
* 🔘 telnet
* 🔘 **traceroute** ✅

---

### **Question 14**

**Q:** What message is sent by a host to check the uniqueness of an IPv6 address before using that address?

* 🔘 **Neighbor solicitation** ✅
* 🔘 ARP request
* 🔘 Echo request
* 🔘 Router solicitation

---

Let me know if you want this in a **table format** or **Markdown-ready README file**.
