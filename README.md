# osTicket Post Installation Configuration

## Environments and Technologies Used

- Microsoft Azure
- Virtual Machines
- osTicket

## Operating Systems Used 

- Windows 10 Pro, version 22H2 - x64 Gen2

## Configuration Steps

1. Configure Roles
2. Configure Departments
3. Configure Teams
4. Configure Agents
5. Configure Users
6. Configure SLA (Service Level Agreement)
7. Configure Help Topics


### Login to the agent portal

Username: LabADMIN
Password: osTicketPassword123!

http://localhost/osTicket/scp/login.php

Click on admin panel on the top right 

![image](https://github.com/user-attachments/assets/c6355bcc-14ae-4b2c-a16d-31fcb8ced5bf)

### Configure Roles

We will configue a role of "Super User" to gain an understanding about how roles work in osTicket

Navigate to Agents > roles > Add New Role

![image](https://github.com/user-attachments/assets/6c990541-f440-4b03-a683-6f26657c5b5d)

Name the new role  `Super User` then navitage to the "Permissions tab" and select all boxes in Tickets, Tasks, Knowledgebase  

Take note of some of the permissons we can assign to roles

#### Tickets Permissions    

![image](https://github.com/user-attachments/assets/baf21f62-c83d-413a-bee9-341ccd99e944)

#### Tasks Permissions  

![image](https://github.com/user-attachments/assets/0380a834-13e5-4969-8b6e-fe0773f844a6)

#### Knowledgebase Permissions  

![image](https://github.com/user-attachments/assets/6dd4f0c6-36fe-4ba0-95ec-ba8ff2629b99)

After we enabled all permissions click "Add Role"

We should see the role "Super-User" in the updated roles table: 

![image](https://github.com/user-attachments/assets/8a67466b-b732-4ae2-8019-67e98477b0f9)


### Configure Departments

The Purpose of departments in osTicket is mainly for ticket "visibility" for example:  
- The "Networking Department" would get assigned network related tickets  
- The "Support Department" Would get assigned tickets like password resets as an example.   

These departments would get assigned tickets that pertain to their department and wouldn't see tickets that are irrelevant 

Lets now create a "SysAdmins" Department

 Navigate to Agents > Departments > click on "Add New Department"

![image](https://github.com/user-attachments/assets/90d97d32-485d-48f2-84b1-2eadf09d20aa)

Lets now create a "SysAdmins" Department

Choose Top-Level Department and name it `SysAdmins` Thats all the configuration for now. click "Create Dept"

![image](https://github.com/user-attachments/assets/64d557f8-0f87-4fb4-a29b-3431560f8e91)

We should see the Department "SysAdmins" in the updated Department table: 

![image](https://github.com/user-attachments/assets/2c877bc2-e850-44a4-87ae-52cb6f49e709)

### Configure Teams

Teams can combine users from multiple departments together 

We will create an "Online Banking" team 

Navigate to  Agents > Teams > click on "Add New Team"

![image](https://github.com/user-attachments/assets/fff5add8-9e7f-4f46-b540-cd579dc8c43b)

Name it "Online Banking" and click Create

![image](https://github.com/user-attachments/assets/a24ebe81-a44a-4f5e-8869-89d9b0ca602d)


### Configure Agents

Agents are other workers who can view and work tickets

Navigate to Agents > Add New

![image](https://github.com/user-attachments/assets/d1c5b74b-4cad-4f08-8b3d-a8c04a2e8535)

Create user Jane Doe

![image](https://github.com/user-attachments/assets/a25f1e35-a56b-4f16-b0f1-c5a7c0a7c260)

![image](https://github.com/user-attachments/assets/c1c136a5-f319-4326-bf82-949b8bbdd148)

![image](https://github.com/user-attachments/assets/7dc54910-470f-4afa-b958-01bd79009a23)

Set Jane Doe's password

Navigate to Agents > Agents > Select Jane doe

![image](https://github.com/user-attachments/assets/13bd1d92-df61-459e-aec4-431f9bf6b79a)

Click set password > Set password to: `osTicketPassword123!`

![image](https://github.com/user-attachments/assets/3765d0db-ef54-4af0-a11e-aa0f6bf59228)


Create user John Doe

Repeat the same steps as above however this time assign this user to the support department with view only privlages 

![image](https://github.com/user-attachments/assets/4ff951ba-743e-4a9c-b901-5c82f06c93f0)

![image](https://github.com/user-attachments/assets/2bd3abbc-cfd1-44a2-a6eb-1317536299b0)

Set John Doe's password

Navigate to Agents > Agents > Select John Doe

![image](https://github.com/user-attachments/assets/48ef21de-34a3-4f44-beab-8706c8770548)

Click set password > Set password to: `osTicketPassword123!`

![image](https://github.com/user-attachments/assets/20b70377-78dc-450d-afff-c0348abcf4af)


The updated agent table should look like this after creating Jane and John

![image](https://github.com/user-attachments/assets/4d28bf61-0ae2-48e0-b637-d02699645859)

### Configure Users

Now we will add end users who can submit tickets

*On the agent panel* Navigate to Users > Add New

![image](https://github.com/user-attachments/assets/0abce924-c715-4c73-a47c-6f0e56ce9e1f)

Create user named karen then click add user

![image](https://github.com/user-attachments/assets/f24c470a-5b38-49ea-bbb6-01a8bad356ad)


### Configure SLA (Service Level Agreement)

*On the admin panel* Navigate to  Manage > SLA > click "Add New SLA Plan"

![image](https://github.com/user-attachments/assets/e37e7f84-551a-439e-8dae-e5b2cff793fc)


We will be setting 3 severity level SLAs
- Sev-A (Grace Period: 1 hour, Schedule: 24/7) -- Major Problems that must be addressed ASAP
- Sev-B (Grace Period: 4 hours, Schedule: 24/7) -- Problems that must be addressed relatively quickly 
- Sev-C (Grace Period: 8 hours, Business Hours) -- Normal Problems 

#### Setting Sev-A

Name: `Sev-A`  
Grace Period: `1`  
Schedule: 24/7  
Click > "Add Plan"
![image](https://github.com/user-attachments/assets/29403359-682f-4298-bc1f-0f49b4b5a201)


#### Setting Sev-B

Name: `Sev-B`  
Grace Period: `4`  
Schedule: 24/7     
Click > "Add Plan"  
![image](https://github.com/user-attachments/assets/7877d514-912a-4624-807c-a40ce66cccd0)


#### Setting Sev-C

Name: `Sev-A`  
Grace Period: `8`  
Schedule: `Monday - Friday 8am - 5pm with U.S. Holidays`   
Click > "Add Plan"  
![image](https://github.com/user-attachments/assets/3dd72ee0-101e-403b-8cc5-b4b5e13d9da2)



### Configure Help Topics

Now we will add the following help topics:
- Business Critical Outage
- Personal Computer Issues
- Equipment Request
- Password Reset


Navigate to Manage > Help Topics > "Add New Help Topic"  

![image](https://github.com/user-attachments/assets/a606eacc-d66f-4cbc-b88b-7b1316b4f210)

![image](https://github.com/user-attachments/assets/3bdaa11f-133e-409b-87c2-9529227f2820)

Contine to add all the topics

Once done it should look like this: 
![image](https://github.com/user-attachments/assets/f78e2444-89e8-4e4c-936e-a76cdeb27772)


Thats it for this lab! We have concluded our inital setup for osTicket

## Next steps

[osTicket: Creating and Working Tickets](https://github.com/jeremiahgriffit/osTicket-Creating-and-Working-Tickets/tree/main)




