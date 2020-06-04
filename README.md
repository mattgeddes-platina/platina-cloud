# Ansible Collection - mattgeddes_platina.platina_cloud

## Overview

This is an Ansible Galaxy collection that allows you to use Platina Command
Center for inventory.

This in turn makes it possible to take any Ansible role(s) and apply them to
any group of nodes within your PCC infrastructure.

## Configuring The Inventory

To configure the PCC inventory, simply add the name/IP of your PCC instance,
along with the username/password for a user account with the ability to query
the PCC nodes list, to the inventory.json file provided.

## Executing The Playbook

A skeleton playbook has been added. Roles may be assigned to hosts/groups of
hosts from there. To execute the playbook, a sample wrapper script has been
provided.
