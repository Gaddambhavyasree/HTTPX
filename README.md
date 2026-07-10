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

📸 **Screenshot**

<img width="678" height="358" alt="Screenshot 2026-07-10 174653" src="https://github.com/user-attachments/assets/9c1b80a4-2e73-43d1-af13-f2801847b110" />


---

# 2️⃣ Display HTTP Status Code

### Command

```bash
httpx -l domains.txt -status-code
```

### Purpose

Displays the HTTP response status for every live host.

📸 **Screenshot**

<img width="626" height="361" alt="Screenshot 2026-07-10 174803" src="https://github.com/user-attachments/assets/e7b0570b-248c-4700-8e3c-7a236e2b137d" />


---

# 3️⃣ Retrieve Website Title

### Command

```bash
httpx -l domains.txt -title
```

### Purpose

Extracts the HTML `<title>` of each website.

📸 **Screenshot**

<img width="952" height="365" alt="Screenshot 2026-07-10 174900" src="https://github.com/user-attachments/assets/a8980d67-32cc-487b-a007-403bf7fe098a" />


---

# 4️⃣ Detect Web Technologies

### Command

```bash
httpx -l domains.txt -tech-detect
```

### Purpose

Identifies technologies and frameworks used by the target website.

📸 **Screenshot**

<img width="1536" height="390" alt="Screenshot 2026-07-10 174926" src="https://github.com/user-attachments/assets/35fd69a2-1e39-449f-ab2c-4bc4cdecfe9f" />


---

# 5️⃣ Display Server Information

### Command

```bash
httpx -l domains.txt -server
```

### Purpose

Displays the HTTP **Server** header returned by the web server.

📸 **Screenshot**

<img width="652" height="361" alt="Screenshot 2026-07-10 174947" src="https://github.com/user-attachments/assets/516f91f8-36d0-4a32-8439-37905c1f8f14" />

---

# 6️⃣ Resolve IP Address

### Command

```bash
httpx -l domains.txt -ip
```

### Purpose

Resolves the domain name to its corresponding IP address.

📸 **Screenshot**

<img width="678" height="372" alt="Screenshot 2026-07-10 175006" src="https://github.com/user-attachments/assets/0b509d7a-15e9-477b-bdea-7e2db84c3002" />


---

# 7️⃣ Display Content Length

### Command

```bash
httpx -l domains.txt -content-length
```

### Purpose

Displays the size of the HTTP response body in bytes.


📸 **Screenshot**

<img width="632" height="350" alt="Screenshot 2026-07-10 210625" src="https://github.com/user-attachments/assets/0f62ccb3-0f5d-4feb-a921-87cb5b261b8d" />


---
