<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1 align="center">osTicket – Post-Installation Configuration</h1>

This project demonstrates the post-installation configuration of the open-source help desk ticketing system **osTicket**. It covers roles, departments, teams, agents, users, SLA plans, and help topics — simulating a real-world IT support environment.

---

## 🖥️ Environments and Technologies Used

- **Microsoft Azure** (Virtual Machine)
- **Remote Desktop Protocol (RDP)**
- **Internet Information Services (IIS)**
- **osTicket** (Open-Source Help Desk Ticketing System)
- **Windows 11** (25h2)


---

## 📋 Prerequisites

> Complete the [osTicket Installation Lab](https://github.com/your-username/osticket-prereqs) before starting this configuration.

- osTicket successfully installed and running
- Admin credentials ready
- Access to both the Admin Panel and Agent Panel

---

## 🔐 Login URLs

| Portal | URL |
|---|---|
| **Admin / Analyst Login** | `http://localhost/osTicket/scp/login.php` |
| **End User Portal** | `http://localhost/osTicket` |

---

## ⚙️ Configuration Steps

### 1. Admin Panel vs. Agent Panel

Before configuring, understand the difference between the two panels:

- **Admin Panel** – Used to manage system settings, agents, roles, departments, and SLAs
- **Agent Panel** – Used by help desk agents to manage and respond to tickets

> You can toggle between panels using the link in the top-right corner of the screen.

---

### 2. Configure Roles

**Path:** `Admin Panel → Agents → Roles`

Roles define the permissions granted to agents within a department.

| Role | Description |
|---|---|
| **Supreme Admin** | Full access to all settings and ticket management |

---

### 3. Configure Departments

**Path:** `Admin Panel → Agents → Departments`

Departments control ticket visibility and routing across the help desk.

| Department | Purpose |
|---|---|
| **SysAdmins** | Handles system-level issues and elevated support |

---

### 4. Configure Teams

**Path:** `Admin Panel → Agents → Teams`

Teams allow agents from different departments to collaborate on specific issues.

| Team | Purpose |
|---|---|
| **Online Banking** | Cross-department team for banking-related escalations |

---

### 5. User Settings – Ticket Creation

**Path:** `Admin Panel → Settings → User Settings`

Configured ticket submission to require user registration:

- ☑️ **Uncheck:** *"Unregistered users can create tickets"*
- ✅ **Enable:** *Registration Required — users must log in to submit tickets*

---

### 6. Configure Agents (Workers)

**Path:** `Admin Panel → Agents → Add New`

Agents are the help desk staff who respond to and resolve tickets.

| Agent | Department |
|---|---|
| **Jane** | SysAdmins |
| **John** | Support |

---

### 7. Configure Users (Customers)

**Path:** `Agent Panel → Users → Add New`

Users are the end customers who submit support tickets.

| User |
|---|
| **Karen** |
| **Ken** |

---

### 8. Configure SLA Plans

**Path:** `Admin Panel → Manage → SLA`

SLA (Service Level Agreement) plans define the expected response and resolution times for tickets.

| SLA Plan | Grace Period | Schedule |
|---|---|---|
| **Sev-A** | 1 hour | 24/7 |
| **Sev-B** | 4 hours | 24/7 |
| **Sev-C** | 8 hours | Business Hours |

> **Sev-A** is reserved for the most critical outages. **Sev-C** applies to low-priority, non-urgent requests.

---

### 9. Configure Help Topics

**Path:** `Admin Panel → Manage → Help Topics`

Help Topics guide users when submitting tickets and help route them to the correct department.

| Help Topic |
|---|
| Business Critical Outage |
| Personal Computer Issues |
| Equipment Request |
| Password Reset |
| Other |

---

## ✅ Summary

After completing this configuration, the osTicket environment is set up to:

- Route tickets based on department and severity
- Enforce SLA response times
- Allow agents and end users to interact through a structured support portal
- Simulate a real-world IT help desk workflow

---

## 🔗 Related Projects

- 📦 [osTicket – Prerequisites and Installation](https://github.com/your-username/osticket-prereqs)
- 🎫 [osTicket – Ticket Lifecycle Examples](https://github.com/your-username/ticket-lifecycle)

---

## 👤 Author

**Jonathan Metellus**
IT Support | Help Desk | Azure | osTicket
[LinkedIn](https://www.linkedin.com/in/jonathan-m-85a5b91a6/) • [GitHub](https://github.com/jonathanmetellus21-ux)
