Role Name
=========

Install and configure NTP client (chrony)

Requirements
------------

* ansible-playbook [core 2.15.13]

Role Variables
--------------

* ntp_server_pools ~ Array of Time Server list

Dependencies
------------

* NA

Example Playbook
----------------


* playbook.yaml 

```
---
- name: Install chrony on all supported systems
  hosts: localhost
  become: true
  roles:
    - arunbagul.chrony
  vars:
     ntp_server_pools:
       - name: 0.pool.ntp.org
       - name: 1.pool.ntp.org
       - name: 2.pool.ntp.org
       - name: 3.pool.ntp.org
```

* How to download playbook (Ansible Galaxy)

```

export ANSIBLE_CONFIG=/etc/ansible/ansible.cfg
ansible-galaxy role install  arunbagul.chrony

```

* How to apply playbook

```
ansible-playbook playbook.yaml
```

License
-------

* All Rights Reserved


Author Information
------------------
* Arun Bagul
