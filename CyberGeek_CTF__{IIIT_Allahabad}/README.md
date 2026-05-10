# CyberGeek'26 CTF Writeup — Root@Kali

![Certificate](Certificate/Root@Kali_Vishu%20Raj_.png)

## 🚩 Event Overview

**Event:** CyberGeek'26 Capture The Flag (CTF)  
**Organized By:** GeekHaven under Aparoksha, IIIT Allahabad  
**Team Name:** Root@Kali  
**Participants:** 300+ Teams  
**Domain:** Cybersecurity / Ethical Hacking / Real-World Security Challenges

CyberGeek'26 was a competitive cybersecurity event focused on real-world offensive security concepts including Web Exploitation, Cryptography, Reverse Engineering, OSINT, Steganography, Forensics, Binary Exploitation, and Networking.

This competition tested not only technical ability but also:

- Analytical thinking
- Time management under pressure
- Team collaboration
- Enumeration methodology
- Exploitation logic
- Research capability
- Persistence during dead-ends

---

# 🧠 Skills Demonstrated

## Offensive Security Skills

- Web Application Security Testing
- Manual Vulnerability Discovery
- SQL Injection Testing
- Cross-Site Scripting (XSS)
- Authentication Bypass Techniques
- Directory & Subdomain Enumeration
- Packet & Traffic Analysis
- Linux Privilege Escalation Basics
- Hash Analysis & Cracking
- Steganography Investigation
- Binary Inspection
- OSINT Methodology

---

# 🛠️ Tools Used

| Category | Tools |
|---|---|
| Recon | Nmap, Sublist3r, ffuf |
| Web Testing | Burp Suite, Browser DevTools |
| Crypto | CyberChef, Hashcat, JohnTheRipper |
| Forensics | Wireshark, ExifTool, Strings |
| Steganography | Steghide, zsteg |
| Reverse Engineering | Ghidra, file, objdump |
| Misc | Linux CLI, Python Scripts |

---

# 📂 Challenge Categories

- Web Exploitation
- Cryptography
- Reverse Engineering
- Forensics
- Steganography
- OSINT
- Networking
- Miscellaneous

---

# 🔥 Writeups

---

# 1. Web Exploitation Challenge

## Objective
Identify and exploit vulnerabilities in the target web application to retrieve the hidden flag.

## Methodology

### Step 1 — Reconnaissance
- Inspected the web application structure
- Enumerated hidden endpoints
- Analyzed request/response behavior
- Checked HTTP headers and parameters

### Step 2 — Manual Testing
- Intercepted traffic using Burp Suite
- Tested for SQL Injection payloads
- Checked reflected inputs for XSS
- Analyzed authentication workflow

### Step 3 — Exploitation
- Identified weak input validation
- Manipulated parameters manually
- Retrieved sensitive response data
- Extracted the flag successfully

---

## Screenshots

### Initial Recon
![Recon](Screenshots/Screenshot%202026-04-18%20025957.png)

### Request Analysis
![Burp](Screenshots/Screenshot%202026-04-19%20005312.png)

### Exploitation Phase
![Exploit](Screenshots/Screenshot%202026-04-19%20010714.png)

---

# 2. Cryptography Challenge

## Objective
Analyze encrypted or encoded content and recover the original flag.

## Methodology

### Analysis Performed
- Identified encoding patterns
- Tested hashing algorithms
- Performed frequency analysis
- Used CyberChef for layered decoding

### Tools Used
- CyberChef
- Hashcat
- JohnTheRipper

### Outcome
Successfully reversed the challenge logic and recovered the hidden flag.

---

## Screenshots

![Crypto1](Screenshots/Screenshot%202026-04-19%20010739.png)

![Crypto2](Screenshots/Screenshot%202026-04-19%20010952.png)

---

# 3. Forensics Challenge

## Objective
Investigate files, metadata, and traffic captures to uncover hidden evidence.

## Investigation Process

