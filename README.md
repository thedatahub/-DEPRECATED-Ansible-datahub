# Ansible provisioning for the Datahub

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)

## Ansible provisioning for the Datahub

This project provides [Ansible](http://www.ansible.com) playbook for easy/quick
installation and configuration of a Datahub instance.

Use this playbook to either setup a Datahub instance on a remote host, or on
your local machine for development purposes.

### Requirements

You will need a working installation of [Vagrant](https://www.vagrantup.com/)
and [Ansible](http://www.ansible.com) on your host machine.

### What is in the box?

Provisioning will result in a box with a complete stack of dependencies needed
to run a Datahub instance. This includes:

- Ubuntu/trusty64
- MongoDB
- Catmandu / Librecat
- NGinX
- PHP 5.6 with php5-cli, php5-intl, php5-mcrypt and the mongo extensions.
- Composer

## Install

Clone this repository to your local machine (we assume you have a dedicated
workspace folder at `~/Workspace` refer to `Vagrantfile` to change this to a
destination of your choice.)

Clone the [Datahub](https://github.com/thedatahub/datahu) repository to
your Workspace folder.

Execute `vagrant up` in the ansible-datahub folder.

```bash
cd ~/Workspace
git clone https://github.com/thedatahub/ansible-datahub
git clone https://github.com/thedatahub/datahub ~/Workspace/datahub
cd ~/Workspace/ansible-datahub
vagrant up
```

## Usage

Out of the box, NGinX listens on IP address `192.168.2.151`. Alternatively, you
could create an entry in your `/etc/hosts` file that points to `datahub.local`.

Open up your browser and navigate to either the IP address or the local domain.

## Author

* Matthias Vandermaesen <matthias.vandermaesen@vlaamsekunstcollectie.be>

## License

This package is free software; you can redistribute it and/or modify it under
the terms of the GPLv3.

Please see [License File](LICENSE) for more information.
