Based on the content you shared from **12.2.1 to 12.2.4**, here is a summary of the **IPv6 address formatting rules** along with the solution for the **Check Your Understanding** example.

---

### ✅ **IPv6 Addressing Summary:**

#### 📌 **1. Preferred Format**

* IPv6 addresses are 128 bits long.
* Written as **8 hextets** separated by colons (`:`), each hextet is 4 hexadecimal digits.
* Example:
  `2001:0db8:0000:1111:0000:0000:0000:0200`

---

#### 📌 **2. Rule 1 - Omit Leading Zeros**

* Remove **leading** zeros **only** in each hextet.
* Example:

  * `01ab` → `1ab`
  * `00ab` → `ab`
  * `0001` → `1`

---

#### 📌 **3. Rule 2 - Double Colon (`::`)**

* Use `::` to replace **one** contiguous block of `0000` hextets.
* Can only be used **once per address**.
* Example:

  * `2001:0db8:0000:0000:0000:0000:abcd:1234`
    → `2001:db8::abcd:1234`

---

### ✅ **Check Your Understanding Example:**

Given hextets:

```
fe80
0
0
0
0
0
101
1111
```

#### 🔹 **Step 1 – Combine the hextets:**

```
fe80:0000:0000:0000:0000:0000:0101:1111
```

#### 🔹 **Step 2 – Omit leading zeros:**

```
fe80:0:0:0:0:0:101:1111
```

#### 🔹 **Step 3 – Use double colon for longest string of 0s:**

```
fe80::101:1111
```

✅ **Final Compressed IPv6 Address:**
`fe80::101:1111`

---

Let me know if you want practice problems or a quiz on IPv6 compression!
