# Ansible Collection - mattgeddes_platina.platina_cloud

## Overview

This is an Ansible Galaxy collection that allows you to use Platina Command
Center for inventory.

This in turn makes it possible to take any Ansible role(s) and apply them to
any group of nodes within your PCC infrastructure.

## Installing this Collection

To install this collection in the current directory, use the command:

```
ansible-galaxy collection install -p . mattgeddes_platina.platina_cloud
```

This may be done as any user.

## Configuring The Inventory

To configure the PCC inventory, simply add the name/IP of your PCC instance,
along with the username/password for a user account with the ability to query
the PCC nodes list, to the inventory.json file provided.

It is recommended that the username/password created be an unprivileged user.
This PCC user should be assigned a role that has read-only access to
Infrastructure and no access to anything else.

## Testing/Viewing The Inventory

To validate that the inventory is being generated correctly, you can execute
the following command from the collection directory:

```
ansible-inventory -i plugins/inventory --list
```

You should be presented with a JSON representation of the Ansible inventory.

## Executing The Playbook

A skeleton playbook has been added. Roles may be assigned to hosts/groups of
hosts from there. To execute the playbook, a sample wrapper script has been
provided. Add any roles or tasks necessary, execute it with ansible-playbook
and tell it to use the Ansible inventory plugin. For example:

```
ansible-playbook -i plugins/inventory ./playbook.yml
```

