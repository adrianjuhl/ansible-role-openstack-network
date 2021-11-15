Ansible role: openstack-network
=========

This role provides the ability to configure a network in OpenStack, consisting of a network, subnet and router network components.

See Role Variables for the types of networks and their components that can be provisioned.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values:

    adrianjuhl__openstack_network__network_name

The name to use for the network.

    adrianjuhl__openstack_network__subnet_name

The name to use for the subnet.

    adrianjuhl__openstack_network__router_name

The name to use for the router.

    adrianjuhl__openstack_network__nameservers

An array/sequence of each IP address to use as a nameserver. For example: [ 8.8.8.8, 8.8.4.4 ]

    adrianjuhl__openstack_network__auth

A dictionary containing the auth information as needed by the auth plugin strategy of the target OpenStack cloud. For the default password plugin, this would contain such elements as auth_url, username, password, project_name, ldap. The password can be supplied by setting an environment variable named OS_PASSWORD.

    adrianjuhl__openstack_network__router_network

The name of the network for which the router is to be connected.

    adrianjuhl__openstack_network__cidr

The CIDR representation of the subnet that should be assigned to the subnet. For example: 10.0.0.0/24

See [OpenStack subnet module Ansible documentation](https://docs.ansible.com/ansible/2.5/modules/os_subnet_module.html#parameters) for more information.


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
