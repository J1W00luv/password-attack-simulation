# Password Attack Simulation

## **Aim:**
To demonstrate how weak passwords can be exploited in a controlled environment, and what mitigation strategies could be used to protect users from password attacks.

## **Method:**
	1. Set up a controlled environment: Configure Kali Linux VM.
	2. Create vulnerabilities: Use Kali to create weaknesses.
	3. Exploit vulnerabilities: Use Kali to gain unauthorised access.
	4. Document & Evaluate: Identify mitigation strategies.

## **Execution:**
I started off by creating a user account ‘victim’ on my Kali machine that had a weak password. I then activated SSH on my host account to establish a connection. I used Hydra to perform a dictionary password attack on my local SSH server. I opened system logs to collect data about all the attempts Hydra will have at guessing the password. I then executed a command to do a brute force using a basic list of words/simple number combinations and successfully cracked the password in a short time.

## **Results:**
![Results in terminal](https://github.com/J1W00luv/password-attack-simulation/blob/main/screenshots/terminalResults.png)

## **Logs:**
![Logs in terminal](https://github.com/J1W00luv/password-attack-simulation/blob/main/screenshots/terminalLogs.png)
## **Evaluation:**
My attack was successful because the SSH service did not have a limit of log in attempts and password use for authentication. The password was in a common dictionary of words used for brute force attacks, and therefore was easily guessed. After gaining the password, I could easily log in with the right credentials into the account. To prevent this type of attack a couple of methods could be used, for example end-user education, so that people are not choosing simple combinations of characters as their passwords, or use SSH Key Authentication, as it is much more complex and cannot be guessed since it is a combination of characters with a huge length of 2048 or 4096 bits.

