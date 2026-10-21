# 🔐 Cyber-Pass — Password Strength & Breach Checker
A privacy-focused web application that checks password strength locally and checks whether a password appears in known data breaches.
* Cyber-Pass is designed to help users make better password security decisions without sending their raw passwords to the breach-checking service.

## ✨ Features
- **Password Strength Checker** — Evaluates password length, character variety, and common patterns.
- **Breach Detection** — Checks passwords against known breach data using the Have I Been Pwned Pwned Passwords range API.
- **Privacy-Focused Design** — Computes the password hash in the browser and sends only its first five characters for the breach lookup.
- **Show/Hide Password** — Toggle password visibility whenever needed.
- **Real-Time Strength Meter** — Shows a visual strength estimate as you type.
- **Clear Button** — Quickly clears the password field and resets the results.
- **Responsive Interface** — Designed to work on desktop and mobile screens.
- **No Account Required** — Use the checker without signing up.

## 🛠️ Tech Stack
- HTML5
- CSS3
- JavaScript
- Web Crypto API
- Have I Been Pwned Pwned Passwords API
### Run Locally
1. Download or clone this repository.
2. Open the project folder.
3. Open `index.html` in a modern browser.
4. Enter a password to view its estimated strength.
5. Select **Check password** to check for known breach matches.
The browser-based checker uses the HTML, CSS, and JavaScript files. The Python files are currently placeholders.

## 🔒 How Password Breach Checking Works
1. The application evaluates password strength locally in the browser.
2. When you request a breach check, the browser calculates the password's SHA-1 hash.
3. Only the first five characters of that hash are sent to the Pwned Passwords API.
4. The API returns matching hash suffixes and their breach counts.
5. The application compares the full hash locally and displays the result.

*Privacy*: Your raw password is never sent to the breach-checking API. Cyber-Pass hashes it locally and sends only the first five characters of the SHA-1 hash, using the k-anonymity approach. Standard network metadata may still be processed by the service.

## ⚠️ Security Notes
- A password not found in breach data is not necessarily secure.
- A strength score is an estimate, not a guarantee of password security.
- Never enter passwords you currently use for sensitive accounts into an online checker unless you trust its implementation.
- Use unique passwords for every account and consider a reputable password manager.
- Avoid using personal information, predictable
