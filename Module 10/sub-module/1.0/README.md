Here is a **cleaned-up and structured version** of the **Basic Router Configuration Steps** from section 10.1.1 for better readability and understanding:

---

### 🔧 10.1.1 Basic Router Configuration Steps

The following tasks should be completed when configuring initial settings on a **Cisco router**:

---

#### **1. Configure the Device Name**

```plaintext
Router(config)# hostname <hostname>
```

* Replaces the default router name with a custom name.

---

#### **2. Secure Privileged EXEC Mode**

```plaintext
Router(config)# enable secret <password>
```

* Sets an encrypted password for privileged (enable) mode.

---

#### **3. Secure User EXEC Mode (Console Access)**

```plaintext
Router(config)# line console 0
Router(config-line)# password <password>
Router(config-line)# login
```

* Adds a password to console access and requires login.

---

#### **4. Secure Remote Access (Telnet/SSH)**

```plaintext
Router(config)# line vty 0 4
Router(config-line)# password <password>
Router(config-line)# login
Router(config-line)# transport input {ssh | telnet}
```

* Sets password and login for remote access.
* Choose between SSH or Telnet.

---

#### **5. Encrypt All Passwords**

```plaintext
Router(config-line)# exit
Router(config)# service password-encryption
```

* Encrypts passwords stored in the configuration file.

---

#### **6. Display Legal Notification (MOTD Banner)**

```plaintext
Router(config)# banner motd #Unauthorized access is prohibited#
```

* Message of the Day (MOTD) banner displays a legal warning.

> Replace `#` with any delimiter of your choice that does not appear in the message.

---

#### **7. Save the Configuration**

```plaintext
Router(config)# end
Router# copy running-config startup-config
```

* Saves current settings to NVRAM for persistent storage.

---
Here is a **structured summary** of section **10.1.2 – Basic Router Configuration Example** using the topology and configuration steps you provided.

---

## 🔧 10.1.2 Basic Router Configuration Example

This example demonstrates how to configure router **R1** in a simple network topology.

---

### 🖧 **Network Topology Overview**

```
PC1 ---- Switch ---- R1 ---- R2 ---- Switch ---- PC2
```

#### 🔌 **Key Addressing Information**

| Device/Interface    | IPv4 Address    | IPv6 Address           | Network                           |
| ------------------- | --------------- | ---------------------- | --------------------------------- |
| **PC1**             | 192.168.10.10   | 2001\:db8\:acad:10::10 | 192.168.10.0/24, acad:10::/64     |
| **R1 G0/0/0**       | 192.168.10.1    | 2001\:db8\:acad:10::1  | Same as PC1                       |
| **R1 G0/0/1**       | 209.165.200.225 | 2001\:db8\:feed:224::1 | 209.165.200.224/30, feed:224::/64 |
| **R2 G0/0/1**       | 209.165.200.226 | 2001\:db8\:feed:224::2 | Same as R1 G0/0/1                 |
| **R2 LAN (to PC2)** | 10.1.1.1        | 2001\:db8\:cafe::1     | 10.1.1.0/24, cafe::/64            |
| **PC2**             | 10.1.1.10       | 2001\:db8\:cafe::10    | Same as R2 LAN                    |

---

### 🛠️ **Step-by-Step Configuration on R1**

#### 1. **Enter Global Configuration Mode and Set Hostname**

```plaintext
Router> enable
Router# configure terminal
Router(config)# hostname R1
R1(config)#
```

> ✅ Prompt changes to reflect the hostname `R1`.

---

#### 2. **Secure Privileged EXEC Mode**

```plaintext
R1(config)# enable secret class
```

> ✅ Sets encrypted password `class` for privileged access.

---

#### 3. **Secure Console (User EXEC Mode)**

```plaintext
R1(config)# line console 0
R1(config-line)# password cisco
R1(config-line)# login
R1(config-line)# exit
```

> ✅ Password `cisco` required to access console.

---

#### 4. **Secure VTY Lines (Remote Access: Telnet/SSH)**

```plaintext
R1(config)# line vty 0 4
R1(config-line)# password cisco
R1(config-line)# login
R1(config-line)# transport input ssh telnet
R1(config-line)# exit
```

> ✅ Password `cisco` required for Telnet/SSH.
> ✅ Both Telnet and SSH access are enabled.

---

#### 5. **Encrypt All Plaintext Passwords**

```plaintext
R1(config)# service password-encryption
```

> ✅ Encrypts all passwords in configuration.

---

#### 6. **Add Legal Warning (MOTD Banner)**

```plaintext
R1(config)# banner motd #
***********************************************
WARNING: Unauthorized access is prohibited!
***********************************************
#
```

> ✅ Displays warning message upon login.

---

#### 7. **Save Configuration to NVRAM**

```plaintext
R1# copy running-config startup-config
Destination filename [startup-config]?
Building configuration...
[OK]
```

> ✅ Saves current settings so they persist after a reboot.

---

Let me know if you'd like the same format for **R2** or if you'd like this content in a **Markdown**, **PDF**, or **poster-style image** format.
