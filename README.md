<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket Help Desk Lab

**Project Overview**

Hands-on help desk administration lab demonstrating the deployment, configuration, and use of **osTicket**, an open-source ticketing platform, in a Microsoft Azure-hosted Windows environment.

The project covers the complete help desk workflow, from deploying the ticketing system and configuring its supporting services to creating users, agents, departments, teams, SLAs, and help topics. The final phase demonstrates a realistic ticket lifecycle from initial intake through troubleshooting and resolution.

---

## Objective

Build practical experience deploying and administering a help desk ticketing platform while simulating a structured IT support environment.

This project demonstrates the ability to:

* Deploy and administer a Windows virtual machine in Azure
* Configure IIS as a web server
* Install and integrate PHP with IIS
* Install and configure MySQL
* Deploy and configure osTicket
* Manage users, agents, roles, departments, and teams
* Configure SLAs and help topics
* Assign and prioritize support tickets
* Document troubleshooting activity
* Communicate with end users
* Resolve and close support tickets

---

## Environment and Technologies

* **Microsoft Azure** — Virtual Machines / Compute
* **Windows 10 21H2**
* **Internet Information Services (IIS)**
* **PHP 7.3.8**
* **MySQL**
* **HeidiSQL**
* **osTicket 1.15.8**
* **Remote Desktop (RDP)**

---

# Part 1 — osTicket Installation

## Azure Virtual Machine Deployment

Provisioned a Windows 10 virtual machine in Microsoft Azure to host the osTicket application and supporting services.

The VM was accessed remotely using Remote Desktop and served as the primary environment for the lab.

---

## IIS Web Server Configuration

Installed and configured **Internet Information Services (IIS)** as the web server for the osTicket application.

Configured the required **CGI** functionality to allow IIS to process PHP applications.

Additional IIS components included:

* PHP Manager for IIS
* IIS URL Rewrite Module

---

## PHP Installation and IIS Integration

Created a dedicated PHP directory at:

`C:\PHP`

Installed PHP 7.3.8 and registered the PHP CGI executable with IIS using PHP Manager.

Required PHP extensions were also enabled:

* `php_imap.dll`
* `php_intl.dll`
* `php_opcache.dll`

This provided the PHP runtime and supporting functionality required by the osTicket application.

---

## MySQL Database Configuration

Installed MySQL and configured the database environment used by osTicket.

Using HeidiSQL, created the application database:

`osTicket`

The database provides persistent storage for ticket information, users, configuration data, and other application records.

> **Lab Security Note:** The database credentials used during the original training lab were intentionally simplified for a disposable learning environment. Production deployments should use strong credentials, restricted database permissions, and the principle of least privilege.

---

## osTicket Deployment

Extracted the osTicket application files and deployed the application to the IIS web root:

`C:\inetpub\wwwroot\osTicket`

Configured the application's `ost-config.php` file and completed the installation through the osTicket web interface.

The installation was then validated by accessing the administrator interface locally through IIS.

---

# Part 2 — Post-Installation Configuration

With the osTicket platform installed, the environment was configured to represent a structured IT support organization.

## Roles and Permissions

Created administrative roles and configured permissions controlling what agents can access and manage within the help desk system.

This demonstrates basic **role-based access control (RBAC)** and the importance of assigning permissions according to job responsibilities.

---

## Departments and Teams

Created organizational structures to support ticket routing and collaboration.

Example configurations included:

* **SysAdmins** department
* **Support** department
* **Online Banking** team

Departments organize agents according to functional responsibilities, while teams allow agents to collaborate around specific support areas.

---

## Agent Accounts

Created support agent accounts and assigned them to appropriate departments.

Example agents included:

* Jane — SysAdmins
* John — Support

Agent accounts represent members of the IT support organization responsible for reviewing, assigning, troubleshooting, and resolving tickets.

---

## End User Accounts

Created end-user accounts representing employees who submit support requests through the help desk.

Example users included:

* Karen
* Ken

This provided a separate user perspective for testing the ticket submission and communication workflow.

---

## Service Level Agreements

Configured multiple SLA levels to establish different response and resolution expectations.

Example SLA levels:

* **Sev-A**
* **Sev-B**
* **Sev-C**

SLAs provide a framework for prioritizing tickets and measuring support response and resolution expectations.

---

## Help Topics

Created structured help topics to categorize incoming support requests.

Examples included:

* Business Critical Outage
* Personal Computer Issues
* Equipment Request
* Password Reset
* Other

Help Topics provide a consistent method for categorizing requests and supporting efficient ticket routing.

---

# Part 3 — Ticket Lifecycle

The final phase of the project demonstrates the complete lifecycle of a help desk ticket from initial submission through resolution.

The simulated scenario involved an **online banking system outage**, providing an example of how a support organization could handle a high-priority issue.

## 1. Intake

An end user submitted a support request through the osTicket support center.

**Example issue:**

> Online banking system down

The ticket captures the initial problem description and creates a record that can be reviewed and managed by the support team.

---

## 2. Assignment and Communication

