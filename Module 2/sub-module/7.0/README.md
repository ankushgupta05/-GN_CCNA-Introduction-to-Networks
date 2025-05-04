Here is the content added in a clear and organized way for your `README.md` file:

---

## 💻 2.7.3 Syntax Checker – Verify Windows PC IP Configuration

To **check IP settings** on a Windows PC, you can use the **Command Prompt**.

### ✅ Command:

```bash
ipconfig
```

### 📄 Sample Output:

```
C:\>ipconfig

Windows IP Configuration

Ethernet adapter Local Area Connection:

   Connection-specific DNS Suffix  . : cisco.com
   Link-local IPv6 Address . . . . . : fe80::b0ef:ca42:af2c:c6c7%16
   IPv4 Address. . . . . . . . . . . : 192.168.1.10
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . : 192.168.1.1
```

This output confirms the IPv4 address, subnet mask, and default gateway assigned to the PC—either manually or via DHCP.

---
Here's the explanation written in clear markdown format for your `README.md` file:

---




## 🔧 2.7.4 Switch Virtual Interface (SVI) Configuration

To allow **remote management of a switch**, an **IP address must be assigned to a Switch Virtual Interface (SVI)**. An SVI does not refer to a physical port but a **virtual interface**, typically `VLAN 1`.

### 📘 Steps to Configure SVI on a Switch:

1. Enter global configuration mode.
2. Enter VLAN 1 interface configuration.
3. Assign an IPv4 address and subnet mask.
4. Enable the interface using `no shutdown`.
5. (Optional but common) Set the **default gateway** for remote communication.

### ✅ Example Configuration:

```bash
Sw-Floor-1# configure terminal
Sw-Floor-1(config)# interface vlan 1
Sw-Floor-1(config-if)# ip address 192.168.1.20 255.255.255.0
Sw-Floor-1(config-if)# no shutdown
Sw-Floor-1(config-if)# exit
Sw-Floor-1(config)# ip default-gateway 192.168.1.1
```

### 💡 Notes:

* `interface vlan 1` creates a virtual interface.
* `ip address` assigns the IPv4 address to the SVI.
* `no shutdown` activates the interface.
* `ip default-gateway` sets the path for the switch to communicate outside its subnet (i.e., to a router).

This setup allows the switch to be managed over the network just like any other IP-enabled device.

---

Would you like the next section added in the same format?
