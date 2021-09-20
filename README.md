Role Name
=========

Disable cloud-init service in Ubuntu.

Requirements
------------

Tested in Ubuntu 20.04

Role Variables
--------------

No vars are needed.

Dependencies
------------

No dependencies

Example
----------------

In your `main.yml`:

    - hosts: servers
      roles:
         - disable-cloud-init

Define target hosts in your inventory file `hosts`:

    [servers]
    192.168.99.11
    192.168.99.12
    192.168.99.13

Call the playbook:

    ansible-playbook -i hosts main.yml

License
-------

MIT

Author
------------------

https://github.com/lucaslehnen

Sources
-------

- https://cloudinit.readthedocs.io/en/latest/topics/boot.html#generator
- https://www.blackmoreops.com/2019/04/19/remove-cloud-init-from-ubuntu/