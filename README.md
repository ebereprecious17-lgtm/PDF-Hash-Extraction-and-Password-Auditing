# 🔐 Week 3 Lab: Cryptographic Hash Extraction & Password Auditing

## 📌 Project Overview
This repository documents my third week of hands-on cybersecurity internship training at **NETWORKWALKS** (mentored by **Waqas Karim, CCIE**)[cite: 3]. The focus of these two lab modules was evaluating document encryption resilience, extracting underlying cryptographic hashes from locked files, and executing offline dictionary-based password recovery[cite: 1, 2, 3].

> **Disclaimer:** *All testing, hash extraction, and password recovery exercises documented in this repository were conducted strictly within an authorized training environment using designated practice files (`My Locked PDF1.pdf` and `My Locked PDF2.pdf`)[cite: 1, 2, 3].*

---

## 🛠️ Tools & Environment
* **Operating System:** Windows[cite: 1, 2, 3]
* **Password Auditing:** John the Ripper (JTR) & Johnny GUI[cite: 1, 3]
* **Hash Analysis & Extraction:** PDF Hash Extractor, Hash Calculator, NetworkWalks Password Cracker[cite: 1, 2]

---

## ⚙️ Lab Execution & Methodology

### Module 1: Hash Extraction & Dictionary Attack with John the Ripper
1. **Target Inspection & Hash Isolation:** Analyzed the first password-protected document (`My Locked PDF1.pdf`) using a **PDF Hash Extractor** to isolate its internal cryptographic hash string (`$pdf$4*4*128...`)[cite: 1].
2. **Hash Formatting:** Saved and formatted the extracted hash into a clean text file (`hash1.txt`) prepared for offline processing[cite: 1].
3. **Password Recovery:** Imported the hash file into **Johnny** (the graphical interface for **John the Ripper**) and launched a targeted dictionary attack[cite: 1].
4. **Verification:** Successfully recovered the plaintext password (`good-luck`), unlocked the PDF document, and captured the first lab flag[cite: 1].

### Module 2: Secondary Hash Analysis & Password Cracking
1. **Cryptographic Verification:** Examined hash structures and checksum behavior using a **Hash Calculator**[cite: 2].
2. **Credential Recovery:** Utilized the **NetworkWalks Password Cracker** alongside hash extraction utilities to audit the second restricted target (`My Locked PDF2.pdf`)[cite: 2].
3. **Verification:** Recovered the access credentials, opened the secured document, and captured the second lab flag[cite: 2].

---

## 🛡️ Key Security Takeaways & Defensive Remediation
* **High-Entropy Password Policies:** Encryption is only as strong as the password protecting it. Short or dictionary-based passwords (`good-luck`) can be compromised within seconds once an attacker obtains the underlying file hash[cite: 1]. Organizations should enforce a minimum of 12–16 characters mixing uppercase, lowercase, numbers, and symbols.
* **Eliminate Predictable Passwords:** Avoid common words, phrases, or predictable substitutions that are easily defeated by standard wordlists and rule-based attacks.
* **Defense in Depth:** Sensitive documents and accounts should never rely solely on single-factor password protection; combine strong encryption with strict access controls and Multi-Factor Authentication (MFA).

---

## 📸 Lab Evidence
*(Tip: Upload your screenshots into an `/images` folder in your repository and link them below)*
* `images/john-the-ripper-crack.png` – Hash extraction and plaintext recovery in Johnny GUI[cite: 1]
* `images/flag-1-capture.png` – Successful decryption of `My Locked PDF1.pdf`[cite: 1]
* `images/flag-2-capture.png` – Successful decryption of `My Locked PDF2.pdf`[cite: 2]
### Lab Screenshots
![John the Ripper Password Recovery](john-the-ripper.jpg)
![NetworkWalks Flag Capture](networkwalks-passwordcrack.jpg)
