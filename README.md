<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1: Azure Setup:

Sign in to your Azure portal.
Create a new Virtual Network (VNet) for your AD infrastructure.
Set up a Virtual Network Gateway if connecting to on-premises infrastructure.
- Step 2: Azure Virtual Machines:

Deploy Windows Server VMs in Azure for your Domain Controllers (DCs).
Ensure they have static IP addresses and are part of the Azure VNet.
- Step 3: Network Configuration:

Configure Azure DNS to point to your Azure VMs as DNS servers.
Ensure proper network security group rules for communication.
- Step 4: Active Directory Installation:

Install Active Directory Domain Services (AD DS) on Windows Server VMs.
Promote these VMs to domain controllers in a new or existing forest/domain.
-Step 5: DNS Configuration:

Configure DNS zones and records for your domain within AD DS.
Ensure that DNS settings on VMs point to each other for resolution.
-Step 6: Site-to-Site VPN (Optional):

Establish a VPN connection to your on-premises network, if required.
Configure proper routing and connectivity between on-premises and Azure.
-Step 7: Backup and Recovery:

Implement regular backups of Active Directory data.
Ensure a disaster recovery plan is in place.
-Step 8: Security and Access Control:

Implement Azure AD Connect to synchronize on-premises and Azure AD identities.
Set up proper access controls and permissions within Azure.
-Step 9: Monitoring and Maintenance:

Implement monitoring and alerting for AD health.
Regularly apply updates and patches to Windows Server VMs.
-Step 10: Documentation:

Document your configuration, including IP addresses, DNS settings, and access controls.

<h2>Deployment and Configuration Steps</h2>

<p>
<img src= "https://i1.wp.com/theithollow.com/wp-content/uploads/2016/07/AzureNet0.png?fit=1056%2C373&ssl=1"/>
</p>
<p>
1.) Azure Setup:
Create an Azure Virtual Network (VNet).
Establish a VPN or ExpressRoute connection to on-premises if needed.
2.) Azure Virtual Machines (VMs):
Deploy Windows Server VMs for Domain Controllers (DCs).
Assign static IP addresses within the Azure VNet.
</p>
<br />

<p>
<img src="https://arminreiter.com/wp-content/uploads/2016/12/20161219_01_overview-1024x659.png"/>
</p>
<p>
1.) Network Configuration:
Configure Azure DNS to point to DCs as DNS servers.
Set up Network Security Groups for VM communication.
2.) Active Directory Installation:
Install Active Directory Domain Services (AD DS) on VMs.
Promote VMs to domain controllers.
3.) DNS Configuration:
Create DNS zones and records for the domain in AD DS.
Ensure VMs use each other as primary and secondary DNS.

</p>
<br />

<p>
<img src="https://learn.microsoft.com/en-us/azure/role-based-access-control/media/shared/rbac-scope.png"/>
</p>
<p>
4.) Access Control (Optional):
Implement Azure AD Connect for identity synchronization.
Set up proper access controls and permissions in Azure.
5.) Monitoring and Maintenance:
Establish monitoring and alerts for AD health.
Regularly apply updates and patches to Windows Server VMs.
6.) Documentation:
Document network settings, DNS configurations, and access controls.
</p>
<br />
