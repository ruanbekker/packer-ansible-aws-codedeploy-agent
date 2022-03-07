# packer-ansible-aws-codedeploy-agent

CodeDeploy AMI using Packer and Ansible

## Description

Packer builds a AMI with the Ansible provisioner to install the CodeDeploy Agent

## AMI Names

The AMI's will be named with the following tags:

- Name: `packer-codedeploy-agent-2022-03-04`
- BaseAMI: `ubuntu/images/hvm-ssd/ubuntu-focal-20.04-amd64-server-20220302`
- Datestamp: `2022-03-04T18:49:22Z`

## Usage

Verify the installation tasks from the role in:
- `ansible/roles/codedeploy-agent/tasks/ubuntu.yml`

Then package the AMI with packer:

```bash
$ packer build packer.json
```
