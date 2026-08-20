**Project Description**

For this lab, I worked with an Ubuntu Linux virtual machine in Oracle VirtualBox. The goal of the lab was to practice some basic Linux security and system administration tasks.
I worked with users and groups, file permissions, the firewall, SSH, and basic security checks. I also took screenshots of my work and organized everything into a GitHub repository.

**Lab Environment**
- Ubuntu Linux
- Oracle VirtualBox
- Ubuntu Terminal
- GitHub

**Goals**

The goals of this lab were to:

- Check and document my Linux system
- Create a user and group
- Practice file permissions
- Configure the firewall
- Check SSH security
- Perform a basic security audit
- Take screenshots of my work
- Document the commands I used
- Organize the project on GitHub

**What I Did**

- Set up an Ubuntu Linux security lab using Oracle VirtualBox.
- Checked and documented my Ubuntu system information.
- Created a security-lab user and group.
- Created a test file and changed its permissions and ownership.
- Configured the UFW firewall.
- Checked the SSH service and reviewed the SSH configuration.
- Performed basic security checks on the Linux system.
- Took screenshots to document each part of the lab.
- Organized the commands and screenshots into my GitHub repository.

**Security Changes**

- Created a separate user and security group for the lab.
- Set file permissions using **chmod** 640.
- Set file ownership and group ownership for the test file.
- Configured UFW to deny incoming connections by default.
- Allowed outgoing connections through the firewall.
- Allowed SSH through the firewall.
- Reviewed the SSH configuration and created a backup before making changes.

**Testing / Verification**

I checked my work after making the security changes to make sure everything was working correctly.

- Used id and **getent** group to verify the user and group.
- Used **ls -l** to verify file permissions and ownership.
- Used **sudo ufw**status verbose to verify the firewall.
- Used **sudo sshd -t** to check the SSH configuration.
- Used **systemctl** status **ssh** to check the SSH service.
- Used **ss -tuln** to check listening network ports.
- Checked running services and system warnings as part of the security audit.

**Skills Demonstrated**

- Linux system administration
- Ubuntu Linux
- User and group management
- File permissions
- Firewall configuration
- SSH
- Security auditing
- Linux command line
- System troubleshooting
- Technical documentation
GitHub
