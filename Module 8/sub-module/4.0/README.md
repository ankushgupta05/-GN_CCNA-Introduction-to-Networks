Here's a summary of sections **8.4.1 to 8.4.4**:

---

### **8.4.1 Host Forwarding Decision**

* Hosts create and manage their own **routing tables** to determine how to forward packets.
* A host can send packets to:

  * **Itself** using loopback addresses (127.0.0.1 for IPv4, ::1 for IPv6).
  * **Local host** on the same network (same network address).
  * **Remote host** on a different network (different network address).
* Decision for local vs remote:

  * **IPv4**: Uses subnet mask and IP address.
  * **IPv6**: Uses router-advertised network prefix.
* Local hosts communicate through switches or wireless APs without routers.
* Communication with **remote hosts** requires **routers** and **routing**.
* The **default gateway** is the router that connects the local network to external networks.

---

### **8.4.2 Default Gateway**

* A **default gateway** is typically a **router** that:

  * Has a local IP in the same range as the host.
  * Can route traffic to other networks.
* It acts like a **doorway** to other networks.
* Without a configured or working default gateway, a host **cannot reach remote networks**.

---

### **8.4.3 A Host Routes to the Default Gateway**

* Hosts receive the default gateway via:

  * **IPv4**: From **DHCP** or manual setup.
  * **IPv6**: From router advertisement or manual setup.
* The gateway's address becomes the **default route** in the host’s routing table.
* This route is used when sending packets to **unknown or remote networks**.

---

### **8.4.4 Host Routing Tables**

* Use `netstat -r` or `route print` to view the **host routing table**.
* The output includes:

  * **Interface List**: Lists all network interfaces and MAC addresses.
  * **IPv4 Route Table**: Shows direct, local, and default routes.
  * **IPv6 Route Table**: Similar to IPv4 but for IPv6 addresses.
* Key entry: `0.0.0.0 0.0.0.0` points to the default gateway.

---

Would you like a visual diagram of the routing decision process?
