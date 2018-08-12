Ansible Role: Inventory known hosts
=========

This role is meant to add the ssh host keys to the local known hosts file. WARNING: This enables man-in-the-middle attacks if you do not properly verify the keys out of band.

Requirements
------------

* Ansible 1.9+
* openssh-clients (ssh-keyscan)
* bind-utils (dig)

Role Variables
--------------

These are the variables that can be passed to the role:

    inventory_known_hosts: "[ 'host1', 'host2']"

Defaults to all hosts in inventory

Dependencies
------------

None.

Example Playbook
----------------

This is a basic example for all hosts in inventory:

    - hosts: localhost
      connection: local
      roles:
         - ansible-role-inventory-known-hosts

You can also use this to check for missing/incorrect ssh keys if you run it in check-mode.

License
-------

GPLv3

Author Information
------------------

[Klaas Demter](https://github.com/Klaas-/)
