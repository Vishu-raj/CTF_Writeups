# 🚩 MYTHX CTF - Writeups & Walkthroughs 

![Visitors](https://img.shields.io/badge/visitors-1006-3178c6?style=flat-square)

![Repo Size](https://img.shields.io/badge/REPO_SIZE-14.2_MiB-555555?style=flat-square) ![Last Commit](https://img.shields.io/badge/LAST_COMMIT-MAY-97ca00?style=flat-square) [![LinkedIn](https://img.shields.io/badge/LINKEDIN-CONNECT-0077b5?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/vishu-raj-49ab332b9/) [![GitHub](https://img.shields.io/badge/GITHUB-VISHU__RAJ-181717?style=flat-square&logo=github)](https://github.com/Vishu-raj) ![Discord](https://img.shields.io/badge/DISCORD-VISHU#0000-5865F2?style=flat-square&logo=discord)

---

Welcome!
This repository is a collection of my CTF (Capture The Flag) challenge write-ups, where I document the process, tools, and techniques I used to solve different security puzzles during the **Hack!tUp CTF**.

The goal of this repo is to both **share knowledge** and **showcase my skills** in web exploitation, vulnerability assessment, and offensive security methodologies.

---

## 📜 Official Certificate
<p align="center">
  <img src="Certificate/Vishu_Raj_Certificate.png" alt="Hack!tUp CTF Certificate" width="800"/>
</p>

---

## 🧠 Challenge Writeups & Methodology

### 1. Web Exploitation: Authentication Bypass & IDOR
<p align="center">
  <img src="Screenshots/Screenshot 2026-04-25 193713.png" width="750"/>
</p>

**Category:** Web Security
**Tools Utilized:** Burp Suite, OWASP ZAP
**Vulnerability Identified:** [e.g., Insecure Direct Object Reference (IDOR) / Broken Access Control]

**Exploitation Steps:**
1. **Reconnaissance:** [Explain how you initially mapped the target application and identified the login/authentication mechanism.]
2. **Interception:** [Detail how you routed traffic through Burp Suite to analyze the request headers and identify the vulnerable parameter.]
3. **Manipulation:** [Describe the exact payload or parameter change (e.g., changing `user_id=1` to `user_id=0`) that allowed you to bypass restrictions.]
4. **Impact:** [Explain how this led to capturing the flag.]

### 2. Injection Flaws
<p align="center">
  <img src="Screenshots/Screenshot 2026-04-25 193726.png" width="750"/>
</p>

**Category:** Web Security
**Tools Utilized:** SQLMap, Manual Testing
**Vulnerability Identified:** [e.g., SQL Injection (SQLi) / Cross-Site Scripting (XSS)]

**Exploitation Steps:**
1. **Input Validation Testing:** [Explain how you tested the input fields with special characters (like `'` or `<script>`) to trigger an error or reflection.]
2. **Payload Crafting:** [Provide the exact payload used to exploit the flaw.]
3. **Execution & Exfiltration:** [Detail how the successful execution resulted in database dumping or retrieving the hidden flag.]

### 3. Traffic Analysis & Enumeration
<p align="center">
  <img src="Screenshots/Screenshot 2026-04-25 203510.png" width="750"/>
</p>

**Category:** Forensics / Reconnaissance
**Tools Utilized:** Gobuster, Wireshark

**Analysis Steps:**
1. **Directory Brute-forcing:** [Explain how you used Gobuster to find hidden directories or files on the target server.]
2. **Traffic Analysis:** [Describe the process of analyzing the provided traffic or server responses to identify anomalies.]
3. **Resolution:** [Show how compiling this data led to the flag.]

---

## 📸 Exploitation Evidence & Challenge Gallery

<details>
  <summary><b>Click to expand full screenshot gallery</b></summary>
  
  <br>
  <p align="center">
    <img src="Screenshots/Screenshot 2026-04-25 203525.png" width="400"/>
    <img src="Screenshots/Screenshot 2026-04-25 204612.png" width="400"/>
  </p>
  <p align="center">
    <img src="Screenshots/Screenshot 2026-04-25 211901.png" width="400"/>
    <img src="Screenshots/Screenshot 2026-04-25 220649.png" width="400"/>
  </p>
  <p align="center">
    <img src="Screenshots/Screenshot 2026-04-25 220727.png" width="400"/>
    <img src="Screenshots/Screenshot 2026-04-25 220855.png" width="400"/>
  </p>
  <p align="center">
    <img src="Screenshots/Screenshot 2026-04-25 220940.png" width="400"/>
    <img src="Screenshots/Screenshot 2026-04-25 220954.png" width="400"/>
  </p>
  <p align="center">
    <img src="Screenshots/Screenshot 2026-04-25 222146.png" width="400"/>
    <img src="Screenshots/Screenshot 2026-04-25 222838.png" width="400"/>
  </p>
  <p align="center">
    <img src="Screenshots/Screenshot 2026-04-28 010910.png" width="400"/>
    <img src="Screenshots/Screenshot 2026-04-28 010927.png" width="400"/>
  </p>
  <p align="center">
    <img src="WhatsApp Image 2026-04-25 at 9.07.44 PM.jpeg" width="800"/>
  </p>
</details>

---

## 👨‍💻 About the Author
**Vishu_Raj**
A cybersecurity enthusiast specializing in ethical hacking and vulnerability assessments. Currently applying offensive security skills in a full professional internship, with a strong focus on bug bounty hunting, manual web exploitation, and mastering industry-standard tools.
