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

- Configure Roles, Departments, and Teams
- Configure User Registration Settings
- Configure Agents (Workers) and Users (Customers)
- Configure SLA Plans (Sev-A, Sev-B, Sev-C)
- Configure Help Topics for Ticket Submission

<h2>Login URLs</h2>

- **Admin/Analyst Login Page:** http://localhost/osTicket/scp/login.php
- **End Users osTicket URL:** http://localhost/osTicket

<h2>Configuration Steps</h2>

---

<h3>Step 1: Agent Panel vs. Admin Panel</h3>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Agent Panel vs Admin Panel"/>
</p>
<p>
Before configuring osTicket, it is important to understand the difference between the Admin Panel and the Agent Panel. The Admin Panel is used to manage system-wide settings such as roles, departments, SLA plans, and help topics. The Agent Panel is where help desk staff (agents) manage and respond to tickets. You can switch between panels using the toggle link in the top-right corner of the osTicket interface.
</p>
<br />

---

<h3>Step 2: Configure Roles</h3>

**Path:** Admin Panel -> Agents -> Roles

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Configure Roles"/>
</p>
<p>
Roles are used to group and assign permissions to agents within departments. In this configuration, a role called <strong>Supreme Admin</strong> was created with full access to all ticketing functions and system settings. This role allows the assigned agent to manage all aspects of the help desk environment.
</p>
<br />

---

<h3>Step 3: Configure Departments</h3>

**Path:** Admin Panel -> Agents -> Departments

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Configure Departments"/>
</p>
<p>
Departments control ticket visibility and help route tickets to the correct team. A department called <strong>SysAdmins</strong> was created to handle system-level and elevated support requests. Departments can be configured to separate Help Desk, SysAdmins, and Networking teams, ensuring tickets are handled by the appropriate group.
</p>
<br />

---

<h3>Step 4: Configure Teams</h3>

**Path:** Admin Panel -> Agents -> Teams

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Configure Teams"/>
</p>
<p>
Teams allow agents from different departments to be pulled together to handle specific issues or projects. A team called <strong>Online Banking</strong> was created to support cross-departmental collaboration on banking-related escalations and critical requests.
</p>
<br />

---

<h3>Step 5: User Registration Settings</h3>

**Path:** Admin Panel -> Settings -> User Settings

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="User Registration Settings"/>
</p>
<p>
To control who can submit tickets, the setting <strong>"Unregistered users can create tickets"</strong> was unchecked. Registration is now required — users must create an account and log in before they are able to submit a support ticket. This helps maintain accountability and reduces spam or anonymous ticket submissions.
</p>
<br />

---

<h3>Step 6: Configure Agents (Workers)</h3>

**Path:** Admin Panel -> Agents -> Add New

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Configure Agents"/>
</p>
<p>
Agents are the help desk staff responsible for managing and resolving tickets. Two agents were added in this configuration: <strong>Jane</strong>, assigned to the SysAdmins department, and <strong>John</strong>, assigned to the Support department. Each agent was given appropriate role permissions based on their department.
</p>
<br />

---

<h3>Step 7: Configure Users (Customers)</h3>

**Path:** Agent Panel -> Users -> Add New

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Configure Users"/>
</p>
<p>
Users are the end customers who submit support tickets through the osTicket portal. Two users were created for this lab: <strong>Karen</strong> and <strong>Ken</strong>. These accounts simulate real-world customers who interact with the help desk by submitting and tracking their support requests.
</p>
<br />

---

<h3>Step 8: Configure SLA Plans</h3>

**Path:** Admin Panel -> Manage -> SLA

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Configure SLA Plans"/>
</p>
<p>
SLA (Service Level Agreement) plans define the expected timeframe for ticket resolution based on severity. Three SLA plans were configured:<br /><br />
- <strong>Sev-A</strong> – Grace Period: 1 hour | Schedule: 24/7 (Critical outages, highest priority)<br />
- <strong>Sev-B</strong> – Grace Period: 4 hours | Schedule: 24/7 (High priority, around-the-clock coverage)<br />
- <strong>Sev-C</strong> – Grace Period: 8 hours | Schedule: Business Hours (Low priority, standard requests)<br /><br />
These SLA plans ensure tickets are escalated and resolved within appropriate timeframes based on their impact and urgency.
</p>
<br />

---

<h3>Step 9: Configure Help Topics</h3>

**Path:** Admin Panel -> Manage -> Help Topics

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Configure Help Topics"/>
</p>
<p>
Help Topics guide users when submitting a ticket by allowing them to categorize their issue. The following help topics were created to cover common support scenarios:<br /><br />
- Business Critical Outage<br />
- Personal Computer Issues<br />
- Equipment Request<br />
- Password Reset<br />
- Other<br /><br />
These categories help route tickets to the correct department and agent while also making it easier to track recurring issues across the organization.
</p>
<br />
