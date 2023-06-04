<h1>Microsoft Azure - Creating a Virtual Machine</h1>

<h2>Table of Contents</h2>
1. <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#description"> Description </a> <br />
2. <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#virtualbox-install-walk-through"> VirtualBox Install Walk-Through </a> <br />
3. <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#kali-linux-install-walk-through"> Kali Linux Install Walk-Through </a> <br />
4. <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#troubleshooting-guide"> Troubleshooting Guide </a> <br />

<h2>Description</h2>
The objective of this project is to create a Virtual Machine (VM) using Microsoft Azure, a cloud computing platform. The VM will provide a scalable and flexible environment for hosting applications and managing resources in a cloud-based infrastructure. <br />

The project will follow a step-by-step approach to ensure a smooth and successful creation of the VM. The key steps involved in the process are as follows: 
<br />

Define Requirements:
<br />

Identify the purpose of the VM and the specific requirements, such as operating system, computing power, storage capacity, and network configuration. <br />
Determine the appropriate Azure region and availability zone to host the VM based on latency, compliance, and data residency requirements. <br />
Azure Account Setup: <br />
<br />

Create an Azure account if not already available. <br />
Set up the necessary subscription and resource group to organize and manage Azure resources effectively. <br />
VM Configuration: <br />
<br />

Select the appropriate VM size based on the workload requirements, considering factors like CPU, RAM, and storage capacity. <br />
Choose the desired operating system image from Azure's marketplace, such as Windows Server or Linux distributions. <br />
Configure additional options, including networking, storage, and availability sets, as per the project requirements. <br />
Network Configuration: <br />
<br />

Define the virtual network (VNet) to which the VM will be connected. <br />
Specify the subnet within the VNet to allocate IP addresses for the VM. <br />
Configure network security groups (NSGs) to control inbound and outbound traffic to the VM. <br />
Set up virtual network peering or VPN connections if necessary. <br />
Storage Configuration: <br />
<br />

Determine the storage requirements for the VM, including the type of storage account (Standard or Premium) and the size of the virtual hard disk (VHD). <br />
Define the storage redundancy option (locally redundant storage or geo-redundant storage) for data protection. <br />
Configure disk caching, encryption, and backup options based on the project's security and data management needs. <br />
Security and Access Management: <br />
<br />

Define access control policies for the VM by configuring Azure Active Directory (AAD) integration, role-based access control (RBAC), and virtual machine access extensions. <br />
Enable monitoring and logging services, such as Azure Monitor and Azure Security Center, to ensure the VM's security and compliance. <br />
VM Deployment: <br />
<br />

Initiate the VM deployment process within the Azure portal or through Azure CLI, PowerShell, or Azure Resource Manager (ARM) templates. <br />
Monitor the deployment progress and resolve any errors or issues that may arise during the provisioning process. <br />
VM Management: <br />
<br />

Install necessary software and applications on the VM. <br />
Implement ongoing management tasks, including scaling, updating, and patching the VM. <br />
Implement automated backup and disaster recovery mechanisms, leveraging Azure services like Azure Backup and Azure Site Recovery. <br />
Testing and Validation: <br />
<br />

Verify the successful deployment and accessibility of the VM. <br />
Perform testing and validation procedures to ensure the VM meets the defined requirements and performs as expected. <br />
Documentation and Handover: <br />
<br />

Document the VM configuration details, including the chosen settings, networking setup, storage configuration, security measures, and access controls. <br />
Prepare user documentation and guidelines for future reference. <br />
Conduct a knowledge transfer session with relevant stakeholders to ensure smooth handover and operational continuity. <br />
By following these steps, this project aims to deliver a fully functional and reliable VM within Microsoft Azure, meeting the specified requirements and providing a scalable infrastructure for hosting applications and managing resources in the cloud. <br />

<h3>Minimum Hardware Requirements</h3>

