linux_users
=========

This role can be used for configure linux users with sudo nopasswd.
1) create user
2) set authorized_key to allow ssh based logins
3) add user to sudoers with nopass
4) disable password authentication
5) disable root ssh access

Requirements
------------

This role requires Ansible 1.2 or higher, and platform requirements are listed in the metadata file.

Role Variables
--------------

linux_user: admin
linux_passwd: <your_password>
key_path: '/home/admin/.ssh/id_rsa.pub'

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: linux_users, linux_user: admin, linux_passwd: <your_password>, key_path: '/home/admin/.ssh/id_rsa.pub' }

License
-------

MTP

Author Information
------------------

Aleksey Demidov