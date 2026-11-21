#  Password Cracking & Hash Extraction Lab (John the Ripper & Johnny GUI)

##  Project Overview
This repository documents two hands-on Cybersecurity & Ethical Hacking lab modules focused on password recovery, cryptographic hashing, and PDF security auditing on Windows:
1. **Module 1:** Extracting a PDF password hash and cracking it offline using **John the Ripper (JTR)** and the **Johnny GUI**.
2. **Module 2:** Extracting and cracking the same protected PDF hash using browser-based dictionary attack tools (**Networkwalks Hash Calculator & Password Cracker**).

> **Disclaimer:** This project was completed strictly for educational purposes in a controlled lab environment to understand password vulnerabilities and cryptographic defense mechanisms.

---

##  Tools & Technologies Used
* **John the Ripper (1.9.0-jumbo-1 Win64):** Command-line password security auditing and hash cracking engine.
* **Johnny GUI:** Graphical interface wrapper for managing JTR sessions and attacks.
* **Online Hash Crack / Networkwalks Hash Calculator:** Tools for extracting `$pdf$...` cryptographic hashes from encrypted PDF files.
* **Windows 10/11 Environment**

---

##  Step-by-Step Methodology

### Module 1: Offline Cracking with John the Ripper & Johnny
1. **Environment Configuration:** Installed John the Ripper (`john-1.9.0-jumbo-1-win64`) and Johnny GUI, linking Johnny's executable path directly to `run/john.exe`.
2. **Hash Extraction:** Uploaded the target encrypted file (`My Locked PDF1.pdf`) to extract its `$pdf$` hash string and saved it cleanly into `hash1.txt`.
3. **Dictionary / Default Attack:** Loaded `hash1.txt` into Johnny and launched a new attack.
4. **Verification:** Successfully recovered the plaintext password (`password1`) and unlocked the target PDF to capture the completion flag.

### Module 2: Browser-Based Dictionary Attack
1. **Local Hash Computation:** Parsed `My Locked PDF1.pdf` using the Networkwalks Hash Calculator to obtain the `$pdf$` hash.
2. **Dictionary Attack Simulation:** Ran a wordlist attack against the extracted hash in the Networkwalks Password Cracker, confirming how weak/common passwords (`password1`) are compromised within seconds.

---

##  Key Security Takeaways
* **Encryption vs. Hashing:** Encryption is a two-way process reversible with the right key, whereas hashing is a one-way cryptographic function used to verify passwords without storing them in plaintext.
* **Why Password Complexity Matters:** Short, dictionary-based passwords (like `password1` or `123456`) can be cracked almost instantly once a file's hash is extracted.
* **Mitigation:** Always enforce long, high-entropy passphrases (12+ characters with mixed uppercase, lowercase, numbers, and symbols) to protect sensitive documents.

---

## 📸 Lab Screenshots
*(Add your screenshots inside the `screenshots/` folder and link them here)*
* `Start.png` – Configuring `john.exe` in Johnny GUI
* `FirstCracking.png` – Password successfully cracked in Johnny
* `SecongCracking.png` – Target PDF unlocked
  
