# Packer Build For Ubuntu

This repository includes a Packer build script for creating Ubuntu boxes for Vagrant.

Boxes built with this build script are published at <a href="https://atlas.hashicorp.com/cloudhotspot/boxes/ubuntu" target="_blank">atlas.hashicorp.com</a>. 

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

Build a single provider:

```bash
$ packer build --only=virtualbox-iso ubuntu1404.json
...
...
==> Builds finished. The artifacts of successful builds are:
--> virtualbox-iso: 'virtualbox' provider box: packer_virtualbox-iso_virtualbox.box
```

```bash
$ packer build --only=vmware-iso ubuntu1404.json
...
...
==> Builds finished. The artifacts of successful builds are:
--> vmware-iso: 'vmware' provider box: packer_vmware-iso_vmware.box 
```

To import a built box into Vagrant:

`$ vagrant box add --name=cloudhotspot/ubuntu <box-file>`