The ticket was reviewed by a support agent and assigned to the appropriate team.

The agent was able to:

* Review the ticket details
* Determine the appropriate assignment
* Apply SLA information
* Communicate with the end user
* Manage ticket access and visibility

This demonstrates the initial triage and communication stage of the help desk workflow.

---

## 3. Troubleshooting and Documentation

The assigned agent worked through the issue while documenting activity within the ticket.

Troubleshooting documentation provides a record of:

* Actions taken
* Internal notes
* Communication with the user
* Status updates
* Progress toward resolution

Maintaining this history allows other technicians to understand what has already been attempted and provides accountability throughout the support process.

---

## 4. Resolution and Closure

After the issue was resolved, the ticket was updated with the final resolution and closed.

The completed ticket provides a record of the original request, troubleshooting activity, communication, and final outcome.

This completes the standard help desk workflow:

**Intake → Assignment → Troubleshooting → Resolution → Closure**

---

# Skills Demonstrated

### Systems Administration

* Windows administration
* Azure virtual machine deployment
* Remote Desktop administration
* IIS configuration
* PHP installation and configuration
* MySQL database administration
* Web application deployment

### Help Desk Administration

* Role and permission management
* User and agent administration
* Department and team organization
* SLA configuration
* Help topic configuration
* Ticket assignment and prioritization

### IT Support Operations

* Ticket intake and triage
* End-user communication
* Troubleshooting documentation
* Ticket escalation and assignment
* SLA-based prioritization
* Ticket resolution and closure

---

# Screenshots & Visual Evidence

## Azure & osTicket Installation

<details>
<summary>Expand Installation Screenshots</summary>

### Azure Virtual Machine

