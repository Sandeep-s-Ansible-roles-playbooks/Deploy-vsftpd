This Ansible playbook automates the installation and service management of a specified package (vsftpd) on both RPM-based (e.g., Red Hat, CentOS, AlmaLinux) and DEB-based (e.g., Ubuntu, Debian) Linux systems.

What This Playbook Does:
1. Gathers system facts to determine the OS family.
2. Installs the package (vsftpd) using the correct package manager:
  a. apt for Debian-based systems
  b. yum for Red Hat-based systems
3. Displays status messages indicating whether the package was newly installed or already present.
4. Checks if the service is running using systemctl.
5. Starts the service only if it is not already running.
6. Ensures the service is enabled to start automatically on boot.

Usage: ansible-playbook -i hosts --ask-pass --become --ask-become-pass deploy_vsftpd.yml
Note: Provide passwords for both the user and the root account.
