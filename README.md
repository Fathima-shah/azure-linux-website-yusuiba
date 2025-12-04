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

- VM Provisioning
![Create Resource Group](images/01_VM_Provision_create_resource_group.png)
![Boot Diagnostics Disabled](images/01_boot_diagnosis_disabled.png)
![Username & Password Setup](images/01_create_password_username.png)
![VM Deployment](images/01_deployed_vm.png)
![Navigate to Resource Group](images/01_go_to_resourcegroup.png)
![Azure Login](images/01_login_azure.png)
![Review & Create VM](images/01_review_create_vm.png)

- SSH Connection to Linux Server
![Open PuTTY & Enter IP](images/02_SSH_Connection_open_putty_enter_public_ip.png)
![PuTTY Login](images/02_putty_login.png)
![PuTTY Username & Password](images/02_putty_login_username_password.png)
![Run apt update](images/02_run_apt_update.png)
![Run apt upgrade](images/02_run_apt_upgrade.png)
![Switch root user](images/02_sudo_su_root.png)

- Apache Installation & Website Setup
![Apache Installation](images/03_apache_installation_install_apache.png)
![Copy HTML Template](images/03_copy_html_content_from_tooplate.png)
![Delete Default HTML Content](images/03_delete_default_HTML_content.png)
![HTML Content Updated](images/03_html_content.png)
![Open index.html](images/03_open_index_html.png)
![Allow Port 80](images/03_networ_change_port.png)

- DNS & Custom Domain Configuration
![DNS Propagation Check](images/04_DNS_propogation_check.png)
![Add A Record VM IP](images/04_add_recordset_vm_public_ip.png)
![Copy Azure Nameservers](images/04_copy_Azure_nameservers.png)
![Create DNS Zone](images/04_create_azure_DNZ_zone.png)
![DNS Record Creation Review](images/04_review_create_DNS.png)
![Update Nameservers in Hostinger](images/04_update_NS_in_hostinger.png)
![Custom Domain Purchase](images/04_custom_domain_domain_dashboard_purch.png)
![Nameserver Changed](images/04_nameserver_changed.png)
![Final DNS Setup](images/04_create_DNS.png)


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

