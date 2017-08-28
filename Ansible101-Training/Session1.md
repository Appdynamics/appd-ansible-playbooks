## Introduction

- Configuration Management tool, server deployment and ad-hoc bash task execution rolled-in-to-one
- Ansible needs to be installed only on the master (laptop). No agents/daemons on target servers
- Sample ad-hoc command: $ ansible example -a "free -m" -u [username]
- Ansible, Vagrant and Virtualbox combination can be used to build complex infrastructure environments on laptop

## Running Ad-Hoc commands

- Inventory file
- Install 'ntp' service on all Redhat hosts: ansible multi -s -m yum -a "name = ntp state = present"
- Install 'git' on any linux variant: ansible app -s -m package -a "name = git state = present"

## Playbooks and Roles

## Playbooks - Beyond the Basics
