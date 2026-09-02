# 🛡️ Information Security Awareness Training & Assessment

> **Company Information Security Training Program**  
> *Target Audience:* All Employees, Contractors, and New Hires  
> *Maintained By:* IT / Information Security Department  
> *Version:* 1.0 | *Review Cycle:* Annual / Onboarding  

---

## 🎯 Purpose & Scope

In today's threat landscape, **the human element is the primary target for cyber attackers**. Over 80% of security incidents originate from social engineering, compromised credentials, or human error.

This repository serves as the official **Information Security Awareness Guide and Testing Framework**. It outlines mandatory security principles, common attack vectors, best practices for daily operations, and an interactive assessment quiz to validate staff readiness.

---

## 📑 Table of Contents

1. [Core Principles of Information Security](#1-core-principles-of-information-security)
2. [Identity & Access Management (Passwords & MFA)](#2-identity--access-management)
3. [Social Engineering & Phishing Awareness](#3-social-engineering--phishing-awareness)
4. [Device & Physical Security](#4-device--physical-security)
5. [Data Classification & Privacy (Including AI Usage)](#5-data-classification--privacy)
6. [Network & Remote Work Hygiene](#6-network--remote-work-hygiene)
7. [Incident Response & Reporting Procedures](#7-incident-response--reporting-procedures)
8. [Knowledge Assessment: Test Your Security IQ](#8-knowledge-assessment-test-your-security-iq)
9. [Answer Key & Learning Rationales](#9-answer-key--learning-rationales)
10. [Daily Security Checklist & Employee Pledge](#10-daily-security-checklist--employee-pledge)

---

## 1. Core Principles of Information Security

All corporate security guidelines are built upon the foundational **CIA Triad**:

| Principle | Meaning | Workplace Example |
| :--- | :--- | :--- |
| **Confidentiality** | Data is accessible only to authorized individuals. | Customer financial records are restricted to HR and Accounting. |
| **Integrity** | Data is accurate, consistent, and protected from unauthorized modification. | Invoices and source code cannot be tampered with in transit or storage. |
| **Availability** | Systems, networks, and data are accessible to authorized users when needed. | Disaster recovery plans and backups ensure services stay online. |

### Guiding Rules
* **Principle of Least Privilege (PoLP):** You should only have access to systems and data required to perform your job role. If you switch teams or projects, access should be updated.
* **Zero Trust:** Never trust by default; always verify. Even inside the office network, access requests must be authenticated and authorized.
* **Shared Responsibility:** Information security is not solely the IT department's job; every employee is the first line of defense.

---

## 2. Identity & Access Management

Compromised credentials are the most common initial access vector for breaches.

### 🔑 Passwords vs. Passphrases
* **Avoid Complexity Traps:** Complex short passwords like `P@$$w0rd1!` are easy for computers to crack and hard for humans to remember.
* **Use Passphrases:** Combine 4 or more random, memorable words with spaces or symbols.
  * *Weak:* `Summer2026!`
  * *Strong:* `coffee-stapler-planet-running` (Longer than 16 characters, high entropy).
* **Never Reuse Passwords:** A breach on a private service (e.g., an online store) will immediately be tried by attackers against your corporate email and VPN (Credential Stuffing).
* **Use the Approved Password Manager:** Store unique, complex credentials securely. Never store passwords in plain text, spreadsheets, sticky notes, or browser auto-fills.

### 📱 Multi-Factor Authentication (MFA / 2FA)
Multi-Factor Authentication requires two or more evidence types:
1. **Something you know** (Password, PIN)
2. **Something you have** (Authenticator app, Hardware FIDO2 key, Smartphone)
3. **Something you are** (Fingerprint, Face scan)

#### MFA Golden Rules
* **Never approve a push prompt you didn't trigger:** Attackers use **MFA Fatigue / Push Bombing** (sending dozens of prompts at 3:00 AM) to wear down victims into approving.
* **SMS is the weakest 2FA:** Prefer hardware security keys (e.g., YubiKey) or time-based one-time password (TOTP) apps (Google Authenticator, Microsoft Authenticator) over SMS, which is vulnerable to SIM-swapping.
* **IT Support will NEVER ask for your password or MFA code:** If someone claims to be IT and asks for your 6-digit code or password, report it immediately.

---

## 3. Social Engineering & Phishing Awareness

Social engineering exploits human psychology—urgency, authority, fear, and curiosity—rather than technical vulnerabilities.

### Common Social Engineering Types
```
Social Engineering
 ├── Phishing        (Mass fraudulent emails with malicious links or attachments)
 ├── Spear Phishing  (Targeted attacks customized with personal/work details)
 ├── Whaling / BEC   (Impersonating C-suite executives requesting urgent payments)
 ├── Smishing / Vishing (Attacks over SMS / Voice phone calls)
 └── Baiting         (Leaving infected USB drives in parking lots or lobbies)
```

### 🚩 Red Flags in Suspicious Communications
1. **Artificial Urgency & Fear:** *"Your account will be suspended in 30 minutes! Wire this payment before the end of the day or deal is lost."*
2. **Sender Spoofing & Lookalike Domains:** Look closely at the sender's actual address, not just the display name:
   * Legitimate: `john.doe@company.com`
   * Malicious: `john.doe@cornpany.com`, `john.doe@company-portal.xyz`, or `ceo-urgent-msg@gmail.com`
3. **Mismatched Hyperlinks:** Hover over links (without clicking) to inspect the destination URL. If the text says `https://portal.company.com` but points to `https://login-verify-account.ru`, do not click!
4. **Unexpected Attachments:** Generic invoices, resumes, shipping notifications, or files ending in `.exe`, `.scr`, `.iso`, `.zip`, or macro-enabled documents (`.xlsm`, `.docm`).
5. **Requests for Sensitive Action outside Normal Channels:** Invoices changing bank account routing numbers, requests to purchase gift cards, or requests to bypass approval processes.

---

## 4. Device & Physical Security

Securing hardware and workstations prevents unauthorized physical and local access.

### 💻 Workstation Hygiene
* **Lock Before You Walk:** Whenever stepping away from your desk (even for 30 seconds), lock your screen:
  * **Windows:** `Win + L`
  * **macOS:** `Cmd + Ctrl + Q`
  * **Linux:** `Super + L` or screen lock shortcut.
* **Clean Desk & Clean Screen Policy:**
  * Do not leave confidential documents or sensitive customer records on desks.
  * Shred sensitive printed paperwork using designated cross-cut shredders.
  * Use privacy screen filters when working in public spaces (trains, cafes, airplanes) to prevent **shoulder surfing**.
* **Disk Encryption:** All corporate laptops must have full-disk encryption active (BitLocker on Windows, FileVault on macOS, LUKS on Linux).

### 🔌 Removable Media & Hardware Attacks
* **Curiosity Kills the Network:** Never plug an unknown USB drive into any corporate device. Attackers drop malicious flash drives in office parking lots, cafeterias, and lobbies.
* **Use Approved Storage Only:** Company-approved cloud storage replaces USB thumb drives for data sharing.
* **Badge Access:** Never allow **tailgating** (letting someone walk behind you through a secure door without badging). Politely instruct visitors to check in at reception.

---

## 5. Data Classification & Privacy

Data must be handled according to its sensitivity level throughout its lifecycle (Creation, Storage, Transmission, Destruction).

### Corporate Data Classification Scheme

| Level | Classification | Examples | Handling Rules |
| :---: | :--- | :--- | :--- |
| **1** | **Public** | Marketing brochures, public press releases, job postings. | Free to distribute externally. |
| **2** | **Internal** | Employee directories, internal wikis, organizational charts. | For internal staff only; do not leak externally. |
| **3** | **Confidential** | Source code, financial reports, business plans, vendor contracts. | Need-to-know access; encrypted at rest and in transit. |
| **4** | **Restricted / PII** | Customer personal data (GDPR/HIPAA), credit card numbers, passwords, API secrets. | Strictly controlled, audit-logged, encrypted, masked where possible. |

### 🤖 Generative AI and Third-Party Cloud Tools (Shadow IT)
* **Never paste proprietary data into public AI chatbots:** Do not input internal source code, customer records, employee personal data, or strategic documents into public LLMs (e.g., free tiers of external AI tools) unless explicitly approved by IT/Legal.
* **Shadow IT:** Using unapproved cloud storage (e.g., personal Dropbox, WeTransfer), browser extensions, or messaging apps for company business creates untracked compliance risks.

---

## 6. Network & Remote Work Hygiene

Working remotely or on the road introduces additional network vulnerabilities.

### 📶 Wi-Fi Best Practices
* **Avoid Open Public Wi-Fi:** Coffee shops, hotel, and airport Wi-Fi networks often lack encryption, allowing attackers to intercept unencrypted traffic or execute **Evil Twin / Man-in-the-Middle** attacks.
* **Use Corporate VPN / ZTNA:** Always connect to the corporate Virtual Private Network (VPN) when working remotely before accessing internal systems.
* **Cellular Hotspot Preferred:** When sensitive work is required outside the office, use your company mobile device's cellular hotspot rather than public Wi-Fi.

### 🏠 Home Office Security
* Change the default administrative username and password on your home Wi-Fi router.
* Ensure your home Wi-Fi uses **WPA2-AES or WPA3** encryption.
* Keep home router firmware updated.
* Separate work devices from IoT smart devices (smart TVs, IoT bulbs, IP cameras) using a guest Wi-Fi network if supported.

---

## 7. Incident Response & Reporting Procedures

Speed is paramount when containing a security incident. An early report can stop a ransomware infection before it spreads to the entire organization.

```
       🚨 If you suspect an incident:
       
Step 1: DISCONNECT      Step 2: REPORT IMMEDIATELY      Step 3: COOPERATE
Turn off Wi-Fi or       Call the IT Security Hotline    Provide details
unplug Ethernet cord.   Do NOT attempt DIY cleaning.    (Don't panic!)
```

### ⚡ When to Report an Incident
Report immediately if you observe:
* You clicked a link and entered your credentials on a suspicious site.
* A device was lost, stolen, or left unattended in an insecure location.
* Unexplained pop-ups, encrypted file extensions, or system sluggishness.
* Unexpected password reset notifications or MFA push requests.
* An email instructing unusual financial transfers or credential changes.

### 🤝 No-Blame Culture
> **Remember:** Everyone makes mistakes. If you clicked a phishing link or downloaded an attachment by accident, **report it immediately**. You will not be penalized for proactive reporting. Concealing or delaying a report turns a minor incident into a company-wide breach.

### 📞 Security Contacts
* **IT Helpdesk:** `it-support@company.internal` | Ext: `x1000`
* **Security Operations (SOC):** `security@company.internal` | Emergency Phone: `+1 (555) 019-SAFE`
* **Internal Slack/Teams Channel:** `#it-security-help`

---

## 8. Knowledge Assessment: Test Your Security IQ

Use this 10-question evaluation to test employee understanding. Answers and rationales are provided in Section 9.

---

### Question 1: Phishing Identification
You receive an email from `support@micros0ft-security-update.com` stating: *"Urgent: Critical vulnerability detected on your laptop. Click here to download the patch within 2 hours or your account will be locked."* What is the proper response?
- **A)** Click the link immediately to download the patch so your laptop remains safe.
- **B)** Forward the email to all colleagues to warn them.
- **C)** Do not click any links; report the email to the IT Security team using the PhishAlarm/Report button.
- **D)** Reply to the email asking if the email is legitimate.

---

### Question 2: Authentication & Credentials
Which of the following is the most secure password practice?
- **A)** `P@ssw0rd2026!` changed every 30 days and written on a sticky note under your keyboard.
- **B)** A 18-character passphrase stored in an approved corporate password manager, paired with hardware token MFA.
- **C)** Reusing the same 12-character alphanumeric password across your work email, personal email, and LinkedIn.
- **D)** Saving your master password in a browser text file named `credentials.txt` on your desktop.

---

### Question 3: MFA Push Bombing
At 2:30 AM, your phone receives four consecutive MFA push notifications requesting approval to log into your corporate portal. You did not initiate this login. What should you do?
- **A)** Approve the notification so your phone stops vibrating and you can go back to sleep.
- **B)** Deny the request, do not approve, and immediately report the unauthorized attempts to IT Security in the morning or via emergency line.
- **C)** Turn off your phone and ignore it.
- **D)** Share the code with a coworker to see if they are also receiving it.

