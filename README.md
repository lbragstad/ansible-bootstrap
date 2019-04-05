# ansible-bootstrap

Ansible scripts for setting up development environments.

## Supported Distributions

* Ubuntu 18.04

## Installation

This tool assumes you have [virtualenv](https://virtualenv.pypa.io/en/latest/)
installed locally.

```
$ virtualenv -p /usr/bin/python3 .venv
$ .venv/bin/pip install -r requirements.txt
$ .venv/bin/ansible-galaxy install -r requirements.yml
```

## Installing Docker

Run the following to install docker:

```
$ .venv/bin/ansible-playbook -i "$TARGET_IP," --user ubuntu --become tasks/install_docker.yaml
```

## Installing Go

```
$ .venv/bin/ansible-playbook -i "$TARGET_IP," --user ubuntu --become tasks/install_go.yaml
```