- <b>Processor: A dual-core processor or higher is recommended. However, a single-core processor can suffice for basic usage.</b> 
- <b>RAM: At least 2 GB of RAM is required for running Kali Linux smoothly. However, it is recommended to have 4 GB or more for better performance, especially when running resource-intensive security tools.</b>
- <b>Storage: A minimum of 20 GB of free disk space is required to install Kali Linux. However, it is advisable to allocate more space (at least 40 GB or higher) to accommodate additional software packages, tools, and data.</b>
- <b>Graphics: Any graphics card that supports the host operating system is sufficient for running Kali Linux in a virtual machine.</b>
- <b>Network: A network interface card (NIC) is required for network connectivity within the Kali Linux VM. Oracle VM VirtualBox allows you to configure network adapters, including NAT, Bridged, or Host-only networking, based on your requirements.</b>
- <b>Host Machine: The host machine should meet the minimum requirements for running Oracle VM VirtualBox itself. Refer to the VirtualBox documentation for specific details regarding the host machine's operating system, processor, RAM, and storage requirements.</b>

<i>It is important to note that the above specifications represent the minimum requirements, and for a better experience, it is recommended to have higher specifications, especially when working with resource-intensive tasks or running multiple virtual machines simultaneously. </i>

<h3>Languages and Utilities Used</h3>

- <b>VirtualBox 7.0.8 Platform Packages</b> (Windows hosts)
- <b>VirtualBox 7.0.8 Oracle VM VirtualBox Extension Pack</b> (All supported platforms)
- <b>Kali Linux - Installer Images</b> (64-bit Installer)
- <b>Bash</b>
- <b>BIOS</b>

<h3>Environments Used </h3>

- <b>Windows 10</b> (22H2 / OS Build 19045.2965)
- <b>Kali Linux</b> (2023.2)


<h2>VirtualBox Install Walk-Through:</h2>

<p align="center">
 <i>If you already have VirtualBox installed, please skip ahead to <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#kali-linux-install-walk-through"> Kali Linux Install </a>. </i> <br />
 <i>Back to <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#kali-linux---initial-setup--troubleshooting-guide-windows-10"> main </a></i> <br />
 <br />
 <br />
 Go to <a href="https://www.virtualbox.org/wiki/Downloads">VirtualBox</a>.<br /> 
 Download <b>VirtualBox 7.0.8 Platform Packages</b> (Windows hosts) and <b>VirtualBox 7.0.8 Oracle VM VirtualBox Extension Pack</b> (All supported platforms).
<br/>
<img src="https://i.imgur.com/YIHswd0.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 Go to Downloads Folder. Run <b>VirtualBox-7.0.8-156879-Win.exe.</b><br/>
<img src="https://i.imgur.com/0PTxQKW.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 In the <b>Oracle VM VirtualBox Setup Wizard</b>, Click <b>Next</b>.<br/>
<img src="https://i.imgur.com/o4EZXBL.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 For the <b>Custom Setup</b>, leave Location as <b>C:\ProgramFiles\Oracle\VirtualBox\</b> and press <b>Next</b>.<br/>
<img src="https://i.imgur.com/tJ4t5U3.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 Proceed with the installation by pressing <b>Next</b>.<br/>
 <i>Warning: You will be disconnected from your Network during a brief portion of this installation. </i><br />
 <i>Warning: If you are Missing Dependencies Python Core / win32api, refer to the <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#missing-dependencies-python-core--win32api">Troubleshooting Section</a>.</i><br />
 <img src="https://i.imgur.com/2y8DnD4.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 At the <b>Ready to Install</b> window, press <b>Install</b>, allow the install, and let the installation complete.<br />
 <i>You may receive a prompt for a network/usb adapter during this process. Make sure to press Yes when this occurs.</i><br />
 <img src="https://i.imgur.com/QVwKIkv.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 Once the installation is complete, leave the checkmark as checked and press <b>Finish</b>.<br />
 <img src="https://i.imgur.com/iC60Y7u.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 Now, we will be installing the extension pack we downloaded earlier onto <b>VirtualBox</b>.<br />
 In <b>Oracle VM VirtualBox Manager</b>, go to <b>Tools</b>, click on the blue squares, and select the <b>Extensions</b> tab. <br />
 <img src="https://i.imgur.com/A3e0HW6.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 Click on <b>Install</b> and select the <b>Oracle_VM_VirtualBox_Extension_Pack-7.0.8.vbox-extpack</b> file. Press <b>Open</b>.<br />
 <img src="https://i.imgur.com/8rDPIwY.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 Click on <b>Install</b>, scroll down to the <b>VirtualBox License</b>, press <b>I Agree</b>.<br />
 <img src="https://i.imgur.com/JZLJbYX.png" height="60%" width="60%" alt="VirtualBox Install Steps"/><br />
 <img src="https://i.imgur.com/7SFC5FV.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 The Extension Pack has been successfully installed and <b>Oracle VM VirtualBox</b> is ready for use.<br />
 <img src="https://i.imgur.com/bNKEvgE.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
