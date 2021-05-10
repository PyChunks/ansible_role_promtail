Role Name
=========

Installs and configures Promtail

Requirements
------------

Git is the only requirement since we install promtail directly from the official repository.

Role Variables
--------------
Variables with a default value:

```jinja2
promtail_version: latest

promtail_binary_path: /usr/bin

promtail_binary_name: promtail

promtail_config_path: /etc/promtail

promtail_config_name: config.yml

client_ip_or_domain: 127.0.0.1

client_port: 3100
```

You will want to change `client_ip_or_domain` if your receiving server is remote.

Otherwise the default values shouldn't be changed unless you need a very specific behaviour.

Dependencies
------------
None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      vars: 
        client_ip_or_domain: loki_domain_here
      roles:
         - ansible_role_promtail 

License
-------

BSD

Author Information
------------------
Created by Vincent D-Gauthier
