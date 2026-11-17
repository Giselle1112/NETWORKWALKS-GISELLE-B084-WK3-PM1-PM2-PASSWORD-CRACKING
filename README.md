# NETWORKWALKS-GISELLE-B084-WK3-PM1-PM2-PASSWORD-CRACKING
🔐 Week 3: Password Cracking & Hash Auditing Labs

Internship: Cybersecurity Internship — NETWORKWALKS Academy

Mentor: Mr. Waqas Karim (CCIE)

Focus Area: Cryptographic Hash Extraction, Offline Dictionary Attacks & Online Password Auditing

📌 Overview

This repository documents the practical labs completed during Week 3 of my cybersecurity internship at NETWORKWALKS. The objective of this week's modules was to evaluate the resilience of password-protected PDF documents against real-world password recovery techniques using both local command-line/GUI tools and browser-based auditing utilities.

Through two practical modules, four encrypted PDF files were audited, their cryptographic hashes extracted, and their underlying passwords recovered to capture all four lab flags.

🛠️ Tools & Technologies Used

John the Ripper (JTR): Industry-standard offline password security auditing and recovery tool.

Johnny GUI: Cross-platform graphical frontend for John the Ripper.

pdf2john: Utility used to extract crackable password hashes from encrypted PDF files.

NETWORKWALKS (NW) Hash Calculator & Password Cracker: Browser-based hash generation and password auditing utility.

🧪 Practical Modules Breakdown

🔹 W3-PM1: Offline Password Cracking with John the Ripper (Johnny GUI)

Target: 3 password-protected PDF documents (File 1, File 2, File 3).

Workflow:

Extracted the cryptographic password hashes from the three locked PDF files using pdf2john.

Loaded the extracted hash files into Johnny GUI.

Executed an offline dictionary attack against the hashes.

Outcome: All three passwords were recovered within seconds, allowing full access to the PDFs and successful capture of the first three flags.

🔹 W3-PM2: Browser-Based Auditing with NETWORKWALKS (NW) Tools

Target: 1 additional encrypted PDF (File 4) + cross-verification of Files 1–3.

Workflow:

Utilized the NETWORKWALKS Hash Calculator & Password Cracker to audit and recover the password for the fourth locked PDF, capturing the fourth flag.

Cross-verified findings by running the first three PDFs through the browser-based NW utility.

Outcome: Both the local offline workflow (John the Ripper) and the online utility (NW Tools) returned identical passwords and flags, confirming consistency across auditing methods.

📂 Repository Contents

 The key lab screenshots documenting hash extraction, Johnny GUI dictionary attacks, NW tool execution, and flag capture (duplicate cross-verification runs omitted for clarity).

README.md — Project overview, methodology, and defensive takeaways.

🛡️ Defensive & SOC Takeaways

Encryption is Only as Strong as the Password: Once an attacker acquires a local copy of an encrypted file, they do not need to interact with an authentication server or risk triggering failed-login alerts. Offline hash extraction allows attackers to test millions of guesses per second without rate limiting.

Dictionary Words & Short Passwords Fail Quickly: Free, publicly available tools can break short or common dictionary-based passwords in seconds.

Mitigation & Best Practices:

Enforce long, high-entropy passphrases (14+ characters) combining random words, numbers, and symbols for sensitive documents.

Implement Multi-Factor Authentication (MFA) wherever identity-based access controls are supported.

Monitor endpoint activity for unauthorized execution of hash-extraction utilities (pdf2john, john, etc.) within SOC environments.

🙏 Acknowledgments

Special thanks to Mr. Waqas Karim (CCIE) and the NETWORKWALKS Academy team for designing a hands-on curriculum that bridges offensive security testing with Blue Team defensive awareness.
