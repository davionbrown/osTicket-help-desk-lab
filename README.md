# osTicket Help Desk Administration & Ticket Lifecycle Lab

## Project Overview

Built and configured an osTicket help desk training environment on a Windows virtual machine hosted in Microsoft Azure.

Completed a CourseCareers training lab and repeated exercises to strengthen my understanding of application installation, database configuration, help desk administration, access control, service-level agreements (SLAs), and incident management.

I also developed an independent CFO laptop troubleshooting scenario to practice ticket creation, technician assignment, diagnostic planning, documentation, and ticket closure.

**Lab Disclaimer:** This project was completed in a controlled training environment. All users and incidents were simulated. The CFO laptop repair described in the ticket was hypothetical; no physical hardware testing or repair was performed.

## Technologies and Skills

- Microsoft Azure Virtual Machines
- Windows and Remote Desktop Protocol (RDP)
- Internet Information Services (IIS)
- CGI and PHP
- MySQL and HeidiSQL
- osTicket Administration
- Role-Based Access Control (RBAC)
- Authentication and Authorization
- Principle of Least Privilege
- Service-Level Agreements (SLAs)
- Ticket Routing, Escalation, and Closure
- Technical Documentation and Troubleshooting

---

## 1. Environment Setup and Installation

### Azure Virtual Machine

![Azure VM Overview](screenshots/01-Azure-VM.png)

Prepared an Azure-hosted Windows virtual machine as the environment for installing and configuring osTicket.

Accessed the virtual machine remotely from my Lenovo Windows laptop using Remote Desktop.

**Skills demonstrated:** Cloud infrastructure, virtualization, Windows administration, and remote connectivity.

### IIS and CGI Configuration

![IIS Configuration](screenshots/02-IIS-configuration.png)

Enabled Internet Information Services (IIS) and CGI functionality to support the PHP-based osTicket application.

This exercise reinforced how web applications depend on properly configured server components.

**Skills demonstrated:** Windows web server configuration, IIS, CGI, and application dependencies.

### MySQL Database

![MySQL Database](screenshots/03-MySQL-Database.png)

Configured MySQL and used HeidiSQL to examine the osTicket database and application tables.

The database provides the storage infrastructure for ticket records, user information, and application configuration.

**Skills demonstrated:** Database fundamentals, MySQL configuration, and application infrastructure.

### osTicket Installation

![osTicket Installation Success](screenshots/04-osticket-Installation.png)

Completed the osTicket installation process and confirmed that the application was accessible for additional administrative configuration.

The installation screen also identified post-installation security tasks, including restricting configuration file permissions and removing installation files.

**Skills demonstrated:** Application deployment, installation verification, and awareness of post-installation security requirements.

---

## 2. Help Desk Administration

### Agent Roles and Permissions

![Agent Roles](screenshots/05-agent-roles.png)

Reviewed and configured agent roles to understand how permissions determine which actions support technicians can perform.

This provided practical exposure to role-based access control and the importance of assigning appropriate permissions.

**Skills demonstrated:** RBAC, authorization, permission management, and least privilege.

### Department Configuration

![Departments](screenshots/06-departments.png)

Configured and reviewed help desk departments, including Support and SysAdmins, to understand how organizational structure influences ticket ownership and departmental access.

The screenshot captures an intermediate stage of the lab configuration, including the Maintenance department before its removal.

**Skills demonstrated:** Department administration, ticket routing, organizational structure, and access control.

### Support Teams

![Support Teams](screenshots/07-support-teams.png)

Configured support teams to explore how agents can be organized for different ticket workflows and collaborative support responsibilities.

**Skills demonstrated:** Team administration, workflow organization, and support operations.

### Support Agents

![Support Agents](screenshots/08-support-agents.png)

Configured simulated technician accounts, including John Doe in Support and Jane Doe in SysAdmins.

Practiced ticket assignment and department-based access restrictions using the training accounts.

Some administrative actions and ticket documentation were also performed through the Davion Brown administrator account rather than the assigned technician account.

This distinction reinforced the importance of accurate account attribution and technician accountability.

**Skills demonstrated:** Agent account administration, technician assignment, authorization, and activity tracking.

### Service-Level Agreements

![SLA Plans](screenshots/09-SLA-plans.png)

Configured three service-level agreement plans with different grace periods.

| SLA | Grace Period |
|---|---|
| Sev-A | 1 hour |
| Sev-B | 4 hours |
| Sev-C | 8 hours |

Practiced selecting SLA plans based on simulated incident requirements, business impact, and service expectations.

**Skills demonstrated:** SLA configuration, incident prioritization, and service management.

### Help Topics

![Help Topics](screenshots/10-help-topics.png)

Reviewed and configured help topics for different support requests, including business-critical outages, password resets, equipment requests, and computer-related issues.

Help topics help classify incoming incidents and organize support workflows.

**Skills demonstrated:** Ticket classification, incident intake, and workflow configuration.

---

## 3. Ticket Management and Access Control

### Banking Outage — Initial Incident Assessment

![Banking Incident](screenshots/11-banking-incident.png)

Created and reviewed a simulated incident involving an outage of an organization's online and mobile banking services.

Examined the ticket's initial properties, including:

- Priority
- Department
- SLA plan
- Technician assignment

The initial ticket settings did not necessarily reflect the potential business impact of a widespread banking outage.

This exercise reinforced the importance of evaluating affected users, service availability, and operational impact when determining incident severity.

**Skills demonstrated:** Incident intake, business-impact assessment, ticket management, and escalation.

### Department-Based Access Control

![Department Access Control](screenshots/12-access-control.png)

Investigated why a Support technician could no longer access the banking incident after the ticket was transferred to the SysAdmins department.

