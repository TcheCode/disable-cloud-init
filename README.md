Disable cloud-init
=========

Disable cloud-init service in Ubuntu.

Example
----------------

In your `main.yml`:

    - hosts: servers
      roles:
         - disable-cloud-init

In your `requirements.yml`:

    - name: disable-cloud-init
      src: https://github.com/TcheCode/disable-cloud-init
      version: 1.0.0

Define target hosts in your inventory file `hosts`:

    [servers]
    192.168.99.11
    192.168.99.12
    192.168.99.13

Install requirements:

```
ansible-galaxy install -r requirements.yml
```

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