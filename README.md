# devhub-week1-security-assessment
Week 1 – Security Assessment for my Cybersecurity Internship at DevelopersHub. Performed vulnerability testing (XSS, SQL Injection, security headers) on a mock user management system.

## 📌 Overview
As part of Week 1 of my Cybersecurity Internship at **DevelopersHub**, I performed a **basic vulnerability assessment** on a simple User Management System running locally (`http://localhost:3000`).  
The goal was to identify common web application vulnerabilities and document possible improvements.

---

## 🔍 Scope
- Target: Localhost test app (`http://localhost:3000`)
- Pages tested: Signup, Login
- Type: Educational mock application only

---

## 🛠️ Tools Used
- **OWASP ZAP** – Automated vulnerability scanning
- **Browser DevTools** – Manual payload injection & header inspection
- **Manual Testing** – XSS & SQL Injection probes
- **Screenshots & Documentation** – Evidence collection

---

## ⚡ Vulnerabilities Found
- **XSS (Cross-Site Scripting)** – Input fields accepted `<script>alert('XSS')</script>`.
- **SQL Injection Attempts** – Login form tested with payloads like `admin' OR '1'='1`. (Explained results in report.)
- **Weak Authentication Design** – Plaintext password storage (no hashing).
- **Missing Security Headers** – No `Content-Security-Policy`, `X-Content-Type-Options`, etc.

---

## ✅ Recommendations
- Sanitize & validate user input (`validator` library).
- Hash & salt passwords using **bcrypt**.
- Implement token-based authentication using **JWT**.
- Secure HTTP headers using **Helmet.js**.
- Enforce HTTPS for secure transmission.

---

## 📂 Deliverables
- 📄 [Week 1 Report (PDF)](./Week1-Report.pdf)  
- 🎥 [Video Demonstration](https://drive.google.com/file/d/16CWmtwXkp5AvkErDzDoRH7Kp8FYgI_53/view?usp=drive_link)  
- 📂 ZAP Scan Report → /zap-report
---