</p>

<h2>Kali Linux Install Walk-Through:</h2>

<p align="center">
<i>Back to <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#kali-linux---initial-setup--troubleshooting-guide-windows-10"> main </a></i> 
<br />
<br />
 Go to <a href="https://www.kali.org/get-kali/#kali-installer-images">Kali Installer Images</a>. Select <b>64-bit</b> and click Download icon on <b>Installer</b><br />
 <i>Depending on your ISP, this process may take an hour or more. It is recommended to let this run in the background until completion.</i>
<img src="https://i.imgur.com/hEV3UI1.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 After the download completes, run <b>Oracle VM VirtualBox.</b> In <b>Oracle VM VirtualBox Manager</b>, click <b>New</b>.<br/>
<img src="https://i.imgur.com/V8jLjNL.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Create Virtual Machine</b>, press <b>Guided Mode</b>, enter KaliLinux into the <b>Name</b> field. For <b>ISO Image</b>, select <b>Other</b> and Select <b>kali-linux-2023.2a-installer-amd64.iso</b><br />
 <b>Type</b> should be set to Linux and <b>Version</b> should be set Ubuntu (64-bit). Press <b>Next</b>.<br/>
<img src="https://i.imgur.com/wDFmqzZ.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Hardware</b>, set <b>Base Memory</b> to at least 4096 MB and set <b>Processors</b> to 4 CPUs. Press <b>Next</b>.<br/>
<img src="https://i.imgur.com/Lnjw6Wr.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Virtual Hard disk</b>, select <b>Create a Virtual Hard Disk Now</b> and set <b>Disk Size</b> to at least 20 GB. Press <b>Next</b>.<br />
 <img src="https://i.imgur.com/rtoSkK0.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Summary</b>, review the items and press <b>Finish</b>.<br />
 <img src="https://i.imgur.com/QL98zmI.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Oracle VM VirtualBox Manager</b>, select <b>KaliLinux</b> and select <b>Settings</b>.<br />
 <img src="https://i.imgur.com/sOHN68b.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Settings</b>, select <b>Display</b> and set <b>Video Memory</b> to its Maximum Value. Press <b>OK</b>.<br />
 <img src="https://i.imgur.com/jb4A7I5.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Make sure <b>KaliLinux</b> is selected and press <b>Start</b>.<br />
 <img src="https://i.imgur.com/aujmH1S.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Kali Linux</b>, select <b>Graphical Install</b> and hit <i>Enter</i>.<br />
 <img src="https://i.imgur.com/hmXflQd.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/><br />
