# 🩸 Heartbleed Bug Demonstration (CVE-2014-0160)

This is a cybersecurity case study I completed during my studies at Wintec, where I safely demonstrated how the infamous Heartbleed bug in OpenSSL can be exploited in a controlled virtual environment.

> 🏆 This project was ranked one of the best across three classes by the lecturer. Very proud of this.

---

## 🧠 What is Heartbleed?

Heartbleed is a serious vulnerability in OpenSSL's implementation of the TLS/DTLS heartbeat extension. It allows an attacker to read sensitive memory contents (e.g., credentials) from affected servers without authentication.

- **CVE ID:** CVE-2014-0160
- **Impact:** Confidential data leak (unencrypted memory content)
- **Status:** Patched in OpenSSL v1.0.1g

---

## 🔬 What I Did

- Built a **safe lab environment** using Docker and Ubuntu
- Deployed a **vulnerable web server** with OpenSSL 1.0.1f
- Sent a malformed heartbeat request to simulate the memory leak
- Successfully extracted a **username and password** I had submitted into the test site
- Operated completely **offline**, ensuring ethical use

---

## 📷 Demo Screenshots

![Lab Setup](screenshots/lab_setup.png)
*My offline Docker-based Ubuntu setup*

![Memory Leak](screenshots/memory_leak.png)
*Extracted memory snippet showing the login credentials*

---

## 🛡️ How to Protect Against It

- Upgrade OpenSSL to version 1.0.1g or newer
- Use intrusion detection tools (e.g., Snort) to detect Heartbeat anomalies
- Reissue SSL certificates after patching
- Practice regular vulnerability scanning

---

## ⚙️ Tools & Technologies

- Docker
- Ubuntu (Server)
- OpenSSL 1.0.1f
- Python + Bash scripting (for testing requests)

