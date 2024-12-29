# Ansible-Playbooks
📘 Ansible Playbook: Server Maintenance and Updates

📑 Overview

This Ansible Playbook automates the maintenance and updates of Linux servers. It ensures that package lists are updated, essential software packages are installed, and kernel updates are completed with a server reboot if necessary.

⚙️ Playbook Features

Update Package Lists: Refreshes the APT package cache.

Upgrade System Packages: Fully upgrades installed packages.

Install Software: Installs essential software packages (e.g., duf, needrestart, htop).

Check for Kernel Updates: Checks if a new kernel is installed.

Server Reboot: Reboots the server if necessary.

Monitor Reboot: Ensures the server is available after reboot.

System Status Check: Displays the server's uptime.

🚀 How to Use the Playbook

Requirements

Ansible must be installed on the control machine.

SSH access to target servers must be configured.

An Ansible inventory file with target servers must exist.

Run the Playbook

ansible-playbook -i inventory.ini playbook.yml

-i inventory.ini: Specifies the inventory file.

playbook.yml: The name of the playbook file.

Example Inventory File (inventory.ini)

[all]
server1.example.com
server2.example.com

Enable Debugging

Add the -v option to display debug information:

ansible-playbook -i inventory.ini playbook.yml -v

🛡️ Important Notes

Always run the playbook on a test system first.

Ensure open connections and running services are secured before reboot.