<br />
<br />
 Select your preferred language and hit <i>Enter</i>.<br />
 <img src="https://i.imgur.com/Mr9kkyo.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Select the location that matches your time zone and hit <i>Enter</i>.<br />
 <img src="https://i.imgur.com/yjEs3XP.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Select your preferred keyboard configuration and hit <i>Enter</i>. <br />
 <img src="https://i.imgur.com/WAlmTn9.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Once you reach <b>Configure the network</b>, leave <b>Hostname</b> as default and hit <i>Enter</i>. <br />
 <img src="https://i.imgur.com/Nz2lMyf.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 For <b>Domain name</b>, you can leave the field blank. Hit <i>Enter</i>.<br />
 <img src="https://i.imgur.com/d7cKnWb.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Set up users and passwords</b>, set <b>Full name for the new user</b> as a custom user name. Hit <i>Enter</i>.<br />
 <i>Warning: It may be difficult to change this later, so make sure it is something you will remember!</i><br />
 <img src="https://i.imgur.com/e5nrgoS.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 For <b>Username for your account</b>, a username will be generated from what you typed earlier. Leave as is and hit <i>Enter</i>.<br />
 <i>Warning: It may be difficult to change this later, so make sure it is something you will remember!</i><br />
 <img src="https://i.imgur.com/S9Lw0sk.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Create a password and enter the password in both of the available fields. Press <b>Continue</b>.<br />
 <i>Warning: It may be difficult to change this later, so make sure it is something you will remember!</i><br />
 <img src="https://i.imgur.com/xK5l7mT.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Configure the clock</b>, choose your corresponding time zone and hit <i>Enter</i>. <br />
 <img src="https://i.imgur.com/TvHuh3G.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Partition disks</b>, select <b>Guided - use entire desk</b> and hit <i>Enter</i>. <br />
 <img src="https://i.imgur.com/RDhHNN5.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 There should only be one disk to select to partition. Hit <i>Enter</i>. <br />
 <img src="https://i.imgur.com/E4WfRn8.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Select <b>All files in one partition (recommended for new users)</b> and hit <i>Enter</i>. <br />
 <img src="https://i.imgur.com/kLi93zf.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Select <b>Finish partitioning and write changes to disk</b> and hit <i>Enter</i>. <br />
 <img src="https://i.imgur.com/NoiZ6BW.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Select <b>Yes</b> for <b>Write the changes to disks?</b> and hit <i>Enter</i>. <br/>
 <img src="https://i.imgur.com/ZMSX9Xl.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Software selection</b>, leave the default selections and press <b>Continue</b>. <br />
 <img src="https://i.imgur.com/mYxh6Ps.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Install the GRUB boot loader</b>, select <b>Yes</b> and press <b>Continue</b>. <br />
 <img src="https://i.imgur.com/d0U9A8y.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Select the first device that appears under <b>Enter device manually</b>. Press <b>Continue</b>. <br />
 <img src="https://i.imgur.com/wDOnTBj.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Kali Linux has now been completely installed for use through <b>Oracle VM VirtualBox</b>. Press <b>Continue</b> to reboot the VM. <br />
 <img src="https://i.imgur.com/nbOR9vl.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>

</p>

<h2>Troubleshooting Guide:</h2>
<p align="center"> <i>Back to <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#kali-linux---initial-setup--troubleshooting-guide-windows-10"> main </a></i> </p>
<br />
 
<h4>Missing Dependencies Python Core / win32api</h4>
<p align="center">
 Install Python from <a href="https://www.python.org/downloads/">here</a> <br />
 Once Python is installed, open cmd and execute the following command: 
<br />
 <i> pip install pywin32 </i>
<br />
 You might have to update pip during this process. To update pip, run the following command in cmd:
<br />
 python.exe -m pip install --upgrade pip
<br />
 You should now be able to proceed with the installations without any further issues.
<br />
 
</p>
<h4>"Not in a hypervisor partition (HVP=0)(VERR_NEM_NOT AVAILABLE)" Error</h4>

<p align="center">
 You need to enable virtualization on your CPU through the BIOS settings. Refer to this <a href="https://recoverit.wondershare.com/partition-tips/not-in-a-hypervisor-partition.html">guide</a>.
<br />
</p>

<h4>Updating Linux through Terminal</h4>
<p align="center">
 Enter the following commands into the terminal: <br />
 <i>sudo apt-get update</i> <br/>
 <i>sudo apt update</i> <br />
 <i>sudo apt upgrade</i> <br />
 Once all of these commands have completed, Linux should be up-to-date. <br />
</p>



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
