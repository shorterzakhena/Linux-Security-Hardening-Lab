**Step By Step Instructions**

**1. System Information**

I started by checking information about my Ubuntu system.

Commands I used:

- lsb_release -a
- whoami**
- hostname
- uname -a

These commands showed me information about my Ubuntu version, username, hostname, and system.

**Screenshot: 01_system_info.png**

**2. User and Group Security**

Next, I created a security group and a user for the lab. I then checked that the user and group were set up correctly.

Commands I used:

- sudo addgroup securitylab
- sudo adduser LABUSER
- sudo usermod -aG securitylab LABUSER
- id LABUSER
- getent group securitylab

**Screenshot: 02_users_groups.png**

**3. File Permissions**

I created a test file and practiced changing its permissions and ownership.

Commands I used:

- mkdir -p ~/security-lab-demo
- echo 'Linux security hardening lab' > ~/security-lab-demo/security.txt
- ls -l ~/security-lab-demo/security.txt
- chmod 640 ~/security-lab-demo/security.txt
- sudo chown $USER:securitylab ~/security-lab-demo/security.txt
- ls -l ~/security-lab-demo/security.txt

I used chmod 640 to give the owner read and write permissions, the group read permission, and no permissions to everyone else.

**Screenshot: 03_file_permissions.png**

**4. Firewall Configuration**

I used UFW to check and configure the Ubuntu firewall.

Commands I used:

- sudo ufw status verbose
- sudo ufw default deny incoming
- sudo ufw default allow outgoing
- sudo ufw allow ssh
- sudo ufw enable
- sudo ufw status verbose

After making the changes, I checked the firewall again to make sure it was active and the rules were showing.

**Screenshot: 04_firewall.png**

**5. SSH Security**

I checked the SSH service and reviewed the SSH configuration.

Commands I used:

systemctl status ssh --no-pager

I also backed up the SSH configuration before making changes:

sudo cp /etc/ssh/sshd_config /etc/ssh/sshd_config.backup

I checked the configuration and made sure it was valid before restarting the SSH service.

- sudo sshd -t
- sudo systemctl restart ssh
- sudo systemctl status ssh --no-pager

**Screenshot: 05_ssh_security.png**

**6. Security Audit**

For the last part of the lab, I performed some basic security checks on the Ubuntu system.

Commands I used:

- sudo ufw status verbose
- systemctl --type=service --state=running --no-pager
- ss -tuln
- sudo find / -xdev -type f -perm -4000 2>/dev/null
- sudo journalctl -p warning -b --no-pager

These commands allowed me to check the firewall, running services, listening ports, privileged files, and system warnings.

**Screenshot: 06_security_audit.png**

Author: Zakhena Shorter IT Professional | Recent IT Graduate
