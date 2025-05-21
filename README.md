## 🔐 Login Page Brute Forcer

This project is a **Python-based tool** designed to perform a brute force attack on web login forms. It takes a list of potential passwords and systematically attempts to log into a given URL with a specific username, helping identify the correct credentials based on the response returned by the target page.

> ⚠️ **Disclaimer:** This tool is intended **only for ethical use**, such as penetration testing on systems you own or have explicit permission to test. Unauthorized use against systems you do not have permission to access is illegal and unethical.

---

### 📌 Features

* Accepts custom **URL**, **username**, and **password list**.
* Identifies login failure using a custom **login failure string**.
* Supports optional **cookie injection** for session-based authentication.
* Uses **GET** (with cookies) and **POST** methods to attempt login requests.
* Highlights progress and results using **colored terminal output**.

---

### 🧠 How It Works

1. The script prompts the user for:

   * Login page URL
   * Target username
   * Path to the password wordlist
   * The string that appears on a failed login attempt
   * Optional cookie value (for sessions requiring authentication)

2. It reads the password list line by line and attempts a login for each password.

3. If the server’s response **does not contain** the failure string, the script concludes the login was successful and displays the valid credentials.

4. If no password matches, it notifies the user that the password is not in the list.

---

### 🚀 Getting Started

#### 🔧 Prerequisites

* Python 3.x
* `requests` and `termcolor` libraries

You can install the required libraries using:

```bash
pip install requests termcolor
```

#### ▶️ Usage

```bash
python3 bruteforce_login.py
```

You will be prompted to enter:

* Login URL
* Target Username
* Path to Password File
* Failure String (e.g., "Invalid Credentials")
* Optional Cookie Value

Example:

```
[+] Enter Page URL: https://example.com/login
[+] Enter Username For The Account To Bruteforce: admin
[+] Enter Password File To Use: passwords.txt
[+] Enter String That Occurs When Login Fails: Invalid username or password
Enter Cookie Value(Optional): session=123abc
```

---

### 🛡️ Warning

Use this tool **only on systems you own or are authorized to test**. Brute-force attacks are illegal on systems you do not have permission to access and can lead to criminal charges.

---
