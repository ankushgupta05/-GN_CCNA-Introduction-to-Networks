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
