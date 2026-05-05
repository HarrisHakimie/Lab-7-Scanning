# LAB-7-SCANNING TASK 7

# Question 1 : Analyse Packet1.Pcap And Find The Flag.

## Answer Question 1 :

<img width="1648" height="895" alt="TRY" src="https://github.com/user-attachments/assets/672b2cab-2577-409c-abaf-ffc13236277f" />

 
<img width="450" height="228" alt="Screenshot 2026-04-30 165103" src="https://github.com/user-attachments/assets/86933de4-bcd9-430d-93f5-640fb547be43" />

# Question 2 : Analyse Packet2.Pcap And Find The Flag. 

## Answer Question 2

<img width="1647" height="821" alt="Screenshot 2026-05-05 145641" src="https://github.com/user-attachments/assets/3e99d860-cab2-4c80-9549-5e0fc7dbb033" />

<img width="1214" height="546" alt="Screenshot 2026-05-05 145719" src="https://github.com/user-attachments/assets/9ef55db2-3bf2-496b-8d3e-9439e3ca1b5e" />

<img width="597" height="718" alt="Screenshot 2026-05-05 145753" src="https://github.com/user-attachments/assets/37d55a5f-ab9a-4cba-a15b-e71c02ee85ff" />

<img width="754" height="751" alt="Screenshot 2026-05-05 145807" src="https://github.com/user-attachments/assets/d74d38c2-19cb-4b03-ae15-a3a171f7afd1" />

<img width="756" height="238" alt="Screenshot 2026-05-05 145823" src="https://github.com/user-attachments/assets/9da71fc4-21d5-48dd-a8fd-fe810bd82447" />

<img width="754" height="602" alt="Screenshot 2026-05-05 145844" src="https://github.com/user-attachments/assets/42ef21f8-0a3d-4028-ae66-a5e916521e43" />


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

1. Disable unused ports
2. Update software
3. Patch Windows (MS17-010)
4. Use strong passwords
5. Firewall rules

# Question 4: Identify the OS (OS Fingerprinting) - TTL
The TTL value observed is 128, which indicates the system is likely running Windows OS.

Image 1
<img width="1150" height="405" alt="1" src="https://github.com/user-attachments/assets/a4e6200a-a04b-4823-96e0-2bf0ef7c3b03" />

## Answer Image 1 : TTL 64 = Linux

Image
<img width="303" height="207" alt="2" src="https://github.com/user-attachments/assets/2ea35dfe-be94-441f-a2cf-a402f460220b" />

## Answer Image 2 : TTL 128 = Windows.

Image
<img width="847" height="195" alt="3" src="https://github.com/user-attachments/assets/5c469d44-fe27-4722-8f3f-b00dcec562e4" /> 

## Answer Image 3 : TTL 128 = Windows.

# Question 5: Analyse the Nessus file

<img width="1919" height="890" alt="image" src="https://github.com/user-attachments/assets/c4988877-3274-478f-a6de-4495ff3921b0" />

<img width="1916" height="884" alt="image" src="https://github.com/user-attachments/assets/e33575c0-9aef-4ed6-a16c-08137b145795" /> 

<img width="1600" height="738" alt="WhatsApp Image 2026-05-01 at 2 03 03 AM" src="https://github.com/user-attachments/assets/8cc2225a-8e29-4cb0-b3ae-64a7d79850c1" />

<img width="1637" height="712" alt="Screenshot 2026-05-05 144831" src="https://github.com/user-attachments/assets/34d7a12a-93ce-4633-9a89-22b524ef745a" /> 

# Answer 

1.	What is the affected Port number
   - Answer: 8009
  	
2.	What is the Affected protocol
   - Answer: Apache JServ Protocol
  	
3.	What is the CVSS Score of vulnerability found
   - Answer: 9.8 (Critical)
     
4.	Can you find any exploit related to this vulnerability?
   - Answer: Yes, attackers can read sensitive files and potentially execute remote code.
      
5.	Find CVE for this vulnerability.
   - Answer: CVE-2020-1938

