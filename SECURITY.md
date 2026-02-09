# Security - Local Wiki (Flask Version)

**Version:** 1.0

This document outlines the security considerations for using the **Local Wiki (Flask Version)**. This app is designed for **personal/local use only**. It is **not intended for public or production use** without additional security measures.

---

## 1. Local Use Only

* This app is meant to run on your own machine, typically accessed via `http://127.0.0.1:5000/`.
* **Do not expose** the Flask development server to the internet. The built-in Flask server is **not secure** and is meant for development/testing only.
* If you want remote access, use a proper **production-grade server** (e.g., Gunicorn, Nginx) with HTTPS and authentication.

---

## 2. Data Storage

* All notes and tags are stored in a **plain JSON file** (`wiki.json` by default).
* No encryption is applied; **anyone with access to your filesystem can read or modify your data**.
* Avoid storing **sensitive information** (passwords, personal identifiers, API keys) in this wiki.
* Regularly back up your JSON file to prevent accidental data loss.

---

## 3. User Input

* The app does **not include user authentication** or role-based access.
* There is **no input sanitization beyond what Flask provides**. While HTML is escaped in templates by default, **avoid pasting malicious scripts** in notes.
* This app assumes all users on the machine are **trusted**.

---

## 4. Recommendations

1. **Keep it local** – Only access via localhost.
2. **Back up your JSON file** often.
3. **Do not run as admin/root** unless necessary.
4. **Consider encryption** if you want to store sensitive notes (e.g., use a simple Python encryption library to encrypt/decrypt note content).
5. **Firewall your machine** if you accidentally expose the port externally.

---

## 5. Known Limitations

* No authentication or permissions system.
* No HTTPS or network security.
* Plaintext JSON storage.
* Sidebar JavaScript is client-side only; no security measures are implemented for web attacks beyond basic Flask defaults.

---

## 6. Disclaimer

This app is **provided "as-is"**. The developer is **not responsible** for any data loss or security issues caused by misuse. Use at your own risk.

---
