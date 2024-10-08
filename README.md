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

- **Connect to the Azure Virtual Machine** to host osTicket.
- **Log in and differentiate between the Admin and Agent Panels** in osTicket.
- **Configure roles, departments, and teams** to manage permissions and visibility for agents.
- **Create and manage agents and users** for the help desk system.
- **Set up Service Level Agreements (SLAs)** to define response and resolution times for tickets.
- **Create and configure Help Topics** to organize and categorize incoming support tickets.


<h2>Configuration Steps</h2>

🔷 ***Connect to the VM created in [osTicket Prerequisites](https://github.com/DamianWimberly/osticket-prereqs)***

- Use **RDP** to connect to the VM via its IP address.

<table>
  <tr>
    <td><img width="200" alt="3" src="https://github.com/user-attachments/assets/ae14a1a6-f5ba-44e8-b69b-596f1888d1c1">
</td>
    <td><img width="200" height= "150" alt="4" src="https://github.com/user-attachments/assets/6a1ef0a9-946a-4e55-8ea3-ff20661ceaa5">
  <tr>
    <td>VM Public IP Address</td>
    <td>Connect via RDP</td></td>
  </tr>
</table>

🔷 ***Log in to osTicket Admin Panel***

- Open your browser and navigate to **http://localhost/osTicket/scp/login.php**.
   - Enter the admin credentials you created during the installation.
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

🔷 ***Differentiate Admin and Agent Panels***

- **Admin Panel**: Used to configure system-wide settings and manage users, roles, and permissions.
- **Agent Panel**: Interface for help desk staff to view and manage tickets.
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

🔷 ***Configure Roles***

- Navigate to **Admin Panel** → **Agents** → **Roles**.
   - Edit existing roles or create new roles with specific permissions for Tickets, Tasks, and Knowledgebase.
   -  Example: Create a "Supreme Admin" role and enable all permissions.
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

🔷 ***Configure Departments***

- Navigate to **Admin Panel** → **Agents** → **Departments**.
   - Create a new department (e.g., "SysAdmins").
   - Set the parent department to **Top Level Department**.
   -  Configure visibility and access so only relevant departments can see specific tickets.
      - Example: Allow the "SysAdmins" department to view all tickets, but limit visibility for other departments.
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

🔷 ***Configure Teams***

- Navigate to **Admin Panel** → **Agents** → **Teams**.
   - Create a new team (e.g., "Online Banking") and set the status to **Active**.
   - Teams allow agents from different departments to collaborate on specific issues or topics.
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

🔷 ***Decide Who Can Create Tickets***

- Navigate to **Admin Panel** → **Settings** → **User Settings**.
  - For learning purposes, uncheck **Unregistered users can create tickets**.
  - Enable **Registration Required** to restrict ticket creation to registered users.
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

🔷 ***Configure Agents***

- Navigate to **Admin Panel** → **Agents** → **Add New**.
   - Add new agents such as "Jane Doe" (in SysAdmins) and "John Doe" (in Support).
      - Assign Jane the **Supreme Admin** role and add her to the **Online Banking** team.
      - Assign John **View Only Access** and add him to the **Support** department.
      - Set agent passwords manually by unchecking "Send the agent a Password Reset Email."
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

🔷 ***Configure Users***

- Navigate to **Agent Panel** → **Users** → **Add New**.
   - Add users like "Karen" and "Ken" who will represent your customers.
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

🔷 ***Configure Service Level Agreements (SLAs)***

- Navigate to **Admin Panel** → **Manage** → **SLA**.
- Set up SLAs with grace periods and schedules:
   - **Sev-A**: 1-hour response, 24/7.
   - **Sev-B**: 4-hour response, 24/7.
   - **Sev-C**: 8-hour response, business hours only.
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

🔷 ***Configure Help Topics***

- Navigate to **Admin Panel** → **Manage** → **Help Topics**.
   -  Add help topics such as "Business Critical Outage," "Password Reset," and "Equipment Request" to categorize tickets.
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
