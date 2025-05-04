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

Here’s how you can write section **2.7.5** in your `README.md` file using a clear and structured format:

---

## ⚙️ 2.7.5 Syntax Checker - Configure a Switch Virtual Interface

This section demonstrates how to configure a **Switch Virtual Interface (SVI)** on VLAN 1 to enable network communication and remote management.

### 🛠️ Step-by-Step Configuration:

1. **Enter interface configuration mode for VLAN 1**:

   ```bash
   Switch(config)#interface vlan 1
   ```

2. **Configure the IPv4 address and subnet mask**:

   ```bash
   Switch(config-if)#ip address 192.168.1.20 255.255.255.0
   ```

3. **Enable the interface**:

   ```bash
   Switch(config-if)#no shutdown
   %LINK-5-CHANGED: Interface Vlan1, changed state to up
   ```

### ✅ Result:

You have successfully configured the switch virtual interface for **VLAN 1**. This allows the switch to participate in the network and be accessed remotely for management.

---






Here are **all the commands** from the Cisco Packet Tracer exercise **“2.7.6 - Implement Basic Connectivity”**, organized step-by-step for configuring switches and PCs:

---

## ✅ **Part 1: Basic Configuration on S1 and S2**

### S1 Configuration

```plaintext
enable
configure terminal
hostname S1

line console 0
password cisco
login
exit

enable secret class

banner motd #Authorized access only. Violators will be prosecuted to the full extent of the law.#

end
write memory
```

### Repeat the same for S2

```plaintext
enable
configure terminal
hostname S2

line console 0
password cisco
login
exit

enable secret class

banner motd #Authorized access only. Violators will be prosecuted to the full extent of the law.#

end
write memory
```

---

## ✅ **Part 2: Configure PCs**

### PC1

* Go to **Desktop > IP Configuration**
* Set:

  ```plaintext
  IP Address: 192.168.1.1
  Subnet Mask: 255.255.255.0
  ```

### PC2

* Go to **Desktop > IP Configuration**
* Set:

  ```plaintext
  IP Address: 192.168.1.2
  Subnet Mask: 255.255.255.0
  ```

---

## ✅ **Part 3: Configure the Switch Management Interface**

### On S1

```plaintext
enable
configure terminal
interface vlan 1
ip address 192.168.1.253 255.255.255.0
no shutdown
exit
end
write memory
```

### On S2

```plaintext
enable
configure terminal
interface vlan 1
ip address 192.168.1.254 255.255.255.0
no shutdown
exit
end
write memory
```

---

## ✅ **Verify Configuration**

### From Switch (S1 or S2)

```plaintext
show ip interface brief
show running-config
```

### From PC1/PC2 (Command Prompt)

```plaintext
ping 192.168.1.253   ← (S1 IP)
ping 192.168.1.254   ← (S2 IP)
ping 192.168.1.2     ← (PC2 IP, from PC1)
```

---

Would you like this in a nicely formatted README.md file too?
