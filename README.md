# osTicket-Post-Installation-Configuration
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

- Configure Roles
- Configure Departments
- Configure Teams
- Configure Agents (workers)
- Configure Users (customers)
- Configure SLA
- Configure Help Topics

<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/fnp9330.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Roles are the permissions granted to Agents per Department that they have access to. Each Role has a set of permissions that can be checked/unchecked for agents given that Role in association with a Department they have access to. An unlimited number of roles can be created and assigned to Agents with access to various departments.
  
To create roles you will first need to log in as an admin into OSticket, from there ensure you are in the admin Panel and you will select Agents -> roles
</p>
<br />

<p>
<img src="https://i.imgur.com/B1Bt5MK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/tgJUkmE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/H9H3UAu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the Definition tab you will name the role and add any internal notes you deem necessary. For our example we will be creating a supreme admin account so in the Permissions tab select all of the abilities in “ticket” “tasks” “Knowledgeable”

After you have selected all desired permissions you can then select add role and you will see the new role added.

</p>
<br />

<p>
<img src="https://i.imgur.com/3q0Jrpm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After that we will create a new SLA Plan or Service Level Agreements, these are unlimited in osTicket. The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed.

We will navigate to the Manage tab and select SLA -> Add New SLA
</p>
<br />

<p>
<img src="https://i.imgur.com/4E5u53r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From there we can create a Plan name to be selected when assigning In the Name field then filling in the rest of the filed to your specified desire: 
  
**Grace Period:** Amount, in hours, before tickets with this SLA will become overdue if not closed in allotted time.
  
**Status:** Choose Active or Disable for the plan.
  
**Transient:** SLA can be overridden on ticket transfer or help topic change; if not transient, the SLA will remain the same as it is assigned on ticket creation.
  
**Ticket Overdue Alerts:** This will DISABLE overdue alert notices to staff for tickets assigned this SLA.
</p>
<br />

<p>
<img src="https://i.imgur.com/PKuutgk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After that we can select “Add Plan” to see our new SLA plan added to our list
</p>
<br />

<p>
<img src="https://i.imgur.com/kCQtjDk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Since tickets are routed through Departments in the help desk Next we will create departments 

Start by making sure you are in the admin panel, select the agents tab and click on Departments-> “add new Department”
</p>
<br />

<p>
<img src="https://i.imgur.com/7ZfGiMl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From here we can fill out the  Department Information:
**Parent:** If nesting departments, this is the Parent Department to nest the department under. Please note: If an agent has access to the Parent Department, they will see the tickets of nested or child departments also, but access does not extend from child departments to Parent Departments.
  
**Status:** The status of the department will determine its visibility as well as if tickets can be routed to that department. 
  
**Active:** The department is available when transferring tickets.
  
**Archived:** The department is no longer in use and cannot be selected to transfer any ticket. Also, if tickets in that department are reopened via an End-User response it will create a new ticket referencing the original ticket number and subject line but the department will be the system default.
  
**Disabled:** Tickets can no longer be transferred to this department and any tickets set up to be auto routed to this department will now be routed to the default department in the Helpdesk. Closed tickets in this department will reopen if the End-User responds.
  
**Name:** Department name as it will be displayed throughout the helpdesk.
  
**Type: **Select Private if you wish to mask assignments to this Department in the Client Portal. Additionally, when labeled as Private, the Department Signature will not be displayed in email replies. At least one department of the help desk must be Public.
  
**SLA:** Service Level Agreement for tickets routed to this Department. This the expected amount of time (in hours) that a ticket is expected to be closed once opened. If the ticket is not closed in the allotted amount of time, it will then be Overdue.
  
**Schedule:** Schedule is used by the Service Level Agreement when rendering tickets routed to this Department. This setting takes precedence over System and SLA schedule settings.
  
**Manager:** Electively, select a Manager for the departments of the help desk. Managers can be configured to receive special alerts.
  
**Ticket Assignment:** Enable this to restrict ticket assignment to include only members of this Department. Department membership can be extended to based on Agent’s Department Access, if Alerts & Notices Recipients includes those with department access.<br />
**Claim on Response:** Check this to disable auto-claim on response/reply for this department. Agents can still manually claim unassigned tickets.<br />
**Reopen Auto Assignment:** Check this to disable auto-assignment of reopened tickets for this department. Otherwise, the Ticket will be auto assigned to the last responding Agent.
  
Outgoing Email Settings:
  
Outgoing Email: Email Address used when responses are sent to Users when Agents post Responses to Tickets.
  
Template Set: Email Template Set used for Auto-Responses and Alerts & Notices for tickets routed to this Department. Template sets can be cloned and edited for department use in the Admin Panel > Emails > Templates.
  
Auto Responder Settings: This allows you to override the global Autoresponder settings for this Department.
  
New Ticket: If checked, this will disable the New Ticket Auto-Response sent to the User when a new ticket is created and routed to this Department.
  
New Message: If checked, this will disable the Auto-Response sent to the User to confirm a newly-posted message for tickets in this Department.
  
Auto-Response Email: Select an email address from which Auto-Responses are sent for this Department; this email would send only auto-response messages, not Agent responses.

And select “Create Dept” when we’re finished 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