![Azure VM](https://github.com/user-attachments/assets/afe23a0e-6341-4de7-a9b4-2c11f976977a)

### Azure Public IP

![Azure Public IP](https://github.com/user-attachments/assets/8e89d4d6-e755-45f5-93fe-1d744b530ccc)

### Remote Desktop

![Remote Desktop](https://github.com/user-attachments/assets/20c22800-c6f1-449c-9228-56af40441397)

### Installation Files

![Installation Files](https://github.com/user-attachments/assets/2215e6b7-5421-45f5-b4b9-004ba39996f8)

### IIS CGI Configuration

![IIS CGI](https://github.com/user-attachments/assets/8a24e127-72f5-4ae9-a942-a19f532992ab)

### PHP Manager

![PHP Manager](https://github.com/user-attachments/assets/a9a4e433-4e90-4d23-a64e-3e9ff0ad0688)

### IIS URL Rewrite

![URL Rewrite](https://github.com/user-attachments/assets/c6536fd6-d0f2-4adf-8dfb-d24b225ab910)

### PHP Directory

![PHP Directory](https://github.com/user-attachments/assets/7166cfaa-c417-4809-8034-772fe2c8a199)

### PHP Installation

![PHP Installation](https://github.com/user-attachments/assets/b2661ca0-77da-4f80-84f5-52c0673d9fd1)

### Visual C++ Redistributable

![VC Redistributable](https://github.com/user-attachments/assets/0cd9580b-8125-42ff-9959-abad56e885ab)

### MySQL Configuration

![MySQL Setup](https://github.com/user-attachments/assets/c2923a73-d8c1-46c3-8fc4-4be7caa9d751)

### IIS Manager

![IIS Manager](https://github.com/user-attachments/assets/9b705a8a-88ba-4ecc-b4c9-37b4907d76a1)

### PHP Registration

![PHP Registration](https://github.com/user-attachments/assets/4c4c0858-39d9-486b-bd25-abd8cdcedb57)

### osTicket Deployment

![osTicket Files](https://github.com/user-attachments/assets/797b172a-fc82-4c9a-908f-3ae68bf99f62)

![osTicket Deployment](https://github.com/user-attachments/assets/e234aa6a-e213-468f-9f88-a0287105904f)

![osTicket Directory](https://github.com/user-attachments/assets/e77602bc-14a5-4f99-9827-8a6777300ce7)

### PHP Extensions

![PHP Extensions](https://github.com/user-attachments/assets/644ae224-bc86-4857-b28d-d4b0c0e57681)

### osTicket Configuration File

![Configuration File](https://github.com/user-attachments/assets/f4389faa-a498-4c31-a4a8-24ddc977c6f3)

![File Permissions](https://github.com/user-attachments/assets/51c9e3ea-09bc-4fc3-a9d6-3ea78d67a060)

### MySQL Database

![HeidiSQL](https://github.com/user-attachments/assets/5dfce464-9ece-4ed8-b513-3d2c157bfe6d)

![osTicket Database](https://github.com/user-attachments/assets/230d0b79-6bcb-41d6-a534-798bd2f487c9)

### osTicket Installation

![osTicket Installer](https://github.com/user-attachments/assets/d3cfe18c-220e-4aef-a2b5-2807749ab2f2)

![Installation Complete](https://github.com/user-attachments/assets/22ecefb0-a186-46bc-8788-a55e7a3a7ddd)

### Administrator Access

![Admin Login](https://github.com/user-attachments/assets/9dbd2b87-3930-4fee-a74c-74955092a4bd)

</details>

---

## Post-Installation Configuration

<details>
<summary>Expand Configuration Screenshots</summary>

### Roles and Permissions

![Roles](https://github.com/user-attachments/assets/216f0685-df4e-4494-876d-6818e0788280)

![Role Permissions](https://github.com/user-attachments/assets/cbc58fde-6d0f-4588-81c8-63a8d9cc7f0e)

### Departments

![Departments](https://github.com/user-attachments/assets/055e8294-072d-46cc-8fe9-372d64b98a3d)

### Teams

![Teams](https://github.com/user-attachments/assets/2d2c4c28-be99-4a34-846c-9083bd56ce76)

### User Settings

![User Settings](https://github.com/user-attachments/assets/2c644168-56bb-4cdb-bccd-15e12ca02978)

### Agent Configuration

![Agent Configuration](https://github.com/user-attachments/assets/bb03b461-ac60-48c1-a1f3-363637d09bf2)

![Agent Permissions](https://github.com/user-attachments/assets/e2fe11d5-e561-4bc3-aec9-6ae90e5225c5)

![Agent Department](https://github.com/user-attachments/assets/2289e323-8bed-4cfb-948f-2946f7abb2a4)

![Agent Configuration](https://github.com/user-attachments/assets/dbdbf07e-9701-4d26-ab94-c1696aa68740)

### End Users

![User Configuration](https://github.com/user-attachments/assets/86d85028-9501-412a-b342-aefc439482fe)

![User Account](https://github.com/user-attachments/assets/13fa0ad1-b8d1-4447-b0ca-395ee9851cad)

### Service Level Agreements

![SLA Configuration](https://github.com/user-attachments/assets/1d6e7028-472d-4651-8c31-d4f3e59b17ce)

![SLA Levels](https://github.com/user-attachments/assets/7e6fa8e5-81ca-458f-b48d-9ae9815458ac)

### Help Topics

![Help Topics](https://github.com/user-attachments/assets/28d03e9a-7829-4c4b-a90a-bc22cc6d3b72)

![Help Topic Configuration](https://github.com/user-attachments/assets/0fe052cb-cb98-4120-b15d-48e7e0a80517)

</details>

---

## Ticket Lifecycle

<details>
<summary>Expand Ticket Lifecycle Screenshots</summary>

### Ticket Intake

**Support Center**

<img width="1552" height="785" alt="Support Center" src="https://github.com/user-attachments/assets/6133f858-1cac-4e1b-a810-c57c30122470" />

**New Ticket**

<img width="1558" height="844" alt="New Ticket" src="https://github.com/user-attachments/assets/a7c8b149-9172-4e78-b4e2-75eac4308045" />

### Assignment & Communication

**Agent View**

<img width="1552" height="781" alt="Agent Ticket View" src="https://github.com/user-attachments/assets/7365e43a-37c2-42c2-a932-f9b5c2832c68" />

<img width="1554" height="780" alt="Ticket Details" src="https://github.com/user-attachments/assets/54a945ad-5b85-4907-b94d-58dbe39c8008" />

**Ticket Access / Visibility**

<img width="1553" height="816" alt="Ticket Permissions" src="https://github.com/user-attachments/assets/6b50fb7c-1f7b-4b9a-9a93-f18ab1a27908" />

<img width="1553" height="781" alt="Ticket Access" src="https://github.com/user-attachments/assets/814df391-3aa0-4a1f-86ee-48caa2224225" />

**SLA and Team Assignment**

<img width="1555" height="779" alt="SLA Assignment" src="https://github.com/user-attachments/assets/3cfb97b5-bca5-43e7-9f68-b1b82afa4c38" />

<img width="1554" height="784" alt="Team Assignment" src="https://github.com/user-attachments/assets/f45debd3-707e-45b6-93d9-921261bf49fc" />

### Troubleshooting & Documentation

<img width="1554" height="781" alt="Ticket Work" src="https://github.com/user-attachments/assets/9afe6141-e6be-4307-9213-a89639ee7a65" />

<img width="1554" height="736" alt="Ticket Updates" src="https://github.com/user-attachments/assets/80f8e56c-c7ef-4888-aa89-d947236113d4" />

<img width="1559" height="805" alt="Ticket Documentation" src="https://github.com/user-attachments/assets/f1c30805-20a5-422c-b48c-755387f7a406" />

### Resolution

<img width="1548" height="767" alt="Resolved Ticket" src="https://github.com/user-attachments/assets/12fc67f3-7be0-4207-8700-9466e56f7f72" />

</details>

---

## Project Outcome

Successfully deployed and configured osTicket in an Azure-hosted Windows environment and demonstrated a complete help desk workflow from **ticket intake through resolution**.

The project combines hands-on **Windows and web application administration** with practical **IT service desk operations**, providing experience directly applicable to entry-level IT support and help desk environments.
