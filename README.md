# Active Directory Lab

<h1>Create Active Directory Home Lab</h1>

<h2>YouTube Guide Demonstrations</h2>

 ### [By Josh Madakor](https://www.youtube.com/watch?v=MHsI8hJmggI&t=2874s)
 ### [By Jim Schultz](https://www.youtube.com/watch?v=aqA6bktFHoY&t=239s)
 ### [By East Charmer](https://www.youtube.com/watch?v=GsmJowwIh8Q)

<h2>Description</h2>
I am currently working on setting up a basic home lab environment running Active Directory using VMware Workstation on PC and VMware Fusion Pro on Mac M1 following the intructions in these 3 YouTube videos above. Configuring and running this lab will help me to understand how active directory and Windows nextworking works. I have been using Active Directory to access System Center Configuration Manager (SCCM) and Remote Dekstop at my currecnt workplace, but this will be my first time configuring the Active Directory by myself which I am very excited about it!  
<br />


<h2>Environments Used </h2>

- <b>Mac M1: Windows 11 Pro on VMware Fusion Pro</b> 
- <b>Windows PC: Windows Server 2022 on VMware Workstation</b> 

<p align="center">
 
<img width="1100" alt="AD mapping" src="https://github.com/user-attachments/assets/f4f44d7f-a263-45d6-96e6-db09e6295333" />

<h2>Program walk-through:</h2>
Install VMware Workstation on Windows PC and VMware Fusion Pro on Mac M1. 

<h2>Set up an AD domain on VMware Workstation on PC steps:</h2>
 1. Install Windows Server in a virtual machine and name the machine: AD-server-2022.

![Install Server 2022](https://github.com/user-attachments/assets/42fa1f7e-e076-4e21-a702-46375713c99d)

2. Installed Active Directory on DC-Server-2022. Promote the server to a Domain Controller (DC). 
![Create AD in server](https://github.com/user-attachments/assets/aef82d8d-db64-47f8-ac0b-6af59e76c29b)

3. Created an AD domain: DC.local. Restarted the virtual machine.
4. Created organizations Units (OUs) for different departments, mine are USA and Thailand.
   ![Create OU](https://github.com/user-attachments/assets/4b69bd57-413f-475c-81ea-b0abc10cdab9)
5. Created user accounts and groups within the OUs.
   ![Group in OU](https://github.com/user-attachments/assets/454673a4-feda-43e0-8d08-2fa74402289b)
   ![Groups in each OU](https://github.com/user-attachments/assets/b85435bc-7771-4806-8bf2-530dfc0f3aa6)
   ![Create new user](https://github.com/user-attachments/assets/909c0c50-58b5-402f-a844-ac2bae2971a7)



   

   




<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
