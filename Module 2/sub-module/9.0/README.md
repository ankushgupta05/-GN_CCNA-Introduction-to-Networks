## NOTE :- 8 number ka question and answer wrong hai

# module 2  final Quize

Here are the answers to the *2.9.4 Module Quiz - Basic Switch and End Device Configuration* in the required format:

---

### Q1: Which statement is true about the running configuration file in a Cisco IOS device?

| Option | Answer                                                              | Explanation                                                               |
| ------ | ------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| 🅐     | ✅ It affects the operation of the device immediately when modified. | ✅ Correct – Changes to the running config take effect immediately.        |
| 🅑     | ❌ It is stored in NVRAM.                                            | ❌ Incorrect – That is the startup config.                                 |
| 🅒     | ❌ It should be deleted using the erase running-config command.      | ❌ Incorrect – This command does not exist; you can clear config manually. |
| 🅓     | ❌ It is automatically saved when the router reboots.                | ❌ Incorrect – Running config is lost unless saved manually.               |

---
---

### ✅ **Corrected Q2: Which two statements are true regarding the user EXEC mode?**

| Option | Answer                                                                      | Explanation                                                              |
| ------ | --------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| 🅐     | ❌ All router commands are available.                                        | ❌ Incorrect – Only a subset of basic commands is available.              |
| 🅑     | ❌ Global configuration mode can be accessed by entering the enable command. | ❌ Incorrect – `enable` leads to privileged EXEC mode, not global config. |
| 🅒     | ✅ The device prompt for this mode ends with the '>' symbol.                 | ✅ Correct – ‘>’ indicates user EXEC mode.                                |
| 🅓     | ❌ Interfaces and routing protocols can be configured.                       | ❌ Incorrect – Configuration is not possible in user EXEC mode.           |
| 🅔     | ✅ Only some aspects of the router configuration can be viewed.              | ✅ Correct – You can view basic info but not all configuration.           |

---

### Q3: Which type of access is secured on a Cisco router or switch with the enable secret command?

| Option | Answer             | Explanation                                                          |
| ------ | ------------------ | -------------------------------------------------------------------- |
| 🅐     | ❌ Virtual terminal | ❌ Incorrect – That’s secured with `line vty` passwords.              |
| 🅑     | ✅ Privileged EXEC  | ✅ Correct – `enable secret` protects access to privileged EXEC mode. |
| 🅒     | ❌ AUX port         | ❌ Incorrect – AUX is secured via `line aux`.                         |
| 🅓     | ❌ Console line     | ❌ Incorrect – Console is secured with `line console` password.       |

---

### Q4: What is the default SVI on a Cisco switch?

| Option | Answer    | Explanation                                                         |
| ------ | --------- | ------------------------------------------------------------------- |
| 🅐     | ✅ VLAN1   | ✅ Correct – VLAN 1 is the default SVI (Switched Virtual Interface). |
| 🅑     | ❌ VLAN99  | ❌ Incorrect – Not default, often used by admins.                    |
| 🅒     | ❌ VLAN100 | ❌ Incorrect – Custom, not default.                                  |
| 🅓     | ❌ VLAN999 | ❌ Incorrect – Typically unused or reserved.                         |

---

### Q5: When a hostname is configured through the Cisco CLI, which three naming conventions are part of the guidelines?

| Option | Answer                                                        | Explanation                                                 |
| ------ | ------------------------------------------------------------- | ----------------------------------------------------------- |
| 🅐     | ✅ The hostname should be fewer than 64 characters in length   | ✅ Correct – Cisco recommends fewer than 64 characters.      |
| 🅑     | ❌ The hostname should be written in all lower case characters | ❌ Incorrect – Case doesn’t matter.                          |
| 🅒     | ✅ The hostname should contain no spaces                       | ✅ Correct – Spaces are not allowed.                         |
| 🅓     | ❌ The hostname should end with a special character            | ❌ Incorrect – Special characters are discouraged.           |
| 🅔     | ✅ The hostname should begin with a letter                     | ✅ Correct – It should start with a letter per naming rules. |

---

### Q6: What is the function of the shell in an OS?

| Option | Answer                                                          | Explanation                                                              |
| ------ | --------------------------------------------------------------- | ------------------------------------------------------------------------ |
| 🅐     | ❌ It interacts with the device hardware.                        | ❌ Incorrect – That’s the kernel’s job.                                   |
| 🅑     | ✅ It interfaces between the users and the kernel.               | ✅ Correct – The shell takes user commands and passes them to the kernel. |
| 🅒     | ❌ It provides dedicated firewall services.                      | ❌ Incorrect – That’s a function of firewall software, not the shell.     |
| 🅓     | ❌ It provides the intrusion protection services for the device. | ❌ Incorrect – That’s handled by specialized IDS/IPS software.            |

---

### Q7: A router with a valid operating system contains a configuration file stored in NVRAM. The configuration file has an enable secret password but no console password. When the router boots up, which mode will display?

| Option | Answer                      | Explanation                                                             |
| ------ | --------------------------- | ----------------------------------------------------------------------- |
| 🅐     | ❌ Global configuration mode | ❌ Incorrect – This requires user interaction.                           |
| 🅑     | ❌ Setup mode                | ❌ Incorrect – Only enters setup if there’s no startup config.           |
| 🅒     | ❌ Privileged EXEC mode      | ❌ Incorrect – You must type `enable` to access it.                      |
| 🅓     | ✅ User EXEC mode            | ✅ Correct – Router boots into user EXEC if console password is not set. |

