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
NVM_EXPORT: |
      export NVM_DIR="$HOME/.nvm"
      [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
      [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
NODE_VERSION: 16
DEFAULT_SHELL_PATH: /bin/bash
DEFAULT_SHELL_CONF_FILE: ~/.bashrc
USERS_NVM_NODE:
  - centos
  - root
SCRIPT_LOCAL_PATH: roles/stevenleclerc.ansible_nvm_node_role/files
```

The `SCRIPT_LOCAL_PATH` is the path where the templated file should be deposed. If you test this roles changed it to `./files`.

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
