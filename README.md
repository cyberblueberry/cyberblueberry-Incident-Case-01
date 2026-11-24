# cyberblueberry-Incident-Case-01
Encrypted investigation responseSOC INCIDENT REPORT

Alert ID: SOC-2026-014

A workstation attempted 135 failed login attempts within 2 minutes from IP address 185.45.22.14.

Questions:
1. What type of cyber attack is shown? ANSWER : many logins attempt The scenario shows a brute-force attack (or password-spraying attack). In this type of cyber attack, an attacker uses automated software to rapidly guess different passwords until they find the right one to break into a user account or workstation.
 
2. What indicators make the activity suspicious? ANSWER:  The main suspicious indicator is the high number of failed logins in a very short time. Having 135 failed attempts within just 2 minutes is much faster than a normal human can type, which strongly points to an automated attack tool rather than a user simply mistyping their password. Additionally, repeated login failures coming from an external IP address (185.45.22.14) toward a workstation is unusual and a clear warning sign.

3. What immediate action should the SOC analyst perform? ANSWER: First, the SOC analyst should check the security logs to see if any of the login attempts from 185.45.22.14 actually succeeded. Next, the analyst should immediately block that IP address at the firewall to stop the attack from continuing, identify which user account was targeted, and escalate the ticket to Tier 2 if there is any sign that the workstation was compromised.

4. What severity level should be assigned? ANSWER: This incident should be assigned a Medium severity level. While a high-speed login attack is a serious threat, the impact remains contained as long as all 135 attempts failed and the IP is blocked. However, if the logs show that a login succeeded or a privileged admin account was targeted, the severity should immediately be raised to High.

5. Give one recommendation to prevent this attack. ANSWER: The best way to prevent this attack is to enforce Multi-Factor Authentication (MFA) along with an account lockout policy. MFA ensures that even if an attacker guesses the correct password, they still cannot log in without the second verification step, while account lockouts automatically stop automated guessing after a few failed tries. 
