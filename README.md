C#  Website Hosting on Azure Linux VM (Yusuiba Project)

This project demonstrates hosting a static website on an **Ubuntu Linux Virtual Machine** in Microsoft Azure and configuring a **custom domain (yusuiba.shop)** purchased from Hostinger.  

---

##  **1. Provisioned Azure Virtual Machine**

- Created a new **Resource Group (RG)**
- Deployed an **Ubuntu Server** VM in **UK South**
- VM Size: **16 GiB memory**
- Authentication:
  - **Username:** vmuser  
  - **Password-based login**
- Disabled **Boot Diagnostics**
- Successfully deployed the VM

---

##  **2. Connected to the Linux Server**

- Connected using **PuTTY** with VM’s **Public IP**
- Logged in with username & password  
- Updated server packages:

```bash
sudo apt update
sudo apt upgrade
```

---

##  **3. Installed & Configured Web Server**

- Installed Apache web server
- Opened the default HTML file:

```bash
vim /var/www/html/index.html
```

- Deleted default content  
- Pasted the HTML template downloaded from **tooplate.com**
- Saved changes using `:wq`
- Allowed HTTP traffic in **Azure Network Security Group** (Port 80)
- Verified website in browser using Public IP

---

##  **4. Purchased & Configured Custom Domain**

- Purchased domain: **yusuiba.shop** from Hostinger
- Created DNS Zone in Azure
- Added **A Record** pointing to VM Public IP
- Copied required **Name Server (NS)** values
- Updated nameservers inside Hostinger DNS panel
- Waited ~24 hours for DNS propagation
- Website successfully mapped:
- 
###  **https://www.yusuiba.shop**
Allowed 24 hrs for DNS propagation


##  **Project Screenshots **

-VM Provisioning
![Create Resource Group](01_VM_Provision_create_resource_group.png)
![Boot Diagnostics Disabled](01_boot_diagnosis_disabled.png)
![Username & Password Setup](01_create_password_username.png)
![VM Deployment](01_deployed_vm.png)
![Navigate to Resource Group](01_go_to_resourcegroup.png)
![Azure Login](01_login_azure.png)
![Review & Create VM](01_review_create_vm.png)

-SSH Connection to Linux Server
![Open PuTTY & Enter IP](02_SSH_Connection_open_putty_enter_public_ip.png)
![PuTTY Login](02_putty_login.png)
![Username & Password Login](02_putty_login_username_password.png)
![Run apt update](02_run_apt_update.png)
![Run apt upgrade](02_run_apt_upgrade.png)
![Switch to root user](02_sudo_su_root.png)

-Apache Installation & Website Setup
![Apache Installation](03_apache_instalalion_install_apache.png)
![HTML Content Updated](03_copy_html_content_from_too_plate.png)
![Delete Default HTML](03_delete_default_HTML_content.png)
![Open index.html](03_open_index_html.png)
![Allow Port 80](03_networ_change_port.png)
![Final HTML Content](03_html_content.png)

-DNS & Custom Domain Configuration
![DNS Propagation Check](04_DNS_propogation_check.png)
![Add A Record VM IP](04_add_recordset_vm_public_ip.png)
![Copy Azure Nameservers](04_copy_Azure_nameservers.png)
![Create DNS Zone](04_create_azure_DNZ_zone.png)
![Custom Domain Purchase](04_custom_domain_domain_dashboard_purchase.png)
![Nameserver Changed](04_nameserver_changed.png)
![Review DNS Setup](04_review_create_DNS.png)
![Update Nameservers in Hostinger](04_update_NS_in_hostinger.png)


# **Skills Gained**

- Azure Virtual Machines (Linux)
- SSH using PuTTY
- Apache Web Server Hosting
- DNS Zone Management
- Custom Domain Mapping
- Azure Networking (NSG rules)
- Linux server configuration
- Website deployment on cloud

##  **Status**
Project Completed ✔
Website successfully mapped to custom domain:

www.yusuiba.shop


