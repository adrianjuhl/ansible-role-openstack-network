Ansible role: openstack-network
=========

This role provides the ability to configure (create or delete) a network in OpenStack, consisting of a network, subnet and router network components.

See Role Variables for the types of networks and their components that can be provisioned.

Requirements
------------

None.

Role Variables
--------------

None.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: adrianjuhl.openstack-network }

License
-------

MIT

Author Information
------------------

[Adrian Juhl](http://github.com/adrianjuhl)