### File Analysis
- Extracted metadata using ExifTool
- Checked hidden strings and file signatures
- Inspected suspicious archives

### Traffic Analysis
- Opened PCAP files in Wireshark
- Filtered suspicious packets
- Reconstructed network activity

### Result
Recovered hidden indicators and extracted the required flag.

---

## Screenshots

![Forensics1](Screenshots/Screenshot%202026-04-19%20011813.png)

![Forensics2](Screenshots/Screenshot%202026-04-19%20014103.png)

---

# 4. Steganography Challenge

## Objective
Discover hidden data embedded inside media files.

## Approach

### Enumeration
- Inspected file metadata
- Performed binary inspection
- Checked for hidden layers and appended content

### Extraction
- Used steganography tools
- Extracted concealed information
- Decoded recovered artifacts

### Result
Successfully extracted the embedded flag.

---

## Screenshots

![Steg1](Screenshots/Screenshot%202026-04-19%20015205.png)

![Steg2](Screenshots/Screenshot%202026-04-19%20021747.png)

---

# 5. Reverse Engineering Challenge

## Objective
Analyze executable logic and recover the validation mechanism.

## Process

### Static Analysis
- Checked binary structure
- Inspected strings and symbols
- Traced logic flow

### Dynamic Observation
- Monitored execution behavior
- Identified validation conditions
- Reconstructed challenge logic

### Result
Recovered the hidden flag after reversing the binary workflow.

---

## Screenshots

![Rev1](Screenshots/Screenshot%202026-04-19%20022137.png)

![Rev2](Screenshots/Screenshot%202026-04-19%20022736.png)

---

# 6. Networking & Miscellaneous Challenges

## Topics Covered

- Packet Analysis
- Service Enumeration
- Port Scanning
- Header Inspection
- Protocol Analysis
- Encoding Tricks
- Logic-Based Challenges

## Key Learning
These challenges reinforced the importance of:

- Attention to detail
- Enumeration depth
- Systematic methodology
- Fast adaptation during live environments

---

## Screenshots

![Misc1](Screenshots/Screenshot%202026-04-19%20023055.png)

![Misc2](Screenshots/Screenshot%202026-04-19%20023922.png)

---

# 📈 Key Takeaways

## Technical Growth

This CTF significantly improved:

- Real-world attack methodology
- Exploitation workflow
- Reconnaissance strategy
- Web application testing skills
- Linux command-line efficiency
- Problem-solving speed
- Security research mindset

---

# 💡 What This Competition Proved

Most beginners approach cybersecurity by memorizing tools. Competitive CTF environments expose why that approach fails.

CyberGeek'26 forced practical thinking:

- Enumeration mattered more than assumptions
- Logic mattered more than automation
- Patience mattered more than brute force
- Understanding protocols mattered more than copy-paste payloads

The competition highlighted a critical reality of cybersecurity:

> The difference between average participants and strong security practitioners is methodology, not tool collection.

---

# 🚀 Future Goals

After participating in CyberGeek'26, the next focus areas are:

- Advanced Web Exploitation
- Active Bug Bounty Hunting
- Binary Exploitation
- Malware Analysis
- Cloud Security
- Red Team Methodology
- Advanced Reverse Engineering

---

# 🏆 Conclusion

CyberGeek'26 was not just a competition — it was a high-pressure practical cybersecurity environment that strengthened offensive security fundamentals and improved real-world problem-solving capability.

Competing against 300+ teams provided valuable exposure to modern attack techniques, structured enumeration, and collaborative security research.

This experience further reinforced the transition from learning cybersecurity theoretically to applying it practically.

---

## 🔗 LinkedIn
[Connect with me on LinkedIn](https://www.linkedin.com/in/vishu-raj-49ab332b9/)

---

# ⭐ Final Note

CTFs are not about collecting certificates.

They expose weaknesses in thinking, methodology, and technical depth. Every failed challenge reveals a gap that needs improvement.

That is exactly why competitive cybersecurity environments accelerate growth faster than passive learning.

