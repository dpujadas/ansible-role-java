java
====

This role installs and configures Java using openjdk or [WebUpd8 Installer](https://launchpad.net/~webupd8team/+archive/ubuntu/java).

Role Variables
--------------

- `java_version`: Which version to install, currently only 7 / 8 are supported (default: '7').
- `java_use_oracle`: Use Oracle Java if True, openjdk otherwise (default: False)
- `java_openjdk_packages`: List of openjdk packages to install (default: ['jre-headless'])
- `java_oracle_set_as_default`: Set this Java as system default (default: True)

Example Playbook
----------------

    - hosts: servers
      roles:
        - { 
          role: 'java',
          java_version: '8',
          java_use_oracle: True
        }

License
-------

MIT

[![Build Status](https://travis-ci.org/dpujadas/ansible-role-java.svg?branch=master)](https://travis-ci.org/dpujadas/ansible-role-java)
