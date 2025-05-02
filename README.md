Ansible Role for Fail2Ban
=======================

Ansible Role for Fail2Ban

Requirements
------------

This role require Ansible 2.0 or higher.

This role was designed for Ubuntu and Amazon Linux

Role Variables
--------------

fail2ban_sshd_bantime - How long to ban offending IP
fail2ban_sshd_findtime - Time period to consider an attack
fail2ban_sshd_maxretry - Number of consecutive failed attempts
fail2ban_sshd_bantime_increment - Bool to increment bantime for repeat offenders
fail2ban_sshd_whitelist - List of IPs to whitelist
fail2ban_iptables_sshd_action - Fail2Ban action for iptables
fail2ban_firewalld_sshd_action - Fail2Ban action for firewalld