The technician could successfully authenticate to osTicket, but departmental authorization restricted access to the transferred ticket.

Used the administrator account to review and modify training permissions, helping identify how agent roles and department access affect ticket visibility.

**Key technical lesson:**

Authentication verifies a user's identity, while authorization determines which resources and actions that user is permitted to access.

The exercise also reinforced the principle of least privilege: technicians should receive only the permissions necessary to perform their assigned responsibilities.

**Skills demonstrated:** Authorization troubleshooting, RBAC, least privilege, and ticket escalation.

---

## 4. Independent CFO Laptop Troubleshooting Scenario

### Create a Fictional End User

![CFO User Account](screenshots/13-cfo-user-account.png)

Created a fictional CFO end-user account named Celeste Brown to practice user administration and develop an independent support scenario beyond the instructor-led exercises.

**Skills demonstrated:** End-user account creation and help desk administration.

### Create and Configure the Incident

![CFO Laptop Ticket](screenshots/14-cfo-ticket.png)

Created Ticket **#936362** for a fictional CFO reporting that her company-issued laptop would not power on.

Configured the following properties:

| Property | Configuration |
|---|---|
| Issue | CFO laptop will not power on |
| Priority | Normal |
| Department | Support |
| SLA | Sev-B (4 hours) |
| Assigned Technician | John Doe |
| Help Topic | Personal Computer Issues |
| Ticket Source | Phone |

The reported issue prevented the CFO from accessing work files and preparing for an upcoming financial presentation.

This scenario provided additional practice in evaluating business impact and documenting technical incidents.

**Skills demonstrated:** Ticket creation, technician assignment, SLA selection, and incident documentation.

### Document the Troubleshooting Process

![CFO Troubleshooting Notes](screenshots/15-cfo-troubleshooting.png)

Created an internal troubleshooting note outlining a structured approach to diagnosing the laptop's reported power issue.

**Troubleshooting plan:**

1. Identify symptoms by checking power indicators, fan activity, and signs of system startup.
2. Verify the power source by inspecting the charging adapter, cable connections, electrical outlet, and charging port.
3. Test with a known-good compatible charger, if available.
4. Determine whether the problem involves a complete power failure, display issue, or startup problem.
5. Consider a manufacturer-approved power reset when appropriate.
6. Evaluate business impact and consider an approved loaner laptop to maintain productivity.

A later internal note documented a hypothetical resolution involving a faulty power adapter that was replaced, restoring normal laptop startup.

**Training clarification:** No physical laptop was examined or repaired. The diagnosis and resolution were simulated to practice support documentation and ticket closure.

The internal notes were entered using the Davion Brown administrator account, although the ticket was assigned to John Doe.

**Skills demonstrated:** Structured troubleshooting, diagnostic planning, business-impact assessment, technical documentation, and accurate activity recording.

### Ticket Audit Trail and Closure

![Closed Tickets Dashboard](screenshots/16-closed-tickets.png)

Reviewed the osTicket Closed Tickets queue and verified two completed simulated incidents:

- CFO laptop power issue — Closed by Davion Brown.
- Accounting department Adobe software issue — Closed by John Doe.

The closed-ticket records demonstrate how osTicket tracks ticket status, closure information, and the accounts responsible for support activity.

**Audit trail observation:**

Although the CFO incident was assigned to John Doe, troubleshooting documentation and ticket closure were performed using the Davion Brown administrator account.

Reviewing this history reinforced the importance of using the correct technician account and accurately recording who performed each action.

The banking outage ticket's final closure was not verified by this screenshot.

**Skills demonstrated:** Ticket lifecycle management, audit trails, incident closure, and technician accountability.

---

## 5. Key Lessons Learned

### Infrastructure and Application Support

Learned how a web-based ticketing system depends on a functioning web server, PHP runtime, and database.

### Authentication vs. Authorization

Developed a clearer understanding of the difference between successfully signing into a system and having permission to access specific resources.

### Help Desk Administration

Practiced configuring departments, teams, roles, agents, and service-level agreements.

### Incident Prioritization

Learned why incident severity should reflect business impact and urgency rather than relying solely on the requester's job title.

### Structured Troubleshooting

Practiced identifying symptoms, developing diagnostic plans, evaluating possible causes, and documenting next steps.

### Technical Documentation

Learned to distinguish planned troubleshooting steps, verified findings, and hypothetical resolutions.

### Technician Accountability

Observed how ticket history and account attribution help organizations determine who performed specific support actions.

### Security and Least Privilege

Learned why departmental access restrictions and appropriate permissions are important for protecting support information.

Also recognized that successful application installation does not automatically mean a system has completed all required security-hardening steps.

---

## 6. Project Scope and Limitations

This project documents hands-on learning within a controlled training environment rather than production IT operations.

The banking outage, Adobe software issue, and CFO laptop incident were simulated.

The CFO laptop problem was not physically tested, and the documented power-adapter replacement was hypothetical.

Some support actions were performed using the administrator account rather than the assigned technician account. These actions are accurately identified in the project documentation.

The installation followed an older training checklist and should not be treated as a recommendation to deploy outdated software versions in a production environment.

The primary objective was to strengthen practical knowledge of help desk administration, access control, incident management, and technical documentation.

---

## 7. Career Relevance

This project supports my transition into entry-level information technology roles, including:

- Help Desk Technician
- IT Support Specialist
- Service Desk Analyst
- Junior Network Support Technician

Through this lab, I gained practical experience working with a ticketing platform, configuring support workflows, managing permissions, documenting simulated incidents, and troubleshooting authorization issues.

I plan to continue building on these foundational skills through additional hands-on labs, technical training, and IT certification studies.