---

### Question 4: Physical Security & Tailgating
You badge into the office main entrance. An unfamiliar person carrying two heavy boxes walks right behind you and asks you to hold the door. How should you respond?
- **A)** Let them in immediately; holding doors is common courtesy.
- **B)** Hold the door, but ask for their employee ID after they set the boxes down.
- **C)** Politely hold the door open while asking them to badge in separately or escort them to the reception desk for verification.
- **D)** Run away and ignore them.

---

### Question 5: Physical Media & Baiting
While walking through the office parking lot, you find a branded 64GB USB flash drive labeled *"Executive Compensation 2026 - Confidential"*. What should you do?
- **A)** Plug it into your work laptop to see who owns it and return it.
- **B)** Plug it into a home computer instead to avoid infecting work systems.
- **C)** Hand the drive directly over to IT Security without plugging it into any device.
- **D)** Format the drive so you can reuse it for personal backups.

---

### Question 6: Public Wi-Fi
You are traveling and need to send a confidential contract to a client while waiting at an airport with free, unsecured public Wi-Fi. What is the safest approach?
- **A)** Connect to the airport Wi-Fi and send the document as quickly as possible.
- **B)** Use your corporate phone's encrypted cellular hotspot, or connect to the corporate VPN before accessing company files.
- **C)** Ask another passenger to share their personal Wi-Fi password.
- **D)** Rename the file to `vacation_photos.zip` and send it over public Wi-Fi.

