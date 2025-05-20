Here are the answers with explanations for your DNS questions:

---

### Question 1

**Which of the following DNS record types is used to resolve IPv6 addresses?**

* ⭕ A
* ⭕ NS
* ✅ **AAAA**
* ⭕ MX

*Explanation:*
The **AAAA** record maps a hostname to its IPv6 address. The **A** record is for IPv4 addresses.

---

### Question 2

**True or false? A DNS server that receives a request for a name resolution that is not within its DNS zone will send a failure message to the requesting client.**

* ⭕ True
* ✅ **False**

*Explanation:*
If a DNS server cannot resolve a name because it’s outside its zone, it typically forwards the query to another DNS server (recursive or forwarding), not immediately a failure.

---

### Question 3

**Which of the following is displayed by the nslookup utility?**

* ✅ **The configured default DNS server**
* ⭕ The IP address of the end device
* ⭕ All cached DNS entries

*Explanation:*
`nslookup` shows the DNS server it is querying by default and the resolution results. It does not list all cached entries.

---

### Question 4

**Which of the following DNS resource record types resolves authoritative name servers?**

* ✅ **NS**
* ⭕ A
* ⭕ MX
* ⭕ AAAA

*Explanation:*
The **NS** (Name Server) record specifies authoritative name servers for a DNS zone.

---

Let me know if you want more details or help!
