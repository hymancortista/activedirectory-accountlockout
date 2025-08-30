<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Deployment and Configuration Steps</h2>

Dealing with Account Lockouts
Get logged into dc-1
Pick a random user account you created previously
Attempt to log in with it 10 times with a bad password
<img width="441" height="474" alt="image" src="https://github.com/user-attachments/assets/1d698c8e-d78b-4687-805b-04dffaf95a05" />


Configure Group Policy to Lockout the account after 5 attempts:
How To Configure Account Lockout Threshold in Group Policy
<img width="931" height="705" alt="image" src="https://github.com/user-attachments/assets/6a2f953c-e66b-4cc2-8768-0fb0ec9360cb" />


Attempt to log in with it 6 times with a bad password
<img width="551" height="139" alt="image" src="https://github.com/user-attachments/assets/e9aa3564-3b87-47eb-ade6-ce3284e7d8af" />


Observe that the account has been locked out within Active Directory
<img width="412" height="521" alt="Screenshot 2025-08-30 143547" src="https://github.com/user-attachments/assets/f11a6d4e-2ae8-42a8-8fa2-07f113519f1f" />

Unlock the account
<img width="402" height="533" alt="image" src="https://github.com/user-attachments/assets/8dd1c586-aec0-4662-bfb7-e792d6ee7a00" />

Reset the password
<img width="523" height="574" alt="image" src="https://github.com/user-attachments/assets/39a6dc21-8b5b-4865-a5bf-53511ecb35f2" />

Attempt to login with it

Enabling and Disabling Accounts
Disable the same account in Active Directory
Attempt to login with it, observe the error message
Re-enable the account and attempt to login with it.

Observing Logs
Observe the logs in the Domain Controller
Observe the logs on the client Machine
Precursor to cybersecurity and security operations: joshmadakor.tech/cyber
