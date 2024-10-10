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

- Windows 10</b> 

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
    <td>Add New Role</td>
    <td>Create "Supreme Admin"</td>
    <td>Configure Permissions </td>
    <td>Role Activated</td>
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
    <td>Add New Department</td>
    <td>Configure "SysAdmins"</td>
    <td>Department Activated</td>
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
    <td>Add New Team</td>
    <td>Configure "Online Banking" Team</td>
  </tr>
</table>

🔷 ***Decide Who Can Create Tickets***

- Navigate to **Admin Panel** → **Settings** → **User Settings**.
- For learning purposes, uncheck **"Require registration and login to create tickets."**

  - *For lab purposes, we want "anyone" to be able to create a ticket. They also have the option to register if they'd like.*
<table>
  <tr>
    <td><img width="200" height="150" alt="Screenshot 2024-10-08 at 8 48 32 PM" src="https://github.com/user-attachments/assets/74ae0703-d15f-483e-a8e5-7848057c8620"></td>
  <tr>
    <td>non-Registration Permitted</td>
  </tr>
</table>

🔷 ***Configure Agents***

- Navigate to **Admin Panel** → **Agents** → **Add New**.
   - Add new agents such as "Jane Doe" (in SysAdmins) and "John Doe" (in Support).
      - Assign Jane the **Supreme Admin** role and add her to the **Online Banking** team.
      - Assign John **Expanded Access** and add him to the **Support** department.
      - Set agent passwords manually by unchecking "Send the agent a Password Reset Email."
<table>
  <tr>
    <td><img width="200" height="150" alt="Screenshot 2024-10-07 at 10 15 52 PM" src="https://github.com/user-attachments/assets/4189109b-e973-42ee-bbd4-203302983c1e"></td>
    <td><img width="100" height="100" alt="Screenshot 2024-10-07 at 10 18 46 PM" src="https://github.com/user-attachments/assets/e1982ed1-4b93-4129-9885-fe2f0aa81416"><img width="100" height="100" alt="Screenshot 2024-10-07 at 10 20 05 PM" src="https://github.com/user-attachments/assets/14f92a77-6d41-4d78-80c1-e56aa33906bd"></td>
    <td><img width="100" height="100" alt="Screenshot 2024-10-07 at 10 20 42 PM" src="https://github.com/user-attachments/assets/77067b56-4530-4526-b715-4ec1ab08d7e9"><img width="100" height="100" alt="Screenshot 2024-10-07 at 10 20 54 PM" src="https://github.com/user-attachments/assets/d0896eb7-21c3-4e4b-af99-fa3db18d9898"></td>
    <td><img width="200" height="150" alt="Screenshot 2024-10-07 at 10 24 49 PM" src="https://github.com/user-attachments/assets/1250a155-5613-44fe-ac40-6038bd779aa1"></td>
    <td><img width="100" alt="Screenshot 2024-10-10 at 10 45 27 AM" src="https://github.com/user-attachments/assets/f954c441-3f8c-4081-8e2a-0af1f85871a3"><img width="100" height="100" alt="Screenshot 2024-10-07 at 10 26 30 PM" src="https://github.com/user-attachments/assets/83502e34-925a-4ec6-a185-612df90df861"></td>

  <tr>
    <td>Add New Agent</td>
    <td>Add Jane Doe</td>
    <td>Jane Doe Configuration</td>
    <td>Add John Doe</td>
    <td>John Doe Configuration</td>
  </tr>
</table>


🔷 ***Configure Users***

- Navigate to **Agent Panel** → **Users** → **Add New**.
   - Add users like "Karen" and "Ken" who will represent your customers.
