# MicroStack Installation Steps

## Overview
This document summarizes the practical installation flow used for deploying MicroStack on Ubuntu Server.

The goal was to create a lightweight cloud platform suitable for learning, testing, and comparing virtualization environments.

## Environment
- Ubuntu Server 22.04 LTS
- server-based deployment
- virtualization learning environment
- practical testing setup

## Preparation
Before the installation, the system was updated to make sure packages and dependencies were current.

Example:
```bash
sudo apt update && sudo apt upgrade -y
sudo reboot
```

## MicroStack Installation
MicroStack was installed using Snap.

Example:
```bash
sudo snap install openstack --channel 2024.1/beta
```

## Node Preparation
The server node was prepared for MicroStack deployment.

Example:
```bash
sunbeam prepare-node-script | bash -x && newgrp snap_daemon
```

## Cluster Bootstrap
After node preparation, the cluster bootstrap process was started.

Example:
```bash
sunbeam cluster bootstrap
```

During this stage, networking-related values were configured interactively.

## OpenStack Configuration
The platform configuration was continued with the OpenStack setup process.

Example:
```bash
sunbeam configure --openrc demo-openrc
```

This step included network-related and environment-related choices.

## Validation
After deployment, the environment was validated by checking platform state and launching a test virtual machine.

Examples:
```bash
juju status -m openstack
sunbeam launch ubuntu --name demo
```

## Related Documentation
- [Installation Steps](installation-steps.md)

## Practical Notes
Key observations from the installation process:
- deployment was relatively fast
- setup was simpler than heavier cloud platforms
- networking choices were important
- validation after installation was necessary

## Summary
MicroStack provided a practical and accessible way to deploy an OpenStack-based learning environment on Ubuntu Server.
