# 🌐 HTTPX - HTTP Probing & Web Reconnaissance

A hands-on lab demonstrating the basic usage of **ProjectDiscovery HTTPX**, a fast and reliable HTTP probing tool used during the reconnaissance phase of web application penetration testing.

> **Disclaimer:** This project was performed in my own lab environment for educational purposes only. Do **not** use these techniques against systems you do not own or have explicit permission to test. I am not responsible for any misuse of this information.

---

## 📖 Overview

HTTPX is a high-performance HTTP probing tool that helps security professionals quickly identify live web applications and collect useful information about them.

This repository demonstrates how to use HTTPX to gather information such as:

- Live hosts
- HTTP status codes
- Website titles
- Web server information
- Technology detection
- IP addresses
- Content length

---

## 📂 Test Input

**domains.txt**

```text
google.com
facebook.com
idontexist123.com
```

---

# 1️⃣ Check Live Hosts

### Command

```bash
httpx -l domains.txt
```

### Purpose

Checks each domain and prints only the reachable websites.

### Example Output

```text
https://google.com
https://facebook.com
```

📸 **Screenshot**

_Add your screenshot here._

---

# 2️⃣ Display HTTP Status Code

### Command

```bash
httpx -l domains.txt -status-code
```

### Purpose

Displays the HTTP response status for every live host.

### Example Output

```text
https://google.com [200]
https://facebook.com [200]
```

### Common Status Codes

| Code | Meaning |
|------|---------|
| 200 | Success |
| 301 | Permanent Redirect |
| 302 | Temporary Redirect |
| 403 | Forbidden |
| 404 | Not Found |
| 500 | Internal Server Error |

📸 **Screenshot**

_Add your screenshot here._

---

# 3️⃣ Retrieve Website Title

### Command

```bash
httpx -l domains.txt -title
```

### Purpose

Extracts the HTML `<title>` of each website.

### Example Output

```text
https://google.com [Google]
https://facebook.com [Facebook – log in or sign up]
```

📸 **Screenshot**

_Add your screenshot here._

---

# 4️⃣ Detect Web Technologies

### Command

```bash
httpx -l domains.txt -tech-detect
```

### Purpose

Identifies technologies and frameworks used by the target website.

### Example Output

```text
https://google.com [Google Frontend]
https://facebook.com [React]
```

📸 **Screenshot**

_Add your screenshot here._

---

# 5️⃣ Display Server Information

### Command

```bash
httpx -l domains.txt -server
```

### Purpose

Displays the HTTP **Server** header returned by the web server.

### Example Output

```text
https://google.com [gws]
https://facebook.com [proxygen]
```

📸 **Screenshot**

_Add your screenshot here._

---

# 6️⃣ Resolve IP Address

### Command

```bash
httpx -l domains.txt -ip
```

### Purpose

Resolves the domain name to its corresponding IP address.

### Example Output

```text
https://google.com [142.250.xxx.xxx]
https://facebook.com [157.240.xxx.xxx]
```

📸 **Screenshot**

_Add your screenshot here._

---

# 7️⃣ Display Content Length

### Command

```bash
httpx -l domains.txt -content-length
```

### Purpose

Displays the size of the HTTP response body in bytes.

### Example Output

```text
https://google.com [18342]
https://facebook.com [92761]
```

📸 **Screenshot**

_Add your screenshot here._

---
