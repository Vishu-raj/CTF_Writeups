# 🚀 MythX: An Endgame Protocol - CTF Writeups

![Category](https://img.shields.io/badge/Category-Cybersecurity%20CTF-blue?style=flat-square)
![Level](https://img.shields.io/badge/Level-National-success?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-CTF7-orange?style=flat-square)

## 📋 Event Overview
This repository contains my detailed writeups and methodologies for the challenges I solved during **MythX: An Endgame Protocol**. This was an intense, National-Level Cybersecurity Capture The Flag (CTF) competition hosted by KIET Deemed-to-be University on the CTF7 platform.

The objective of this repository is to document my step-by-step approach to identifying, exploiting, and securing vulnerabilities found within the competition environments.

---

## 🛠️ Arsenal & Methodology
To tackle the challenges in this CTF, my workflow heavily relied on manual enumeration and targeted exploitation using the following toolkit:
* **Operating System:** Kali Linux
* **Web Proxy & Manipulation:** Burp Suite, OWASP ZAP
* **Automated Exploitation:** SQLMap

---

## 🚩 Challenge Writeups

### Challenge: [Insert Challenge Name]
**Category:** [e.g., Web Exploitation] | **Points:** [e.g., 100]

#### 1. Reconnaissance
The challenge provided a target URL. Initial interaction with the web application revealed a standard user portal. My first step was to map the application's attack surface using Burp Suite to intercept and analyze the HTTP requests.

> **Screenshot: Initial Request Interception**
> *Replace this text with your actual screenshot from the event*
> ![Initial Intercept](Screenshots/Screenshot_Name_1.png)

#### 2. Vulnerability Discovery
While testing the application's input fields, I noticed abnormal behavior in how the server handled specific parameters. By manipulating the request, I identified a vulnerability [Describe vulnerability, e.g., an IDOR or SQLi]. 

> **Screenshot: Identifying the Vulnerability**
> *Replace this text with your actual screenshot from the event*
> ![Vulnerability Proof](Screenshots/Screenshot_Name_2.png)

#### 3. Exploitation & Flag Capture
I crafted a targeted payload to exploit the identified weakness. [Explain the exact payload or tool command used, e.g., routing the request through SQLMap to dump the schema]. The successful execution granted unauthorized access, allowing me to retrieve the final flag.

> **Screenshot: Successful Exploitation & Flag**
> *Replace this text with your actual screenshot from the event*
> ![Flag Captured](Screenshots/Screenshot_Name_3.png)

#### 🛡️ Mitigation Advice
To patch this vulnerability, the developers should:
1. Implement strict server-side input validation.
2. [Add specific fix, e.g., Use parameterized queries to prevent SQL injection or enforce strict access control checks on every API request].

---

## 👨‍💻 Author

**Vishu_Raj**
*Cybersecurity Intern @ Codec Technologies | Student at DIATM*
* **GitHub:** [Vishu_Raj](https://github.com/Vishu_Raj)
* **Bugcrowd:** [Vishu_Raj](https://bugcrowd.com/Vishu_Raj)
