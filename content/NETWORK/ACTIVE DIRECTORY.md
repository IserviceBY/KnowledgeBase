---
lastSync: Mon Feb 23 2026 10:57:31 GMT+0300 (Moscow Standard Time)
---
# What is Active Directory?

Active Directory, often shortened to AD, is a directory service developed by Microsoft. It helps organizations keep track of users, computers, printers, groups, and other resources on a network — all in one place. Instead of managing access manually for each device or user, AD allows IT teams to organize everything centrally.

Active Directory is both a database and a directory service that helps define who can do what within a network. It allows organizations to manage their network and resources efficiently, making it a crucial tool for enterprises to secure and streamline their networks.

As a database, Active Directory allows you to store and manage identities and their information. As a directory service, it enables identities to authenticate themselves to access a resource, and authorizes access for users in the network itself.

It’s been around since Windows 2000 Server and remains a key part of many IT environments today, especially for businesses using Windows-based systems.


# How Does Active Directory Work?

The main Active Directory service is Active Directory Domain Services (AD DS), which is part of the Windows Server operating system. Once the Active Directory Domain Services is installed on a server, it becomes a domain controller (DCs). This server stores the entire AD database, including objects, trees, and their relationships. Organizations normally have several Domain Controllers, and each one has a copy of the directory for the entire domain. Changes made to the directory on one domain controller, for example this could be a password update or the addition or deletion of data, are replicated to the other DCs so that they all remain up to date. Desktops, laptops and other devices running Windows (rather than Windows Server) can be part of an Active Directory environment, but they do not run Active Directory Domain Services.

**Here’s a simple breakdown of how it works:**

**Authentication:** When you enter your username and password, AD verifies your identity using stored credentials.

**Authorization:** Once you're authenticated, AD checks your permissions — for example, whether you're allowed to access a shared folder or install software.

**Directory Structure:** Everything in AD — users, devices, and resources — is organized in a structured way, like folders within folders. These are called Organizational Units (OUs) and help admins apply specific rules to different departments or teams.

**Group Policies:** Admins can define security rules (like password policies or Restrict/Allow Apps, Network Settings, Startup/Shutdown Scripts) and apply them to groups of users through something called Group Policy Objects (GPOs).

**Domain Controllers:** These are the servers that run AD DS (Active Directory Directory Services). When you log in or request access, you’re talking to one of these servers.

Put simply, Active Directory creates a centralized system where user identities and permissions are stored and managed, helping organizations stay organized, secure, and in control.


# What are the Main Components of Active Directory?

Active Directory depends on Domain Controllers and Sites as its core components to deliver operational management of network resources effectively.

### Domain Controllers

The servers known as Domain Controllers (DCs) deploy Active Directory Domain Services (AD DS) to offer authentication and authorization functions as well as directory replication capabilities. Every Domain Controller maintains an exact duplicate of the Active Directory database that contains data about users and computers, and group entities spread across the domain. The modifications performed on a single Domain Controller, including passwords or user accounts, will distribute these changes to every Domain Controller in the system for maintaining uniformity. Organizations implement several DCs because this strategy provides both redundancy and reliability to network operations. Specialized DC roles consist of Global Catalog Servers that maintain a complete domain object storage with partial object storage from other domains in the forest to support cross-domain searches.

### Sites

Active Directory Sites correspond to network IP subnets, maintaining strong communication connections. Active Directory sites enable domain controllers to achieve efficient replication of data between different network locations through proper data synchronization across distant sites. The user experience gains improvement through site functionality because sites send authentication requests to domain controllers within nearest reach, thus decreasing response delays. Active Directory administrators utilize sites to schedule replication activities effectively and control network bandwidth costs, specifically during high-demand times.

These components unite to maintain Active Directory’s operational efficiency within complex organizations that operate extensive network systems.

# Source:
https://www.lepide.com/blog/what-is-active-directory/