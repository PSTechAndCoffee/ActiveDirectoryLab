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

3. Create an AD domain: DC.local. Restart the virtual machine.
4. Create organizations Units (OUs) for different departments, mine are USA and Thailand.
   ![Create OU](https://github.com/user-attachments/assets/4b69bd57-413f-475c-81ea-b0abc10cdab9)
5. Create user accounts and groups within the OUs.
   ![Group in OU](https://github.com/user-attachments/assets/454673a4-feda-43e0-8d08-2fa74402289b)
   ![Groups in each OU](https://github.com/user-attachments/assets/b85435bc-7771-4806-8bf2-530dfc0f3aa6)
   ![Create new user](https://github.com/user-attachments/assets/909c0c50-58b5-402f-a844-ac2bae2971a7)

<h2>Create a VM for Winodws 11 Pro on VMware Fusion:</h2>
Create a new virtual machine: PC1 and install Windows 11 Pro that comes with VMware Fusion. Let it run and restart.

<img width="1390" alt="Create VM with Win11" src="https://github.com/user-attachments/assets/c15cfbb5-e8c3-4f8e-993f-7f958f41d0eb" />

<h2>Join PC1 Client to a Domain Controller steps:</h2>
1. Before joining PC1 client to domain DC.local. First, I need to make sure both VMs, DC and PC1, are on the same connection settings. In my situation, NAT connection did not work because both VMs could not find or ping each other. So, I had to change connection on both VMs to Bridged connection. This is under VM settings> Network Adapter.

2. Once both VMs are set to be on Bridged connection. Go back to DC and set the network connection to be static network and use the IP address and subnet mask from ipconfig in cmd.
 
![ipconfig on server DC](https://github.com/user-attachments/assets/86602855-183e-4e6f-af00-069d18d5dca2)

![IP address DC](https://github.com/user-attachments/assets/54158366-0efa-46a1-844f-670b6d814c31)

3. Configure PC1 client's connection to use DHCP but set its DNS to be the same with DC's IP address.
   
<img width="877" alt="Screenshot 2025-02-17 at 1 46 29 PM" src="https://github.com/user-attachments/assets/f4c96aa4-b4b0-4c77-8629-73b306ad94ca" />

4. Make sure I can ping DC from PC1 or can ping PC1 from DC. Then, PC1 should be ready to join DC.local.
   
5. On PC1 client, under System Properties, join domain: DC.local. Enter account that will have permission to join domain, which is Administrator. Click ok and restart VM.
   
<img width="1440" alt="Screenshot 2025-02-17 at 12 59 08 PM" src="https://github.com/user-attachments/assets/68756566-43ab-4b13-b21c-ce17ae9d18b3" />

6. PC1 joined DC.local. Now I should be able to sign in with an account that I created in DC.local.
 
<img width="1406" alt="Screenshot 2025-02-17 at 2 00 17 PM" src="https://github.com/user-attachments/assets/803144ec-4341-4222-97ae-e8188775bee1" />

<img width="1426" alt="Screenshot 2025-02-17 at 1 40 20 PM" src="https://github.com/user-attachments/assets/4e3dd869-9b1f-4969-86d2-a79cf129ed59" />




   

   




<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
