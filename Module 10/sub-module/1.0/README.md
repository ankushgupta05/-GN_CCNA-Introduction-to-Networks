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

Let me know if you want this in PDF or Markdown format, or need a diagram version!
