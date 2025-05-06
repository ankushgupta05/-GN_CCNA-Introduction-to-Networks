Here are the correct answers to **Questions 1 to 10**, formatted just like Question 13:

---

### **Question 1**

**An employee at a branch office is creating a quote for a customer. In order to do this, the employee needs to access confidential pricing information from internal servers at the Head Office. What type of network would the employee access?**

| Option | Answer               | Explanation |                                                                                            |
| ------ | -------------------- | ----------- | ------------------------------------------------------------------------------------------ |
| 🅐     | an extranet          | ❌ Incorrect | Extranets allow access to authorized external users, not internal branch employees.        |
| 🅑     | a local area network | ❌ Incorrect | A LAN is limited to a single location, not remote access.                                  |
| 🅒     | the Internet         | ❌ Incorrect | The Internet is public, not suitable for accessing confidential internal data.             |
| 🅓     | an intranet          | ✅ Correct   | Intranets are private networks used to securely share company information among employees. |

---

### **Question 2**

**Match each characteristic to its corresponding Internet connectivity type.**

| Characteristic                                          | Match               | Explanation                                                       |
| ------------------------------------------------------- | ------------------- | ----------------------------------------------------------------- |
| high bandwidth connection that runs over telephone line | B: DSL              | DSL uses existing telephone lines to deliver high-speed Internet. |
| uses coaxial cable as a medium                          | A: Cable            | Cable Internet uses coaxial cables commonly used for TV.          |
| typically has very low bandwidth                        | D: Dialup telephone | Dialup uses analog phone lines and is very slow.                  |
| not suited for heavily wooded areas                     | C: Satellite        | Satellite signals are disrupted by trees and weather.             |

---

### **Question 3**

**Which statement describes the use of powerline networking technology?**

| Option | Answer                                                                                        | Explanation |                                                                                     |
| ------ | --------------------------------------------------------------------------------------------- | ----------- | ----------------------------------------------------------------------------------- |
| 🅐     | New "smart" electrical cabling is used to extend an existing home LAN.                        | ❌ Incorrect | Powerline uses existing cabling, not new "smart" ones.                              |
| 🅑     | A home LAN is installed without the use of physical cabling.                                  | ❌ Incorrect | Powerline *does* use physical power cables.                                         |
| 🅒     | Wireless access points use powerline adapters to distribute data through the home LAN.        | ❌ Incorrect | Access points may use it, but it’s not the general definition.                      |
| 🅓     | A device connects to an existing home LAN using an adapter and an existing electrical outlet. | ✅ Correct   | Powerline networking transmits data over existing electrical wiring using adapters. |

---

### **Question 4**

**In the `show running-config` command, which part of the syntax is represented by `running-config`?**

| Option | Answer      | Explanation |                                                                      |
| ------ | ----------- | ----------- | -------------------------------------------------------------------- |
| 🅐     | a keyword   | ✅ Correct   | `running-config` is a predefined keyword used in the command syntax. |
| 🅑     | the command | ❌ Incorrect | The command is `show`.                                               |
| 🅒     | a prompt    | ❌ Incorrect | A prompt is the CLI symbol, like `Router>`.                          |
| 🅓     | a variable  | ❌ Incorrect | `running-config` is not user-defined or variable input.              |

---

### **Question 5**

**Which command or key combination allows a user to return to the previous level in the command hierarchy?**

| Option | Answer | Explanation |                                                                         |
| ------ | ------ | ----------- | ----------------------------------------------------------------------- |
| 🅐     | Ctrl-C | ❌ Incorrect | Ctrl-C breaks the current command/process.                              |
| 🅑     | Ctrl-Z | ❌ Incorrect | Ctrl-Z exits configuration mode and returns to privileged exec mode.    |
| 🅒     | Exit   | ✅ Correct   | `exit` is used to go back one level in the command hierarchy.           |
| 🅓     | End    | ❌ Incorrect | `end` returns directly to privileged exec mode, not the previous level. |

---

### **Question 6**

**How is SSH different from Telnet?**

| Option | Answer                                                                                                                                                        | Explanation |                                                           |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------- | --------------------------------------------------------- |
| 🅐     | SSH makes connections over the network, whereas Telnet is for out-of-band access.                                                                             | ❌ Incorrect | Both are used over networks.                              |
| 🅑     | SSH must be configured over an active network connection, whereas Telnet is used to connect to a device from a console connection.                            | ❌ Incorrect | Both can be used over network connections.                |
| 🅒     | SSH requires the use of the PuTTY terminal emulation program. Tera Term must be used to connect to devices through the use of Telnet.                         | ❌ Incorrect | Both tools can be used for either protocol.               |
| 🅓     | SSH provides security to remote sessions by encrypting messages and using user authentication. Telnet is considered insecure and sends messages in plaintext. | ✅ Correct   | SSH is secure, whereas Telnet transmits data unencrypted. |

