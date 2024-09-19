<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the configuration of osTicket to simulate a help desk environment. The Admin Panel allows adjustments to roles, departments, and SLAs, while the Agent Panel is used by support staff to manage tickets. These settings offer flexibility to fit your learning or business needs.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Configuration Steps</h2>

🔷 ***Connect to the VM created in [osTicket Prerequisites](https://github.com/DamianWimberly/osticket-prereqs)***

- Use **RDP** to connect to the VM via its IP address.

🔷 ***Log in to osTicket Admin Panel***

- Open your browser and navigate to **http://localhost/osTicket/scp/login.php**.
- Enter the admin credentials you created during the installation.

🔷 ***Differentiate Admin and Agent Panels***

- **Admin Panel**: Used to configure system-wide settings and manage users, roles, and permissions.
- **Agent Panel**: Interface for help desk staff to view and manage tickets.

🔷 ***Configure Roles***

- Navigate to **Admin Panel** → **Agents** → **Roles**.
- Edit existing roles or create new roles with specific permissions for Tickets, Tasks, and Knowledgebase.
- Example: Create a "Supreme Admin" role and enable all permissions.

🔷 ***Configure Departments***

- Navigate to **Admin Panel** → **Agents** → **Departments**.
- Create a new department (e.g., "SysAdmins").
- Set the parent department to **Top Level Department**.
- Configure visibility and access so only relevant departments can see specific tickets.
- Example: Allow the "SysAdmins" department to view all tickets, but limit visibility for other departments.

🔷 ***Configure Teams***

- Navigate to **Admin Panel** → **Agents** → **Teams**.
- Create a new team (e.g., "Online Banking") and set the status to **Active**.
- Teams allow agents from different departments to collaborate on specific issues or topics.

🔷 ***Decide Who Can Create Tickets***

- Navigate to **Admin Panel** → **Settings** → **User Settings**.
- For learning purposes, uncheck **Unregistered users can create tickets**.
- Enable **Registration Required** to restrict ticket creation to registered users.

🔷 ***Configure Agents***

- Navigate to **Admin Panel** → **Agents** → **Add New**.
- Add new agents such as "Jane Doe" (in SysAdmins) and "John Doe" (in Support).
- Assign Jane the **Supreme Admin** role and add her to the **Online Banking** team.
- Assign John **View Only Access** and add him to the **Support** department.
- Set agent passwords manually by unchecking "Send the agent a Password Reset Email."

🔷 ***Configure Users***

- Navigate to **Agent Panel** → **Users** → **Add New**.
- Add users like "Karen" and "Ken" who will represent your customers.

🔷 ***Configure Service Level Agreements (SLAs)***

- Navigate to **Admin Panel** → **Manage** → **SLA**.
- Set up SLAs with grace periods and schedules:
   - **Sev-A**: 1-hour response, 24/7.
   - **Sev-B**: 4-hour response, 24/7.
   - **Sev-C**: 8-hour response, business hours only.

🔷 ***Configure Help Topics***

- Navigate to **Admin Panel** → **Manage** → **Help Topics**.
- Add help topics such as "Business Critical Outage," "Password Reset," and "Equipment Request" to categorize tickets.

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
