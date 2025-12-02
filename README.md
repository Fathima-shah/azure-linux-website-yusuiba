1. Provisioned Azure Virtual Machine

Created a new Resource Group (RG)

Deployed an Ubuntu Server VM in UK South region

Chosen size: 16 GiB memory

Authentication: Username: vmuser, password-based login

Disabled Boot Diagnostics

Completed deployment after review

2. Connected to the Linux Server

Used PuTTY to SSH using VM’s Public IP

Logged in with username & password

Updated server packages:

sudo apt update
sudo apt upgrade

3. Installed & Configured Web Server

Installed required web server packages (Apache)

Opened the default HTML file:

vim /var/www/html/index.html


Removed default content and pasted the new HTML template

Saved file (:wq)

Updated Network Inbound Rules to allow HTTP (Port 80)

Verified website using VM Public IP

4. Purchased & Configured Custom Domain

Purchased domain yusuiba.shop from Hostinger

Created DNS Zone in Azure

Added A-Record pointing to VM Public IP

Copied Nameservers (NS) from Azure DNS

Updated nameservers in Hostinger DNS panel

Allowed 24 hrs for DNS propagation

Website successfully mapped to custom domain:
www.yusuiba.shop