---

### **Question 7**

**A network administrator enters the `service password-encryption` command into the configuration mode of a router. What does this command accomplish?**

| Option | Answer                                                                                                                          | Explanation |                                                                                   |
| ------ | ------------------------------------------------------------------------------------------------------------------------------- | ----------- | --------------------------------------------------------------------------------- |
| 🅐     | This command prevents someone from viewing the running configuration passwords.                                                 | ✅ Correct   | It encrypts passwords in the running-config so they're not visible in plain text. |
| 🅑     | This command provides an exclusive encrypted password for external service personnel who are required to do router maintenance. | ❌ Incorrect | No special external access is provided.                                           |
| 🅒     | This command enables a strong encryption algorithm for the enable secret password command.                                      | ❌ Incorrect | `enable secret` already uses stronger encryption by itself.                       |
| 🅓     | This command encrypts passwords as they are transmitted across serial WAN links.                                                | ❌ Incorrect | It only encrypts stored passwords, not transmissions.                             |
| 🅔     | This command automatically encrypts passwords in configuration files that are currently stored in NVRAM.                        | ❌ Incorrect | It affects currently running configuration; not stored NVRAM config directly.     |

---

### **Question 8**

**An administrator uses the `Ctrl-Shift-6` key combination on a switch after issuing the `ping` command. What is the purpose of using these keystrokes?**

| Option | Answer                                    | Explanation |                                                                     |
| ------ | ----------------------------------------- | ----------- | ------------------------------------------------------------------- |
| 🅐     | to interrupt the ping process             | ✅ Correct   | `Ctrl-Shift-6` stops ongoing processes like `ping` or `traceroute`. |
| 🅑     | to exit to a different configuration mode | ❌ Incorrect | It doesn't change modes.                                            |
| 🅒     | to allow the user to complete the command | ❌ Incorrect | This combination doesn't help in command completion.                |
| 🅓     | to restart the ping process               | ❌ Incorrect | It actually stops it, not restarts.                                 |

---

### **Question 9**

**After making configuration changes on a Cisco switch, a network administrator issues a `copy running-config startup-config` command. What is the result of issuing this command?**

| Option | Answer                                                                                     | Explanation |                                                                  |
| ------ | ------------------------------------------------------------------------------------------ | ----------- | ---------------------------------------------------------------- |
| 🅐     | The configuration changes will be removed and the original configuration will be restored. | ❌ Incorrect | That would require `reload` or replacing startup-config.         |
| 🅑     | The current IOS file will be replaced with the newly configured file.                      | ❌ Incorrect | IOS is separate from the configuration.                          |
| 🅒     | The new configuration will be loaded if the switch is restarted.                           | ✅ Correct   | This saves the running config to NVRAM so it loads after reboot. |
| 🅓     | The new configuration will be stored in flash memory.                                      | ❌ Incorrect | Flash memory stores the IOS, not the config by default.          |

---

### **Question 10**

**What are two characteristics of RAM on a Cisco device? (Choose two.)**

| Option | Answer                                                                     | Explanation |                                                    |
| ------ | -------------------------------------------------------------------------- | ----------- | -------------------------------------------------- |
| ☑      | The configuration that is actively running on the device is stored in RAM. | ✅ Correct   | RAM holds the running-config.                      |
| ☐      | RAM provides nonvolatile storage.                                          | ❌ Incorrect | RAM is volatile and data is lost when powered off. |
| ☐      | RAM is able to store multiple versions of IOS and configuration files.     | ❌ Incorrect | Flash stores IOS versions, not RAM.                |
| ☑      | The contents of RAM are lost during a power cycle.                         | ✅ Correct   | RAM is volatile memory.                            |
| ☐      | RAM is a component in Cisco switches but not in Cisco routers.             | ❌ Incorrect | Both switches and routers use RAM.                 |

---

Would you like me to continue with Questions 11–20 in the same format?





Here’s the solution in the same format for **Questions 11 to 16**:

---

### **Question 11**

**Which two host names follow the guidelines for naming conventions on Cisco IOS devices? (Choose two.)**

