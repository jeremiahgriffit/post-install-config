<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Configure osTicket, post-installation](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure system-wide settings (timezone, default email, site name)
- Set up helpdesk departments (e.g., IT Supportm Billing)
- Add and assign agents to departments
- Configure email fetching or piping (POP/IMAP or SMTP)
- Set up SLA (Service Level Agreement) plans
- Configure cron job for automated tasks (auto-ticket fetch, notifications)
- Install and enable optional plugins (e.g., LDAP Auth, Auto Assign)
- Customize email templates and autoresponders
- Test the system by submitting and resolving a test ticket

<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Upon successful installation of osTicket and removal of the setup directory, access the admin dashboard using the username and password that were set up during installation. This is your first step toward making the help desk work with your chosen settings.
The help desk has several basic settings that need to be configured upon installation: the system email address, the default department, the timezone settings. Once these settings are properly configured, automated responses and ticket notifications will be sent as expected.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then, establish departments—like "Technical Support" or "Billing"—by going to the Admin Panel and selecting Agents and then Departments. Place agents (staff members) in departments according to the assignments that work best for them.
Next, navigate to Admin Panel > Manage > SLA Plans to set up service level agreements that dictate response deadlines for tickets. This is crucial to prioritize urgent issues and ensure that we keep our customers happy.Test the default flow by submitting a ticket to ensure that email routing and agent notifications work as intended.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Finally, set up the email piping or fetching (POP/IMAP) to convert incoming support emails into tickets automatically. You can configure this under Email > Remote Mail Fetching. If you’re hosting the system yourself, ensure that a cron job is running to check for new incoming emails on a consistent basis (if you’re hosted on IIS, use Task Scheduler). You can also install and enable a number of different plugins, such as an LDAP plugin for authentication, or internal ticket filters to set up custom routing rules for your tickets. Overall, osTicket is a very flexible system to help you grow your help desk.
</p>
<br />
