Vagrant Commands and Workflow
vagrant global-status: Displays the status of all VMs.
vagrant up: Starts the specified VM.
vagrant halt: Powers off the specified VM.
vagrant reload: Applies configuration changes in the Vagrantfile to the running VM without destroying it.
vagrant destroy: Powers off and deletes all files associated with the VM.
VM Configuration
To modify settings such as IP address, RAM, and CPU, update the Vagrantfile accordingly.

Directory Syncing
A shared directory enables file synchronization between the host machine and the VM, allowing seamless access to files on both systems.
Example:
![image](https://github.com/user-attachments/assets/390439e9-7dc7-45e9-b396-752e4e43043e)

Provisioning / Bootstrapping
Provisioning allows you to automate initial setup by running a specified script when the VM is powered on for the first time. Add the script to the Vagrantfile under the provision section to automate setup tasks.

Example: For a finance template setup, download the "Mini Finance HTML Template" by Tooplate using wget to the /tmp/ directory, unzip it, and move it to /var/www/httpd to prepare for serving.

To host a website using HTTPD, place the project files in /var/www/httpd, then access the private IP in a browser to render index.html.

Automation
To automate the full setup, include all necessary commands in the provisioning section of the Vagrantfile.

WordPress Setup
For WordPress installation, you can follow the manual setup guide from Ubuntu or use the automated WordPress IAS option.

Managing Multiple VMs
To run multiple VMs within a single Vagrant project, define each VM separately within the Vagrantfile following the appropriate syntax. Use vagrant halt <vm_name> and vagrant ssh <vm_name> to control individual VMs without impacting others.
