# Apache CloudStack Installation Steps

## Overview
This document summarizes the practical installation flow used for deploying Apache CloudStack on Ubuntu Server.

The goal was to evaluate a more advanced cloud management platform suitable for deeper infrastructure administration and more complex learning environments.

## Environment
- Ubuntu Server 22.04 LTS
- server-based deployment
- virtualization learning environment
- practical testing setup

## Preparation
Before installing Apache CloudStack, the required packages and dependencies were prepared.

Example:
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y openjdk-11-jdk mariadb-server nfs-kernel-server qemu-system-x86 libvirt-daemon-system libvirt-clients virtinst genisoimage
```

## KVM Preparation
KVM-related modules were loaded to support virtualization.

Example:
```bash
sudo modprobe kvm
sudo modprobe kvm_intel
```

## Hostname and Hosts Configuration
The server hostname and local name resolution were configured before deployment.

Example:
```bash
sudo hostnamectl set-hostname cloudstack.lab.local
sudo nano /etc/hosts
```

## Repository Configuration
The Apache CloudStack package repository was added to the system.

Example:
```bash
echo "deb http://download.cloudstack.org/ubuntu jammy 4.17" | sudo tee /etc/apt/sources.list.d/cloudstack.list
sudo wget -O /etc/apt/trusted.gpg.d/cloudstack.asc http://download.cloudstack.org/release.asc
sudo apt update
```

## CloudStack Installation
CloudStack management packages were installed after the repository was added.

Example:
```bash
sudo apt install -y cloudstack-management cloudstack-usage
```

## Database Configuration
MariaDB was configured to support CloudStack.

Example configuration steps included:
```bash
sudo nano /etc/mysql/mariadb.conf.d/50-server.cnf
sudo systemctl restart mysql
sudo mysql_secure_installation
```

## Database Initialization
A CloudStack database and user were created, and the database setup process was started.

Example:
```bash
sudo cloudstack-setup-databases cloud:cloud@localhost --deploy-as=root
```

## Management Server Setup
The CloudStack management server was initialized.

Example:
```bash
sudo cloudstack-setup-management
```

## NFS Storage Preparation
Primary and secondary storage directories were created and prepared for use.

Example:
```bash
sudo mkdir -p /export/primary
sudo mkdir -p /export/secondary
sudo chown -R nobody:nogroup /export/primary /export/secondary
```

## NFS Export Configuration
The NFS export configuration was adjusted to make storage available for the platform.

Example:
```bash
sudo nano /etc/exports
sudo exportfs -a
sudo systemctl restart nfs-kernel-server
```

## Validation
After installation, the platform was validated by opening the CloudStack management interface and continuing infrastructure setup through the web UI.

Validation included:
- confirming the management service was available
- accessing the web interface
- preparing zones, pods, clusters, and storage
- validating that virtual machine deployment was possible

## Practical Notes
Key observations from the installation process:
- setup required more components than MicroStack
- deployment was more complex and required careful preparation
- storage, database, and networking played a major role
- the platform provided broader management capability after setup

## Summary
Apache CloudStack provided a more advanced and feature-rich platform for building and evaluating a virtualized learning environment on Ubuntu Server.
