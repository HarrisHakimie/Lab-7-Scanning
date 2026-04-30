## Lab-7-Scanning
#TASK 7

Question 1: Analyse packet1.pcap and find the flag.

ANSWER :
<img width="1648" height="895" alt="TRY" src="https://github.com/user-attachments/assets/672b2cab-2577-409c-abaf-ffc13236277f" />
 
<img width="450" height="228" alt="Screenshot 2026-04-30 165103" src="https://github.com/user-attachments/assets/86933de4-bcd9-430d-93f5-640fb547be43" />

## Question 3: Interpret an Nmap Output
1. What can an attacker do with each port?
2. What vulnerabilities are likely present based on the version?
3. Which one is the highest risk and why?
4. What attack path can be built from this?
5. What should be the remediation?

## 1. What attacker can do
- Port 21 (FTP) Upload/download files Anonymous login attack
- Port 22 (SSH) Brute-force login Remote access
- Port 80 (HTTP) Website attacks (SQLi, XSS)
- Port 139 & 445 (SMB) File sharing access Exploit Windows vulnerabilities

## 2. Vulnerabilities
- vsftpd 2.3.4 Backdoor vulnerability (very famous)
- OpenSSH 5.3 Old version - possible brute-force & weak crypto
- Apache 2.2.8 Outdated - multiple CVEs (RCE, DoS)
- SMB (Windows 7 SP1) Vulnerable to EternalBlue (MS17-010)

## 3. Highest Risk
Port 445 (SMB)

- Remote code execution
- Wormable (spreads automatically)
- Used in ransomware (e.g. WannaCry)

## 4. Attack Path
Example attack chain:

1. Scan target (Nmap)
2. Exploit SMB (EternalBlue)
3. Gain shell access
4. Move laterally
5. Access FTP / Web data

## 6 Remediation
Disable unused ports
Update software
Patch Windows (MS17-010)
Use strong passwords
Firewall rules
