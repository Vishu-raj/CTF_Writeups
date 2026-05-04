# 🏆 MythX: An Endgame Protocol CTF - Writeups

**Author:** Vishu Raj  
**Team:** Trojan_Titans  
**Institution:** Durgapur Institute of Advanced Technology and Management (DIATM)  

Welcome to my detailed writeups and methodology documentation for **MythX: An Endgame Protocol**, a National-Level Cybersecurity Capture The Flag (CTF) championship organized by the KIET Group of Institutions. 

## 🛡️ Event Overview
* **Event:** MythX: Cybersecurity Summit and Innovation Challenge
* **Platform:** CTF7
* **Format:** Jeopardy-Style CTF
* **Date:** March 28 - March 29, 2026
* **Total Players:** 378 | **Total Challenges:** 51

MythX is a high-intensity simulation designed to test exploitation and adaptation under real-world conditions, featuring industry-inspired challenges across multiple cybersecurity domains.

---

## 📜 Certificate of Participation

![Vishu Raj - Certificate of Participation](Certificate/Vishu_Raj_Certificate.png)

---

## 💻 Challenge Writeups

### 1. [Web] Homegrown Authentication System
* **Points:** 300
* **Difficulty:** Medium
* **Author:** Shubham Gabhale

#### Challenge Description
The challenge introduced a custom authentication system for the CTF7 staff portal. It utilized signed cookies instead of standard JWTs, granting guest access by default while reserving the admin panel for senior staff only.

![Challenge Description](Screenshots/Screenshot_2026-05-02_042718.png)

#### Methodology & Exploitation

**Step 1: Traffic Interception & Source Code Review**
I began by proxying my web traffic through Burp Suite to analyze the authentication flow. Upon inspecting the HTTP history and the raw response from the root directory (`/`), I discovered a critical Information Disclosure vulnerability. The developers left a debug comment in the HTML body containing the backend signing secret:
`<!-- debug: auth_secret=supersecretkey -->`

![Burp Suite - Source Code Leak](Screenshots/Screenshot_2026-04-25_220855.png)

**Step 2: Analyzing the Session Token**
Looking at the request headers, I noticed the `session_token` cookie. The token was Base64 encoded. 

**Step 3: Decoding & Forgery Preparation**
Sending the cookie to Burp Suite's Decoder revealed a JSON object containing the user's state and a cryptographic signature:
`{"username": "guest", "role": "user", "sig": "502138887ed78468c7e7becd22823500"}`

![Burp Suite - Cookie Decoding](Screenshots/Screenshot_2026-04-25_204612.png)

**Step 4: Exploitation (Privilege Escalation)**
Because the application uses a "homegrown" signed cookie mechanism rather than a robust JWT implementation, and because the `auth_secret` was leaked, the system is vulnerable to cookie forgery. 
By changing the `"role": "user"` to `"role": "admin"`, and utilizing the leaked `supersecretkey` to generate a valid new hash for the `"sig"` parameter, I was able to forge an administrative session cookie, bypass access controls, and capture the flag.

---

### 2. [Crypto/Forensics] Dead_Signal

#### Challenge Description
This challenge involved investigating a directory named `Dead_Signal` containing intercepted communications, specifically a Command and Control (C2) beacon and a hex dump file.

#### Methodology & Analysis

**Step 1: Analyzing the C2 Beacon**
Opening the `intercepted` text file revealed Stage 1 of a C2 Beacon transmitted on `2024-04-19 04:00:00 UTC`. The file contained a short ciphertext string:
`ZPDRRNAZNALLYKEAQ`

This appears to be a classic substitution cipher (such as Caesar, Vigenère, or Affine). 

![Intercepted C2 Beacon](Screenshots/Screenshot_2026-04-25_203510.png)

**Step 2: Hexadecimal Decoding**
Next, I investigated the `deadrop.hex` file. The file contained a continuous hex string:
`273126393b313b20352e782f712121320d3961220d39643b102c2e7d66362760332f`

![Hex Dump Analysis](Screenshots/Screenshot_2026-04-25_203525.png)

**Step 3: Decryption & Flag Extraction**
*(Note: Add your specific decryption steps here—e.g., "Converting the hex string to ASCII revealed a secondary payload/clue, which, when combined with the decrypted Stage 1 beacon, yielded the final flag.")*

---

### 🛠️ Tools Used
* **Burp Suite Professional:** Traffic interception, request manipulation, and Base64 decoding.
* **Text Editors / Hex Editors:** Analyzing raw data dumps and intercepted beacon traffic.
* **Browser DevTools:** Initial inspection and cookie management.

---
*Constantly expanding my offensive security toolkit and adapting to real-world threat scenarios.*
