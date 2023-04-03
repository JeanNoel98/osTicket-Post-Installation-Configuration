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
- OSTicket

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
<img src="https://i.imgur.com/CR0pztl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

From here we can fill out the  Department Information:<br />
We can refrence the forum:
[osTicket Documents](https://docs.osticket.com/en/latest/Admin/Agents/Departments.html) 
to see what each field means and what it does and fill in the appropriate information.
after we're done select “Create Dept” to finish
</p>
<br />

<p>
<img src="https://i.imgur.com/iae6Jya.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Teams allow you to pull Agents from different Departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter.<br />
Having Agents from different Departments assigned to a Team will supersede the parameters of the Agents’ Department rules.<br /> <br /> For example, you can create a Help Topic associated with a particular product you produce, and assign it to a Team of specialist Agents from different Departments.<br />
To create a Team in your Admin Panel Begin by selecting the agents tab and click on Teams-> “add new Team”
</p>
<br />

<p>
<img src="https://i.imgur.com/zM6iZVz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From there you can fill out the appropriate information in both the “team” section and the “members” section and select “create team when you are finished.
</p>
<br />

<p>
<img src="https://i.imgur.com/X36gdL8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we will configure our settings to make sure we allow anyone to create tickets without having to register by going to the admin panel selecting the settings tab and navagating to the user section and masking sure the “Registration Required:” box is not ticked and “Registration Method:” is set to Public
</p>
<br />

<p>
<img src="https://i.imgur.com/vbnQxlh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we will be adding agents, start by ensuring you are in the admin Panel then by going into the Agents Tab and selecting Agents -> “add new agent”
</p>
<br />

<p>
<img src="https://i.imgur.com/IQxVvjE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/t7ox3CE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/7VI5suo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Agents are given access to the help desk with the intent to respond and resolve the tickets. When adding an Agent to the help desk, they will need to be assigned to a Primary Department and given a Primary Role for the Tickets/Tasks routed to that department. <br /> Agents can be given Extended Access to additional departments of the help desk as well as assigned different Roles to those departments; this can be configured in the Access tab of the Agent’s Profile.
</p>
<br />

<p>
<img src="https://i.imgur.com/fm4N9HJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You can then fill out the appropriate information in all sections and select “create” when you are finished.
</p>
<br />

<p>
<img src="https://i.imgur.com/6iCedmA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we will add users Users are the ticket owners of the tickets in the help desk. When a ticket is created in the help desk, the user is associated with their email address in the User Directory of the help desk. Users can be added or deleted from the User Directory of the help desk at any time. Please note, if the user is deleted the tickets of the user must also be deleted.<br /> To add a user we will first make sure we are in the Agent Panel then we will navigate to the Users tab and select user directory -> add new user
</p>
<br />

<p>
<img src="https://i.imgur.com/FXpg3ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You can then fill in the appropriate information and select “add user”
</p>
<br />

<p>
<img src="https://i.imgur.com/uZKvp80.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The final process we will go through in this post-installation setup of OS Ticketing system is creating Help topics</p>

for this you will need to make sure you are in the Admin Panel and you will go to the Manage tab and select Help topics-> “Add new help topic”
</p>
<br />

<p>
<img src="https://i.imgur.com/9pIfL5Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/SDk5wdn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You can fill in the appropriate Titles and information in all the tabs under add new help topic and click “add topic” to finish!

</p>
<br />

