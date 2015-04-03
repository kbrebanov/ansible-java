java
====

Installs Java

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name                           | Default | Description                                           |
|--------------------------------|---------|-------------------------------------------------------|
| java_oracle_version            | 8       | Version of Oracle Java to install                     |
| java_oracle_install_jce_policy | false   | Enable/Disable installation of Oracle Java JCE policy |

Dependencies
------------

None

Example Playbook
----------------

Install Oracle Java 8
```
- hosts: all
  roles:
    - { role: kbrebanov.java }
```

Install Oracle Java 8 and JCE policy
```
- hosts: all
  roles:
    - { role: kbrebanov.java, java_oracle_install_jce_policy: true }
```

Install Oracle Java 7
```
- hosts: all
  roles:
    - { role: kbrebanov.java, java_oracle_version: 7 }
```

Install Oracle Java 7 and JCE policy
```
- hosts: all
  roles:
    - { role: kbrebanov.java, java_oracle_version: 7, java_oracle_install_jce_policy: true }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
