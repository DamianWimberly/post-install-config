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
    <td>Connect via RDP</td>
  </tr>
</table>

🔷 ***Log in to osTicket Admin Panel***

- Open your browser and navigate to **http://localhost/osTicket/scp/login.php**.
   - Enter the admin credentials you created during the installation.
<table>
  <tr>
    <td><img width="200" height="150" alt="Screenshot 2024-10-07 at 8 24 48 PM" src="https://github.com/user-attachments/assets/9e644089-4545-4f03-b8f9-b2fae9cca845"></td>
    
  <tr>
    <td>osTicket Login</td>
  </tr>
</table>

🔷 ***Differentiate Admin and Agent Panels***

- **Admin Panel**: Used to configure system-wide settings and manage users, roles, and permissions.
- **Agent Panel**: Interface for help desk staff to view and manage tickets.
<table>
  <tr>
    <td><img width="200" height="150" alt="Screenshot 2024-10-07 at 8 31 03 PM" src="https://github.com/user-attachments/assets/123e6581-436e-432d-8f81-2d653b052a94"></td>
    <td><img width="200" height="150" alt="Screenshot 2024-10-07 at 8 31 20 PM" src="https://github.com/user-attachments/assets/34f8a1b2-434c-43c1-8ea3-17259447ee47"></td>
  <tr>
    <td>Admin Panel</td>
    <td>Agent Panel</td>
  </tr>
</table>

🔷 ***Configure Roles***

- Navigate to **Admin Panel** → **Agents** → **Roles**.
   - Edit existing roles or create new roles with specific permissions for Tickets, Tasks, and Knowledgebase.
   -  Example: Create a "Supreme Admin" role and enable all permissions.
<table>
  <tr>
    <td><img width="200" height="150" alt="Screenshot 2024-10-07 at 8 37 24 PM" src="https://github.com/user-attachments/assets/d6b3a050-270e-4e53-af6f-290ebeb0ae3b"></td>
    <td><img width="200" height="150" alt="Screenshot 2024-10-07 at 8 42 34 PM" src="https://github.com/user-attachments/assets/f87698a8-5e19-4c50-aaaa-c1920717188b"></td>
    <td><img width="200" height="150" alt="Screenshot 2024-10-07 at 8 44 03 PM" src="https://github.com/user-attachments/assets/def66cc2-a8f8-456c-a1cf-86dc6035dced"><img width="200" height="150" alt="Screenshot 2024-10-07 at 8 44 27 PM" src="https://github.com/user-attachments/assets/f32bf5b7-78a9-4fce-8690-3b5091b60564"></td>
    <td><img width="200" height="150" alt="Screenshot 2024-10-07 at 8 44 45 PM" src="https://github.com/user-attachments/assets/52b4d734-82e7-46ca-b09b-dd0d51f4fe5b"> </td>
  <tr>
    <td>VM Public IP Address</td>
    <td>Connect via RDP</td>
    <td>Connect via RDP</td>
    <td>Connect via RDP</td>
  </tr>
</table>

🔷 ***Configure Departments***

- Navigate to **Admin Panel** → **Agents** → **Departments**.
   - Create a new department (e.g., "SysAdmins").
   - Set the parent department to **Top Level Department**.
   -  Configure visibility and access so only relevant departments can see specific tickets.
      - Example: Allow the "SysAdmins" department to view all tickets, but limit visibility for other departments.
<table>
  <tr>
    <td><img width="200" height="150" alt="Screenshot 2024-10-07 at 9 02 17 PM" src="https://github.com/user-attachments/assets/beabb323-5955-449b-9e26-23cadab0a403"></td>
    <td><img width="200" height="150" alt="Screenshot 2024-10-07 at 9 21 34 PM" src="https://github.com/user-attachments/assets/1227f850-8fd5-408b-9a9b-c22030f2b04b"></td>
    <td><img width="200" height="150" alt="Screenshot 2024-10-07 at 9 31 30 PM" src="https://github.com/user-attachments/assets/114c01fe-3196-465b-b04d-9335dcddc65e"></td>
  <tr>
    <td>Step 1</td>
    <td>Step 2</td>
    <td>Step 3</td>
  </tr>
</table>

🔷 ***Configure Teams***

- Navigate to **Admin Panel** → **Agents** → **Teams**.
   - Create a new team (e.g., "Online Banking") and set the status to **Active**.
       - Teams allow agents from different departments to collaborate on specific issues or topics.
<table>
  <tr>
    <td><img width="200" height="150" alt="Screenshot 2024-10-07 at 9 33 41 PM" src="https://github.com/user-attachments/assets/93bb09d0-ad2b-4750-b5f5-2ce8cfb71e82"></td>
    <td><img width="200" height="150" alt="Screenshot 2024-10-07 at 9 34 37 PM" src="https://github.com/user-attachments/assets/9947582f-55c2-4068-8062-5e8e1e1aaa78"></td>
  
  <tr>
    <td>Step 1</td>
    <td>Step 2</td>
  </tr>
</table>

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
<table>
  <tr>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  <tr>
    <td>Step 1</td>
    <td>Step 2</td>
    <td>Step 3</td>
    <td>Step 4</td>
  </tr>
</table>
