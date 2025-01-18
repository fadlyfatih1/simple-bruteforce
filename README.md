# BWAPP Brute Force Script

This script is designed to brute force login credentials for the [BWAPP](https://bwapp.hakhub.net/login.php) website. The script tries different passwords from a provided list and attempts to log in using a known username (`admin`). It is a simple demonstration of how a brute force attack works on web applications and should only be used for educational purposes on platforms where you have permission to test.

**Disclaimer:** This script should only be used on sites or applications where you have explicit permission to perform security testing. Unauthorized access to systems or accounts is illegal and unethical.

---

## Requirements

- Python 3.x
- `requests` library (install it via `pip install requests`)

---

## Usage

1. **Create an account**: Visit the [BWAPP](https://bwapp.hakhub.net/login.php) website and register a new account if you haven't already.
   
2. **Prepare the Password List**: Prepare a text file containing a list of potential passwords (one per line). This file will be used in the brute force attempt.

3. **Run the Script**: Run the script with the following command:

    ```bash
    python bruteforce.py
    ```

4. **Enter Required Information**: The script will ask for the following input:

   - **Page URL**: Enter the login page URL of the BWAPP website. (The default URL is `https://bwapp.hakhub.net/login.php`)
   - **Username**: Enter the username for the account to brute force. (Default is `admin`)
   - **Password File**: Enter the path to the password list file (e.g., `passwords.txt`).
   - **Login Failed String**: Enter the string that appears on the website when the login fails. (Usually something like "Incorrect username or password.")
   - **Cookie Value (Optional)**: If the website requires a session cookie for the login, you can provide it here.

---

## Example

Here is an example of running the script:

```bash
[+] Enter Page URL: https://bwapp.hakhub.net/login.php
[+] Enter Username For The Account To Bruteforce: admin
[+] Enter Password File To Use: password.txt
```

## Script Logic

   - The script will read the password file line by line.
   - For each password, it will attempt to login using the POST method with the provided username and password.
   - If the login attempt fails (based on the failed login string you provided), it will continue to the next password.
   - If it finds a valid login (i.e., no failed login string in the response), it will print the correct username and password.

## Important Notes
   - Only use this script for educational purposes and on platforms where you have permission to perform security testing (e.g., bug bounty programs or your own lab environment).
   - Brute-forcing websites without permission is illegal and unethical.
