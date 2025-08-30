<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Dealing with Account Lockouts</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Steps to Unlock Accounts</h2>

In order for accounts to be locked out of access after multiple failed attempts, do the following<br />
Configure Group Policy to Lockout the account after 5 attempts:
<img width="931" height="705" alt="image" src="https://github.com/user-attachments/assets/6a2f953c-e66b-4cc2-8768-0fb0ec9360cb" />



After attemptting to log in with a bad password this will appear

<img width="441" height="474" alt="image" src="https://github.com/user-attachments/assets/1d698c8e-d78b-4687-805b-04dffaf95a05" />



After 5 failed failed login attempts, they should be locked out

<img width="551" height="139" alt="image" src="https://github.com/user-attachments/assets/e9aa3564-3b87-47eb-ade6-ce3284e7d8af" />


To unlock the User, go to Active Directory Users & Controls, then 
- Right Click on mydomain.com
- Click on Find and search for the locked out user
<img width="412" height="521" alt="Screenshot 2025-08-30 143547" src="https://github.com/user-attachments/assets/f11a6d4e-2ae8-42a8-8fa2-07f113519f1f" />

<img width="523" height="574" alt="image" src="https://github.com/user-attachments/assets/39a6dc21-8b5b-4865-a5bf-53511ecb35f2" />


Click on Properties then go the Account tab
Click on the Unlock the account button and Apply 

<img width="402" height="533" alt="image" src="https://github.com/user-attachments/assets/8dd1c586-aec0-4662-bfb7-e792d6ee7a00" />

The user can now log back in using their previous credentials, if they wish to change password, right click on the user and click on Reset Password and change accordingly
Reset the password

<img width="523" height="574" alt="image" src="https://github.com/user-attachments/assets/39a6dc21-8b5b-4865-a5bf-53511ecb35f2" />

This now concludes how to unlock accounts.
