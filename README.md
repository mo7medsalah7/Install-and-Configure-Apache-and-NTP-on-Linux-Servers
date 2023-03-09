# Install-and-Configure-Apache-and-NTP-on-Linux-Servers

# Description
## This is an Ansible Project wehere you can install web server `httpd` or `apache2`

# Roles
## I used my roles that are hosted on my **Github** account.
## The roles in this project are listed below.
- ansible_apache_role:- **https://github.com/mo7medsalah7/ansible_apache_role**
- ansible_ntp_role:- **https://github.com/mo7medsalah7/ansible_ntp_role**

## How To Use Roles 
- in `roles/requirements.yml`

```
roles:
  - src: https://github.com/mo7medsalah7/ansible_apache_role
    scm: git
    version: main
  - src: https://github.com/mo7medsalah7/ansible_ntp_role
    scm: git
    version: main
```

# Inventory.
## The managed/remote hosts are listed in the file `inventories/hosts`

# Installation
## - Install Roles with Ansible Galaxy
`ansible-galaxy install -r roles/requirements`

`ansible-playbook -i inventories/hosts apache-ntp-playbook.yml`