<table>
  <tr>
    <td><img width="200" height="150" alt="Screenshot 2024-10-08 at 9 24 51 PM" src="https://github.com/user-attachments/assets/a4ad16c9-0d32-491e-a48f-a9e13c13f404"></td>
    <td><img width="200" height="150" alt="Screenshot 2024-10-08 at 9 25 48 PM" src="https://github.com/user-attachments/assets/651bb592-65f5-46a2-a9f5-e9d34383b0e0"><img width="200" height="150" alt="Screenshot 2024-10-08 at 9 26 34 PM" src="https://github.com/user-attachments/assets/88d93661-085a-4a6b-9fb2-f4ba6794b6b0"></td>
    <td><img width="200" height="150" alt="Screenshot 2024-10-08 at 9 27 28 PM" src="https://github.com/user-attachments/assets/231ffa71-1086-49b1-af97-279b3d86e2ff"><img width="200" height="150" alt="Screenshot 2024-10-08 at 9 27 39 PM" src="https://github.com/user-attachments/assets/fa4901b9-b56a-4f07-8213-6e92127d908c"></td>
  <tr>
    <td>Add User</td>
    <td>User: Karen</td>
    <td>User: Ken</td>
  </tr>
</table>

🔷 ***Configure Service Level Agreements (SLAs)***

- Navigate to **Admin Panel** → **Manage** → **SLA**.
- Set up SLAs with grace periods and schedules:
   - **Sev-A**: 1-hour response, 24/7.
   - **Sev-B**: 4-hour response, 24/7.
   - **Sev-C**: 8-hour response, business hours only.
<table>
  <tr>
    <td><img width="200" height="150" alt="Screenshot 2024-10-08 at 9 42 47 PM" src="https://github.com/user-attachments/assets/db8f87a4-7ad6-4ca3-9d06-a545882751fd"></td>
    <td><img width="200" height="150" alt="Screenshot 2024-10-08 at 9 46 15 PM" src="https://github.com/user-attachments/assets/41918ded-6b58-46da-9fb0-d9bdcc53b9cb"></td>
    <td><img width="200" height="150" alt="Screenshot 2024-10-08 at 9 46 56 PM" src="https://github.com/user-attachments/assets/0351e7f2-0c92-480a-acde-f2264e4ca66d"></td>
    <td><img width="200" height="150" alt="Screenshot 2024-10-08 at 9 47 21 PM" src="https://github.com/user-attachments/assets/21f229be-8e5e-4a7f-851f-c4990c367035"></td>
  <tr>
    <td>Add New SLA Plan</td>
    <td>Sev-A</td>
    <td>Sev-B</td>
    <td>Sev-C</td>
  </tr>
</table>


🔷 ***Configure Help Topics***

- Navigate to **Admin Panel** → **Manage** → **Help Topics**.
   -  Add help topics such as "Business Critical Outage," "Password Reset," and "Equipment Request" to categorize tickets.
   -  In **New ticket options**, you can select the default Help Topic priority and SLA Plan
<table>
  <tr>
    <td><img width="200" height="150" alt="Screenshot 2024-10-08 at 10 06 09 PM" src="https://github.com/user-attachments/assets/eeb8ff2a-e2f6-42df-8fc4-f18a23e1e67f"></td>
    <td><img width="200" height="150" alt="Screenshot 2024-10-08 at 10 07 47 PM" src="https://github.com/user-attachments/assets/03d6e9e7-1918-4d3f-9a50-3670d0b087f2"><img width="200" alt="Screenshot 2024-10-09 at 4 18 53 PM" src="https://github.com/user-attachments/assets/50ce33ba-4cba-433d-9d06-927a3a609669">
</td>
    <td><img width="200" alt="Screenshot 2024-10-09 at 4 22 21 PM" src="https://github.com/user-attachments/assets/8089340a-b5f0-48d9-b5db-6177f55844f5"></td>
    <td><img width="200" alt="Screenshot 2024-10-09 at 4 22 43 PM" src="https://github.com/user-attachments/assets/e1596f01-78ae-4470-b51a-2efa380e444d">
</td>
  <tr>
    <td>Add New Help Topic</td>
    <td>Business Critical Outage</td>
    <td>Password Reset</td>
    <td>Equipment Request</td>
  </tr>
</table>