---

### Question 7: Artificial Intelligence & Sensitive Data
You want to summarize a confidential internal sales report and extract customer contact details. You open a free public generative AI tool in your browser. What should you do?
- **A)** Paste the entire report into the prompt; public AI tools keep all data completely confidential.
- **B)** Only paste the customer names and phone numbers, but remove the company names.
- **C)** Do not paste confidential corporate data, customer PII, or internal metrics into public AI tools; consult IT for approved enterprise AI environments.
- **D)** Translate the text into another language first, then paste it.

---

### Question 8: Business Email Compromise (BEC)
You receive an email appearing to come from your CEO: *"I am in an urgent closed-door acquisition meeting and cannot talk. Please wire $25,000 immediately to this new supplier account. Do not call me, just confirm once done."* What should you do?
- **A)** Execute the transfer immediately because it came from the CEO and states it is urgent.
- **B)** Verify the request through a secondary, out-of-band communication channel (e.g., known phone number, direct manager, or standard finance verification procedure) before taking any action.
- **C)** Reply to the email asking the CEO for their credit card number instead.
- **D)** Forward the email to your personal email account to process it from home.

---

### Question 9: Workstation Security
You are leaving your desk for 5 minutes to grab coffee in the office breakroom. What should you do?
- **A)** Leave your computer unlocked since you will be back in under 5 minutes.
- **B)** Turn off your monitor, leaving the PC unlocked.
- **C)** Lock your workstation (`Win + L` or `Cmd + Ctrl + Q`) before leaving.
- **D)** Ask a neighbor to look at your screen while you are away.

