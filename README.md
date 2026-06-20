<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 11</b> (25h2)

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

<table>
  <tr>
    <td><img src="https://i.imgur.com/bnnEXTW.png" width="100%" alt="Admin Panel View"/></td>
    <td><img src="https://i.imgur.com/5iqeMTr.png" width="100%" alt="Agent Panel View"/></td>
  </tr>
  <tr>
    <td align="center"><em>Admin Panel</em></td>
    <td align="center"><em>Agent Panel</em></td>
  </tr>
</table>
<p>
Before configuring osTicket, it is important to understand the difference between the Admin Panel and the Agent Panel. The Admin Panel is used to manage system-wide settings such as roles, departments, SLA plans, and help topics. The Agent Panel is where help desk staff (agents) manage and respond to tickets. You can switch between panels using the toggle link in the top-right corner of the osTicket interface.
</p>
<br />

---

<h3>Step 2: Configure Roles</h3>

**Path:** Admin Panel -> Agents -> Roles

<table>
  <tr>
    <td><img src="https://i.imgur.com/vmfQyzk.png" width="100%" alt="Roles List Page"/></td>
    <td><img src="https://i.imgur.com/GFNyBv6.png" width="100%" alt="Supreme Admin Permissions"/></td>
  </tr>
  <tr>
    <td align="center"><em>Roles List Page</em></td>
    <td align="center"><em>Supreme Admin – Permissions Tab</em></td>
  </tr>
</table>
<p>
Roles are used to group and assign permissions to agents within departments. In this configuration, a role called <strong>Supreme Admin</strong> was created with full access to all ticketing functions and system settings. This role allows the assigned agent to manage all aspects of the help desk environment.
</p>
<br />

---

<h3>Step 3: Configure Departments</h3>

**Path:** Admin Panel -> Agents -> Departments

<table>
  <tr>
    <td><img src="https://i.imgur.com/V5OuMBt.png width="100%" alt="Departments List Page"/></td>
    <td><img src="https://i.imgur.com/4Pmn1xz.png" width="100%" alt="SysAdmins Department Settings"/></td>
  </tr>
  <tr>
    <td align="center"><em>Departments List Page</em></td>
    <td align="center"><em>SysAdmins Department Settings</em></td>
  </tr>
</table>
<p>
Departments control ticket visibility and help route tickets to the correct team. A department called <strong>SysAdmins</strong> was created to handle system-level and elevated support requests. Departments can be configured to separate Help Desk, SysAdmins, and Networking teams, ensuring tickets are handled by the appropriate group.
</p>
<br />

---

<h3>Step 4: Configure Teams</h3>

**Path:** Admin Panel -> Agents -> Teams

<table>
  <tr>
    <td><img src="https://i.imgur.com/E50VfKV.png" width="100%" alt="Teams List Page"/></td>
    <td><img src="https://i.imgur.com/Od5j5oP.png" width="100%" alt="Online Banking Team Members"/></td>
  </tr>
  <tr>
    <td align="center"><em>Teams List Page</em></td>
    <td align="center"><em>Online Banking Team – Members Tab</em></td>
  </tr>
</table>
<p>
Teams allow agents from different departments to be pulled together to handle specific issues or projects. A team called <strong>Online Banking</strong> was created to support cross-departmental collaboration on banking-related escalations and critical requests.
</p>
<br />

---

<h3>Step 5: User Registration Settings</h3>

**Path:** Admin Panel -> Settings -> User Settings

<table>
  <tr>
    <td><img src="https://i.imgur.com/JhpnXwg.png" width="100%" alt="User Settings Page"/></td>
    <td><img src="https://i.imgur.com/aKCxjVA.png" width="100%" alt="Registration Required Setting Unchecked"/></td>
  </tr>
  <tr>
    <td align="center"><em>User Settings Page</em></td>
    <td align="center"><em>Unregistered users unchecked – Registration Required</em></td>
  </tr>
</table>
<p>
To control who can submit tickets, the setting <strong>"Unregistered users can create tickets"</strong> was unchecked. Registration is now required — users must create an account and log in before they are able to submit a support ticket. This helps maintain accountability and reduces spam or anonymous ticket submissions.
</p>
<br />

---

<h3>Step 6: Configure Agents (Workers)</h3>

**Path:** Admin Panel -> Agents -> Add New

<table>
  <tr>
    <td><img src="https://i.imgur.com/0JUc4JB.png" width="100%" alt="Agents List – Jane and John"/></td>
    <td><img src="https://i.imgur.com/gLt3Pq9.png" width="100%" alt="Agent Profile – Department Assignment"/></td>
  </tr>
  <tr>
    <td align="center"><em>Agents List – Jane &amp; John</em></td>
    <td align="center"><em>Agent Profile – Department Assignment</em></td>
  </tr>
</table>
<p>
Agents are the help desk staff responsible for managing and resolving tickets. Two agents were added in this configuration: <strong>Jane</strong>, assigned to the SysAdmins department, and <strong>John</strong>, assigned to the Support department. Each agent was given appropriate role permissions based on their department.
</p>
<br />

---

<h3>Step 7: Configure Users (Customers)</h3>

**Path:** Agent Panel -> Users -> Add New

<table>
  <tr>
    <td><img src="https://i.imgur.com/HZvQ4cD.png" width="100%" alt="User Directory – Karen and Ken"/></td>
    <td><img src="https://i.imgur.com/PrieHnN.png" width="100%" alt="User Profile Page"/></td>
  </tr>
  <tr>
    <td align="center"><em>User Directory – Karen &amp; Ken</em></td>
    <td align="center"><em>User Profile Page</em></td>
  </tr>
</table>
<p>
Users are the end customers who submit support tickets through the osTicket portal. Two users were created for this lab: <strong>Karen</strong> and <strong>Ken</strong>. These accounts simulate real-world customers who interact with the help desk by submitting and tracking their support requests.
</p>
<br />

---

<h3>Step 8: Configure SLA Plans</h3>

**Path:** Admin Panel -> Manage -> SLA

<table>
  <tr>
    <td><img src="https://i.imgur.com/placeholder.png" width="100%" alt="SLA Plans List – Sev-A, Sev-B, Sev-C"/></td>
    <td><img src="https://i.imgur.com/placeholder.png" width="100%" alt="Sev-A SLA Settings"/></td>
  </tr>
  <tr>
    <td align="center"><em>SLA Plans List – Sev-A, Sev-B, Sev-C</em></td>
    <td align="center"><em>Sev-A – 1 Hour / 24/7</em></td>
  </tr>
</table>
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

<table>
  <tr>
    <td><img src="https://i.imgur.com/placeholder.png" width="100%" alt="Help Topics List"/></td>
    <td><img src="https://i.imgur.com/placeholder.png" width="100%" alt="Business Critical Outage Help Topic"/></td>
  </tr>
  <tr>
    <td align="center"><em>Help Topics List</em></td>
    <td align="center"><em>Business Critical Outage – Topic Settings</em></td>
  </tr>
</table>
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
