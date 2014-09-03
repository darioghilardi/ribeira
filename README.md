# Ribeira - Ansible script for Ruby development

An Ansible script that provides a Ruby development environment.

## How to

Change ip address of the machine to static.
Then use the following commands on the machine to refresh the network configuration.

```
ifdown eth1
ifup eth1
```

Add the static ip in your hosts file with a comfortable alias.

Add a zsh alias to connect quickly.

Rename `playbook.yml.example` to `playbook.yml` and change the user home folder of your machine.

Remove the roles you don't want to install from the `playbook.yml`.

Rename `hosts.example` to `hosts` and add the correct values.

Launch the provisioning with `ansible-playbook -i hosts playbook.yml`.
