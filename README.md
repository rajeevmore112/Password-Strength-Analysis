## Password-Strength-Analysis
Author: Rajeev More
Date: October 28, 2025

## Objective
To create passwords of varying strength, test them using online tools, and analyze what makes them secure.

## Tools Used
 - PasswordMeter: Calculates strength based on complexity rules (length, symbols, case, numbers). `https://passwordmeter.com`
 - NordPass Password Checker: Estimates crack time and checks breach exposure via HaveIBeenPwned.                                  `https://nordpass.com/password-strength-checker`

## Combined results of PasswordMeter & NordPass
| ID  | Password              | PasswordMeter Score | NordPass Strength | Crack Time | Breach Exposure | Verdict                     |
| --- | --------------------- | ------------------- | ----------------- | ---------- | --------------- | --------------------------- |
| P1  | password123           | 43%                 | Weak              | 2 sec      | 1,238,605 leaks |  Very Weak                 |
| P2  | summer2025            | 53%                 | Weak              | 5 days     | 124 leaks       |  Weak                      |
| P3  | BlueDog77             | 66%                 | Moderate          | 1 day      | 98 leaks        |  Moderate but compromised |
| P4  | myfavbook!            | 30%                 | Weak              | 12 days    | No leaks        |  Weak but not exposed     |
| P5  | T!gerEye55            | 84%                 | Moderate          | 12 days    | No leaks        |  Secure                    |
| P6  | M0on_R!ver88          | 100%                | Strong            | 3 years    | No leaks        |  Strong                    |
| P7  | r4!nB0w$C!ty_92       | 100%                | Strong            | Centuries  | No leaks        |  Very Strong              |
| P8  | q@Z8x#nM3Lp^rT        | 100%                | Strong            | Centuries  | No leaks        |  Excellent                |
| P9  | J9!vLr7@tE3pQ#2z      | 100%                | Strong            | Centuries  | No leaks        |  Excellent                |
| P10 | 9#Kp!7t^GxVw@1zQeL%2m | 100%                | Strong            | Centuries  | No leaks        |  Extremely Secure         |

## Key Observations
- Short passwords and common words fail both tests easily.
- Exposure in breaches is as dangerous as weak complexity.
- Randomized passwords (14+ characters) achieve “Strong” results across both tools.
- Using symbols, mixed case, and numbers dramatically increases entropy.
- Both tools complement each other — PasswordMeter quantifies complexity, NordPass validates real-world safety.

## Tip to create Strong passwords 
| Category    | Example        | Strength     | Recommendation                      |
| ----------- | -------------- | ------------ | ----------------------------------- |
| Weak        | password123    |  Very Weak   | Avoid common words/numbers          |
| Moderate    | BlueDog77      |  Medium      | Add symbols and more length         |
| Strong      | M0on_R!ver88   |  Strong      | Good balance of length & complexity |
| Very Strong | q@Z8x#nM3Lp^rT |  Excellent   | Ideal for password manager use      |

- Use 14–16+ characters per password.
- Mix uppercase, lowercase, digits, and symbols.
- Avoid dictionary words or personal info.
- Check for leaks via HaveIBeenPwned
- Enable Multi-Factor Authentication (MFA).
- Store credentials in a secure password manager.
- Change passwords periodically for high-value accounts.

## Common Password Attacks
1. Brute-Force Attack
- A brute-force attack systematically tries every possible combination of characters until the correct password is found.
- Example: Trying all 6-character combinations like aaaaaa, aaaAaa, aaa1aa, etc.
- Tip: Use long passwords (12+ characters) with diverse characters. Every extra character exponentially increases cracking     time.
 
2. Dictionary Attack
- A dictionary attack uses a pre-compiled list of common words or leaked passwords to guess credentials quickly.
- Example: Using lists like password, welcome, qwerty123, letmein.
- Tip: Avoid using real words or predictable combinations (like names or dates). Use random phrases or patterns.

3. Credential Stuffing
- Attackers use previously leaked usernames and passwords from breaches to try on other sites.
- Tip: Use unique passwords for every account and enable MFA.

4. Rainbow Table Attack
- Attackers use precomputed hash databases of common passwords to reverse-engineer hashes.
- Mitigation: Use salted password hashing algorithms (e.g., bcrypt, Argon2) for storage.

5. Phishing Attack
- Tricks users into revealing passwords on fake websites or through fake messages.
- Tip: Always verify URLs, enable MFA, and never reuse passwords.

## How Password Complexity Affects Security
Password complexity refers to the mix of character variety, randomness, and length within a passowrd, directly impacts how resistant a 
password is to attacks.

| Factor            | Security Impact                               |
|-------------------|-----------------------------------------------|
| Length            | Stronger defenses against brute-force attacks |
| Character Variety | Increases unpredictability                    |
| Randomness        | Prevents dictionary-based attacks             |
| Uniqueness        | Reduces credential stuffing risks             |

## Repository Structure
Password-Strength-Analysis/
├─ README.md
└─  screenshots/
    ├─ PasswordMeter/
       ├─ P1.jpg – P10.jpg
    └─ NordPass/
       ├─ P1.jpg – P10.jpg
