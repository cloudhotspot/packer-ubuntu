# Packer Build For Ubuntu

This repository includes a Packer build script for creating Ubuntu boxes for Vagrant.

## Supported Providers

- Virtualbox
- VMWare Desktop/Workstation/Fusion

## Quick Start

```bash
$ packer build ubuntu1404.json
...
...
==> Builds finished. The artifacts of successful builds are:
--> virtualbox-iso: 'virtualbox' provider box: packer_virtualbox-iso_virtualbox.box
--> vmware-iso: 'vmware' provider box: packer_vmware-iso_vmware.box 
```