---

### Question 10: Post-Click Response
You accidentally click a link in an email and enter your corporate password on a site that you immediately realize is a fake login portal. What is the correct protocol?
- **A)** Close the browser tab and pretend nothing happened to avoid getting into trouble.
- **B)** Wait 24 hours to see if any unusual charges or logins occur.
- **C)** Immediately disconnect network access (Wi-Fi/cable), notify the IT Security Incident team, and change your password from another secure device.
- **D)** Delete your browser history and restart your computer.

---

## 9. Answer Key & Learning Rationales

| Question | Correct Answer | Rationale |
| :---: | :---: | :--- |
| **Q1** | **C** | Legit vendors do not send urgent ultimatum emails from lookalike domains (`micros0ft...`). Report it without clicking links or downloading attachments. |
| **Q2** | **B** | Long passphrases stored in an encrypted vault paired with hardware MFA provide maximum defense against brute-forcing, credential stuffing, and phishing. |
| **Q3** | **B** | Repeated unsolicited MFA requests represent an MFA Fatigue attack. Approving grants the attacker full access. Deny and report immediately. |
| **Q4** | **C** | Tailgating relies on politeness. Everyone must badge in or be checked in by reception to ensure facility integrity. |
| **Q5** | **C** | The USB is a classic "Baiting" trap containing malware or BadUSB payload designed to execute scripts on connection. Always surrender found media to IT. |
| **Q6** | **B** | Open Wi-Fi is vulnerable to eavesdropping and rogue access points. Cellular hotspots and enterprise VPNs encrypt traffic end-to-end. |
| **Q7** | **C** | Data entered into public AI tools may be retained, used for model retraining, or exposed in breaches. Never expose company confidential data. |
| **Q8** | **B** | Urgent payment requests bypassing verification protocols are classic BEC scams. Always verify out-of-band using predetermined numbers or workflows. |
| **Q9** | **C** | An unlocked workstation takes only seconds to compromise or photograph. Always lock your screen every time you step away. |
| **Q10** | **C** | Prompt reporting allows the security team to revoke active sessions and reset credentials before the attacker establishes persistence. |

---

## 10. Daily Security Checklist & Employee Pledge

### ✅ Daily Security Checklist
- [ ] My screen is locked whenever I am away from my desk.
- [ ] No passwords, access tokens, or sensitive papers are left in open view.
- [ ] I verify sender addresses and hover over links before clicking.
- [ ] I only use company-approved tools and storage solutions for work documents.
- [ ] I immediately report any strange system behavior or suspicious communications.

### ✍️ Employee Security Pledge
> *"I understand that I play an essential role in protecting company data, systems, and customer privacy. I commit to following the security policies outlined in this guide, maintaining vigilance against social engineering, and reporting suspected security issues promptly to the IT Security team."*

---
*For questions, training suggestions, or policy clarifications, please contact the IT Security Team.*
