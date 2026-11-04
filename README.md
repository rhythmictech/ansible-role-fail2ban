Ansible Role for Fail2Ban
=======================

Ansible Role for Fail2Ban

Requirements
------------

This role require Ansible 2.0 or higher.

This role was designed for Ubuntu and Amazon Linux

The firewall fail2ban bans with depends on the platform:

| Platform | Firewall | Notes |
|---|---|---|
| Ubuntu, EL < 8, Amazon Linux 2 | iptables | AL2 installs fail2ban from EPEL |
| EL >= 8 | firewalld | firewalld is installed and started |
| Amazon Linux 2023 | nftables | Installs `fail2ban-server` from the AL2023 repos, not the `fail2ban` meta-package (which pulls in firewalld). sshd is read from the journal. |

Role Variables
--------------

fail2ban_sshd_bantime - How long to ban offending IP

fail2ban_sshd_findtime - Time period to consider an attack

fail2ban_sshd_maxretry - Number of consecutive failed attempts

fail2ban_sshd_bantime_increment - Bool to increment bantime for repeat offenders

fail2ban_sshd_whitelist - List of IPs to whitelist

fail2ban_iptables_sshd_action - Fail2Ban action for iptables

fail2ban_firewalld_sshd_action - Fail2Ban action for firewalld

fail2ban_nftables_sshd_action - Fail2Ban action for nftables
