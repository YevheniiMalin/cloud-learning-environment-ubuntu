# Cloud Learning Environment using Ubuntu

![Platform](https://img.shields.io/badge/platform-Ubuntu%20Server-E95420)
![Virtualization](https://img.shields.io/badge/virtualization-MicroStack%20%7C%20CloudStack-blue)
![Focus](https://img.shields.io/badge/focus-Infrastructure%20%26%20User%20Isolation-green)
![Status](https://img.shields.io/badge/status-Portfolio%20Project-black)

## Overview
This project demonstrates the implementation of a cloud-based ICT learning environment using Ubuntu Server. The focus is on deploying and evaluating two virtualization platforms:

- MicroStack
- Apache CloudStack

The project is based on my bachelor’s thesis and presents a practical comparison of both platforms from the perspective of learning environments, infrastructure management, usability, and user isolation.

## Repository Contents
- [Architecture](architecture/README.md)
- [MicroStack](microstack/README.md)
- [Apache CloudStack](cloudstack/README.md)
- [Security and User Isolation](security/README.md)
- [Platform Comparison](comparison/README.md)
- [Thesis Background](docs/thesis-background.md)
- [Future Improvements](docs/future-improvements.md)
- [Finnish Version](README_FI.md)

## Goals
- Deploy cloud platforms on Ubuntu Server
- Evaluate virtualization platforms for educational use
- Test user isolation and role separation
- Compare MicroStack and Apache CloudStack
- Document installation, configuration, and testing process

## Technologies
- Ubuntu Server 22.04 LTS
- MicroStack
- Apache CloudStack
- KVM
- MariaDB
- NFS
- Linux system administration
- Virtualization and networking

## Key Focus Areas
- Virtualization as an ICT learning environment
- User isolation in shared infrastructure
- Platform usability and manageability
- Network setup and administration
- Documentation and repeatability

## Results
The project showed that both MicroStack and Apache CloudStack can be used in an ICT learning environment, but they serve slightly different purposes.

- MicroStack is lightweight and easier to deploy
- Apache CloudStack provides broader management capabilities
- Both platforms support user isolation and virtual machine management
- CloudStack is more suitable for advanced and larger environments
- MicroStack is well suited for learning and introductory use

## Background
This repository is based on my bachelor’s thesis:  
**“Virtualization Technology as an ICT Learning Environment”**

The purpose of this repository is to turn the thesis work into a more technical and practical portfolio project.

## Future Direction
This project can be extended with:
- architecture diagrams
- sanitized configuration examples
- automation scripts
- security hardening notes
- cloud governance and IAM-oriented extensions

## Author
**Yevhenii Malin**  
Bachelor of Engineering (ICT)
