# LAB-7-SCANNING TASK 7

# Question 1 : Analyse Packet1.Pcap And Find The Flag.

## Answer Question 1 :

<img width="1648" height="895" alt="TRY" src="https://github.com/user-attachments/assets/672b2cab-2577-409c-abaf-ffc13236277f" />

 
<img width="450" height="228" alt="Screenshot 2026-04-30 165103" src="https://github.com/user-attachments/assets/86933de4-bcd9-430d-93f5-640fb547be43" />

# Question 2 : Analyse Packet2.Pcap And Find The Flag. 

## Answer Question 2


# Question 3 : Interpret An Nmap Output

1. What can an attacker do with each port?
2. What vulnerabilities are likely present based on the version?
3. Which one is the highest risk and why?
4. What attack path can be built from this?
5. What should be the remediation?

## Answer Question 3

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

## 5. Remediation
Disable unused ports
Update software
Patch Windows (MS17-010)
Use strong passwords
Firewall rules

# Question 4: Identify the OS (OS Fingerprinting) - TTL
Image 1
<img width="1150" height="405" alt="1" src="https://github.com/user-attachments/assets/a4e6200a-a04b-4823-96e0-2bf0ef7c3b03" />

## Answer Image 1 Question 4

Image
<img width="303" height="207" alt="2" src="https://github.com/user-attachments/assets/2ea35dfe-be94-441f-a2cf-a402f460220b" />

## Answer Image 2 Question 4

Image
<img width="847" height="195" alt="3" src="https://github.com/user-attachments/assets/5c469d44-fe27-4722-8f3f-b00dcec562e4" /> 

## Answer Image 3 Question 4

# Question 5: Analyse the Nessus file
Upload to your nessus (Network_Scan.nessus) and analyse the files. Focus on critical or high findings that was identifies in analysis named “Ghostcat”.

1.	What is the affected Port number
2.	What is the Affected protocol
3.	What is the CVSS Score of vulnerability found
4.	Can you find any exploit related to this vulnerability?
5.	Find CVE for this vulnerability. 

## Answer Question 5 :
