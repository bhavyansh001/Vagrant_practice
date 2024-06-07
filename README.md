# Vagrant Practice

This repository contains two branches with different Vagrant configurations to help practice with Vagrant.

## Branches

### Main Branch

This branch contains a single Vagrant VM configuration.

### Multi-VM Branch

This branch contains a multi-VM setup with four defined VMs: `the_website`, `service_A`, `service_B`, and `database`.

## Vagrant Commands

Below are some common Vagrant commands to manage your VMs:

- Initialize a Vagrant environment:
```sh
    vagrant init
```
- Start and provision the Vagrant environment:
```sh
    vagrant up
```
- SSH into the running Vagrant VM:
```sh
    vagrant ssh
```
- Stop the Vagrant VM:
```sh
    vagrant halt
```
- Destroy the Vagrant VM:
```sh
    vagrant destroy
```
- Reload the Vagrant VM (restarts the VM and applies changes to the Vagrantfile):
```sh
    vagrant reload
```
- List the boxes
```sh
    vagrant box list
```
- Check status of VMs
```sh
    vagrant status
```
- Check global status of all VMs
```sh
    vagrant global-status
```
For a multi vm configuration, use the commands mentioned above followed by name of the vm
For example:
```sh
    vagrant up database
```

## Vagrant Plugins

Vagrant plugins extend the functionality of Vagrant. Here are some useful plugins:

- **vagrant-vbguest**: Automatically installs the host's VirtualBox Guest Additions on the guest system.
```sh
    vagrant plugin install vagrant-vbguest
```
- **vagrant-disksize**: Allows you to resize the disk of the VM.
```sh
    vagrant plugin install vagrant-disksize
```
- **vagrant-hostmanager**: Manages the `/etc/hosts` file on guest machines.
```sh
    vagrant plugin install vagrant-hostmanager
```

## Notes

- Ensure you have Vagrant and VirtualBox installed on your system.
- Modify the Vagrantfile configurations as needed to suit your environment and requirements.