---

### Q8: An administrator has just changed the IP address of an interface on an IOS device. What else must be done in order to apply those changes to the device?

| Option | Answer                                                                                 | Explanation                                                  |
| ------ | -------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| 🅐     | ✅ Copy the running configuration to the startup configuration file.                    | ✅ Correct – This ensures changes are preserved after reboot. |
| 🅑     | ❌ Copy the information in the startup configuration file to the running configuration. | ❌ Incorrect – That would overwrite the changes.              |
| 🅒     | ❌ Reload the device and type yes when prompted to save the configuration.              | ❌ Incorrect – Manual save is preferred.                      |
| 🅓     | ❌ Nothing must be done.                                                                | ❌ Incorrect – Changes are lost after reboot unless saved.    |

---

### Q9: Which memory location on a Cisco router or switch will lose all content when the device is restarted?

| Option | Answer  | Explanation                                           |
| ------ | ------- | ----------------------------------------------------- |
| 🅐     | ❌ ROM   | ❌ Incorrect – ROM contents are permanent.             |
| 🅑     | ❌ Flash | ❌ Incorrect – Flash is non-volatile.                  |
| 🅒     | ❌ NVRAM | ❌ Incorrect – NVRAM retains data after reboot.        |
| 🅓     | ✅ RAM   | ✅ Correct – RAM is volatile and is cleared on reboot. |

---

### Q10: Why would a technician enter the command `copy startup-config running-config`?

| Option | Answer                                                          | Explanation                                                     |
| ------ | --------------------------------------------------------------- | --------------------------------------------------------------- |
| 🅐     | ❌ To remove all configurations from the switch                  | ❌ Incorrect – That’s not what this command does.                |
| 🅑     | ❌ To save an active configuration to NVRAM                      | ❌ Incorrect – That’s `copy running-config startup-config`.      |
| 🅒     | ✅ To copy an existing configuration into RAM                    | ✅ Correct – It loads the startup config into the active memory. |
| 🅓     | ❌ To make a changed configuration the new startup configuration | ❌ Incorrect – That would require the reverse command.           |

---

### Q11: Which functionality is provided by DHCP?

| Option | Answer                                               | Explanation                                       |
| ------ | ---------------------------------------------------- | ------------------------------------------------- |
| 🅐     | ✅ Automatic assignment of an IP address to each host | ✅ Correct – DHCP automates IP address assignment. |
| 🅑     | ❌ Remote switch management                           | ❌ Incorrect – Not a DHCP function.                |
| 🅒     | ❌ Translation of IP addresses to domain names        | ❌ Incorrect – That’s DNS.                         |
| 🅓     | ❌ End-to-end connectivity test                       | ❌ Incorrect – That’s done by ping/traceroute.     |

---

### Q12: Which two functions are provided to users by the context-sensitive help feature of the Cisco IOS CLI?

| Option | Answer                                                                                   | Explanation                                               |
| ------ | ---------------------------------------------------------------------------------------- | --------------------------------------------------------- |
| 🅐     | ❌ Providing an error message when a wrong command is submitted                           | ❌ Incorrect – Not the main function.                      |
| 🅑     | ✅ Displaying a list of all available commands within the current mode                    | ✅ Correct – It lists valid commands.                      |
| 🅒     | ✅ Determining which option, keyword, or argument is available for the entered command    | ✅ Correct – Helps with command syntax.                    |
| 🅓     | ❌ Allowing the user to complete the remainder of an abbreviated command with the TAB key | ❌ Incorrect – Cisco CLI doesn’t use TAB for autocomplete. |
| 🅔     | ❌ Selecting the best command to accomplish a task                                        | ❌ Incorrect – That’s up to the user.                      |

---

### Q13: Which memory location on a Cisco router or switch stores the startup configuration file?

| Option | Answer  | Explanation                                    |
| ------ | ------- | ---------------------------------------------- |
| 🅐     | ❌ RAM   | ❌ Incorrect – That’s for running-config.       |
| 🅑     | ❌ ROM   | ❌ Incorrect – ROM holds bootstrap and POST.    |
| 🅒     | ✅ NVRAM | ✅ Correct – Startup config is stored in NVRAM. |
| 🅓     | ❌ Flash | ❌ Incorrect – Flash holds IOS image.           |

---

### Q14: To what subnet does the IP address 10.1.100.50 belong if a subnet mask of 255.255.0.0 is used?

| Option | Answer        | Explanation                                            |
| ------ | ------------- | ------------------------------------------------------ |
| 🅐     | ✅ 10.1.0.0    | ✅ Correct – 255.255.0.0 mask gives subnet of 10.1.0.0. |
| 🅑     | ❌ 10.0.0.0    | ❌ Incorrect – That would be true for 255.0.0.0.        |
| 🅒     | ❌ 10.1.100.32 | ❌ Incorrect – That would require a /27 or /28 mask.    |
| 🅓     | ❌ 10.1.100.0  | ❌ Incorrect – That would be true for /24 mask.         |

---

Let me know if you’d like this in a downloadable `.md` file or formatted table.