| Option            | Answer      | Explanation                                                         |
| ----------------- | ----------- | ------------------------------------------------------------------- |
| ✅ SwBranch799     | ✅ Correct   | Uses only letters and numbers; no spaces or special characters.     |
| ⛔ Floor(15)       | ❌ Incorrect | Contains parentheses, which are not allowed in Cisco IOS hostnames. |
| ⛔ HO Floor 17     | ❌ Incorrect | Contains spaces, which are not valid in hostnames.                  |
| ✅ RM-3-Switch-2A4 | ✅ Correct   | Dashes are allowed, and the name is appropriately formatted.        |
| ⛔ Branch2!        | ❌ Incorrect | Contains an exclamation mark, which is not allowed in hostnames.    |

---

### **Question 12**

**What function does pressing the Tab key have when entering a command in IOS?**

| Option                                                                | Answer      | Explanation                                |
| --------------------------------------------------------------------- | ----------- | ------------------------------------------ |
| 🅐 It aborts the current command and returns to configuration mode.   | ❌ Incorrect | Ctrl+C is used to abort commands.          |
| 🅑 It completes the remainder of a partially typed word in a command. | ✅ Correct   | The Tab key auto-completes command words.  |
| 🅒 It exits configuration mode and returns to user EXEC mode.         | ❌ Incorrect | Use `end` or `Ctrl+Z` to exit config mode. |
| 🅓 It moves the cursor to the beginning of the next line.             | ❌ Incorrect | Enter key does this, not Tab.              |

---

### **Question 13**

**What command will prevent all unencrypted passwords from displaying in plain text in a configuration file?**

| Option                                         | Answer      | Explanation                                                     |
| ---------------------------------------------- | ----------- | --------------------------------------------------------------- |
| 🅐 (config)# enable secret Secret\_Password    | ❌ Incorrect | This encrypts only the enable secret password.                  |
| 🅑 (config)# enable password secret            | ❌ Incorrect | Invalid command syntax.                                         |
| 🅒 (config-line)# password secret              | ❌ Incorrect | Invalid syntax and context for global encryption.               |
| 🅓 (config)# enable secret Encrypted\_Password | ❌ Incorrect | This sets an encrypted password but doesn't encrypt all others. |
| 🅔 (config)# service password-encryption       | ✅ Correct   | Encrypts all plaintext passwords in the config file.            |

---

### **Question 14**

**Passwords can be used to restrict access to all or parts of the Cisco IOS. Select the modes and interfaces that can be protected with passwords. (Choose three.)**

| Option                      | Answer      | Explanation                                                 |
| --------------------------- | ----------- | ----------------------------------------------------------- |
| ⛔ Boot IOS mode             | ❌ Incorrect | Not a password-protected mode.                              |
| ⛔ Ethernet interface        | ❌ Incorrect | Cannot be password protected directly.                      |
| ⛔ Router configuration mode | ❌ Incorrect | Access to this mode is protected indirectly via EXEC mode.  |
| ✅ Console interface         | ✅ Correct   | You can set a console line password using `line console 0`. |
| ✅ VTY interface             | ✅ Correct   | VTY lines (Telnet/SSH) can be password protected.           |
| ✅ Privileged EXEC mode      | ✅ Correct   | Protected using `enable password` or `enable secret`.       |

---

### **Question 15**

**What command is used to verify the condition of the switch interfaces, including the status of the interfaces and a configured IP address?**

| Option                     | Answer      | Explanation                                                |
| -------------------------- | ----------- | ---------------------------------------------------------- |
| 🅐 show ip interface brief | ✅ Correct   | Displays the summary of interface status and IP addresses. |
| 🅑 ipconfig                | ❌ Incorrect | This is a Windows command, not a Cisco IOS command.        |
| 🅒 ping                    | ❌ Incorrect | Used to test connectivity, not view interface details.     |
| 🅓 traceroute              | ❌ Incorrect | Shows the route packets take, not interface info.          |

---

### **Question 16**

**Refer to the exhibit. A network administrator is configuring access control to switch SW1. If the administrator uses a console connection to connect to the switch, which password is needed to access user EXEC mode?**

| Option       | Answer      | Explanation                                                                                              |
| ------------ | ----------- | -------------------------------------------------------------------------------------------------------- |
| 🅐 letmein   | ❌ Incorrect | This is for `enable password`, used for privileged EXEC mode.                                            |
| 🅑 linevtyin | ❌ Incorrect | This is for VTY (remote) access, not console access.                                                     |
| 🅒 secretin  | ❌ Incorrect | This is for `enable secret`, used for privileged EXEC mode.                                              |
| 🅓 lineconin | ✅ Correct   | This password is configured under `line console 0` and is required to access user EXEC mode via console. |

---

Would you like me to continue with Question 17 to 20 in this same table format?
