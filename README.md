Role Name
=========

This role will install nvm then node/npm with the version set from the NODE_VERSION variable

Requirements
------------

You have to use a sudoer user to validate the last part of the script:
- Link binaries to /usr/bin (node and npm)

If you cannot, just add `--skip-tag nvm-node-link-binaries`

Role Variables
--------------
By default:

```
NODE_VERSION: 16
DEFAULT_SHELL_PATH: /bin/bash
DEFAULT_SHELL_CONF_FILE: ~/.bashrc
USERS:
  - centos
  - root
```

Dependencies
------------

None

Example Playbook
----------------



License
-------

BSD

Author Information
------------------

Steven LECLERC
