Deploy Stack
============

A role to deploy a Stack on a Docker Swarm cluster. To update the Stack, the stack is destroyed and recreated with the new structrure.
It uses a file wrote on the target machine to manage if the stack is to deploy/update.

Requirements
------------

It requires a complete setup of a Docker Swarm cluster.

Role Variables
--------------

Stack file (classic file) or Stack hash (the file can be converted in an hash?).
A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: deploy-stack, deploy_stack_stack_file: docker-compose.yml }

    - hosts: servers
      roles:
         - { role: deploy-stack, deploy_stack_stack_hash: "'version': '3.2', 'services': [ { 'http': { 'image': 'fabrizio2210/rpi-busybox-httpd:latest' } } ]" }
License
-------

BSD

Author Information
------------------

Fabrizio2210
