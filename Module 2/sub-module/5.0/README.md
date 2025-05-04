Thought for a second


````markdown
## 2.5.1 Configuration Files (Config File ka Hisab)

Cisco device ke do main config files hote hain:

1. **running-config**  
   - **Kahan?** RAM (volatile memory)  
   - **Kya hai?** Jo bhi aap abhi kar rahe ho, sab usmein hota hai.  
   - **Command dekhne ke liye:**  
     ```bash
     Sw# show running-config
     ```  
   - **Note:** Power off ya reload se sab chala jaayega agar save na kiya ho.

2. **startup-config**  
   - **Kahan?** NVRAM (non-volatile)  
   - **Kya hai?** Save ki hui settings. Device reboot par ye load hoti hai.  
   - **Command dekhne ke liye:**  
     ```bash
     Sw# show startup-config
     ```

### 💾 Running → Startup me kaise save karein?

```bash
Sw# copy running-config startup-config
````

Ya

```bash
Sw# write memory
```

— Isse jo bhi aapne ab tak configure kiya, wo NVRAM me safe ho jayega.

---

## 2.5.2 Alter the Running Configuration (Running Config Ko Wapas Puraana Karna)

A. **Running config me galti ho gayi, save nahi kiya?**

1. **Commands hatao** ek-ek karke:

   ```bash
   Sw(config)# no <galat command>
   ```
2. **Ya reload kar do** (magar downtime hoga):

   ```bash
   Sw# reload
   ```

   * Prompt aayega “Save changes? \[yes/no]” → `no` ya `n` type karo, fir Enter.

B. **Galti startup-config me bhi save ho gayi?**

1. **Startup config erase karo:**

   ```bash
   Sw# erase startup-config
   ```

   * Confirmation maangega → Enter dabao.
2. **Phir reload karo:**

   ```bash
   Sw# reload
   ```

   → Device factory default settings ke saath dobara start ho jayega.

---

> 🔑 **Tip:** Running → Startup save karne ke baad hi power off/reset karo, warna sab chala jayega!

```

— Is section ko apne `README.md` me paste kar lo. Batao agar download-able file chahiye ho!
```







Great, I’ve reviewed the uploaded PDF titled **"2.5.5 Packet Tracer - Configure Initial Switch Settings"**. It looks like you're trying to understand how to perform the initial configuration of a switch using Cisco Packet Tracer. You mentioned that you've followed the steps, but you're still not getting the hostname and banner to appear as expected.

Here’s a checklist to help you troubleshoot and verify each step:

---

### ✅ Basic Checklist for Switch Initial Configuration

1. **Enter privileged EXEC mode**

   ```
   Switch> enable
   ```

2. **Enter global configuration mode**

   ```
   Switch# configure terminal
   ```

3. **Set the hostname**

   ```
   Switch(config)# hostname MySwitch
   ```

   * After this command, the prompt should change from `Switch(config)#` to `MySwitch(config)#`.

4. **Set the banner message**

   ```
   MySwitch(config)# banner motd #Unauthorized access is prohibited!#
   ```

   * Make sure you use **`#`** as the delimiter at both ends.

5. **Set a password for console access**

   ```
   MySwitch(config)# line console 0
   MySwitch(config-line)# password cisco
   MySwitch(config-line)# login
   MySwitch(config-line)# exit
   ```

6. **Set the enable password**

   ```
   MySwitch(config)# enable password class
   ```

7. **Save the configuration**

   ```
   MySwitch# copy running-config startup-config
   ```

---

### 🛠 Common Issues

* If your **hostname or banner doesn’t appear**:

  * You might be in the wrong mode (check for `Switch>` vs. `Switch#`).
  * You didn’t **save the config**; it resets when the session ends.
  * You’re in the wrong **switch console tab** in Packet Tracer.
  * You didn't use `login` under `line console 0` — without it, the password and banner won’t trigger.

---

Would you like me to generate a working demo script or provide a Packet Tracer `.pkt` file with the settings correctly configured?

