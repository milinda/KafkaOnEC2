# Kafka on EC2 (WIP)

Ansible scripts for deploying Kafka (v0.9.1 with Zookeeper 3.4.6) on EC2.

# How To Run

## Prerequisites

* **Ansible**
* **boto** - required for Ansible EC2 module
* Setup boto configuration based on [http://boto.readthedocs.org/en/latest/boto_config_tut.html](http://boto.readthedocs.org/en/latest/boto_config_tut.html)
* Access to EC2 Key Pair

## Steps

1. Edit configuration file ```group_vars/all``` based on your reqiurements and environment.
2. Execute ```ansible-playbook --private-key=<AWS_key_file> kafka.yml```