# docker-swarm-tutorial
Vagrant configuration for 3 Docker nodes - suitable for completing the tutorial at https://docs.docker.com/engine/swarm/swarm-tutorial/

It creates 3 Docker nodes with the latest Docker 1.12 release candidate installed on each using the same hostnames and IP addresses as the tutorial.

# Pre-requisities
Requires [Vagrant](https://www.vagrantup.com/) and [Ansible](https://www.ansible.com/) to be installed on the host machine.

If you are using a Mac then Homebrew is a handy way to install Ansible. See https://valdhaus.co/writings/ansible-mac-osx/

# Usage

Install the Host Manager plugin for Vagrant.

```
./install_vagrant_plugins.sh
```

Create the 3 nodes using Vagrant by running ```vagrant up```.

# Connecting to the Nodes

The Vagrantfile creates 3 nodes:-

| Hostname | IP Address |
| -------- | ---------- |
| manager1 | 192.168.99.100 |
| worker1 | 192.168.99.101 |
| worker2 | 192.168.99.102 |

To connect to the individual nodes, you can use ```vagrant ssh <hostname>```.

For example, ```vagrant ssh manager1```.
