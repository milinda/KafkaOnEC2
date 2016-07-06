# Kafka on EC2

Ansible scripts for deploying Kafka (v0.9.1 with Zookeeper 3.4.6) on EC2. These scripts were developed based on various resources from Internet. Below is the main reference:

* [Ansible Playbook - Setup Kafka Cluster](http://whatizee.blogspot.com/2015/05/ansible-playbook-setup-kafka-cluster.html)



# How To Run

## Prerequisites

* **Ansible**
* **boto** - required for Ansible EC2 module
* Setup boto configuration based on [http://boto.readthedocs.org/en/latest/boto_config_tut.html](http://boto.readthedocs.org/en/latest/boto_config_tut.html)
* Access to EC2 Key Pair


## Steps

1. Edit configuration file ```group_vars/all``` based on your reqiurements and environment.
2. Execute ```ansible-playbook --private-key=<AWS_key_file> -u ubuntu kafka.yml```

# Notes

* In one of my Macs I got the error described in [https://github.com/ansible/ansible/issues/5734](https://github.com/ansible/ansible/issues/5734). If you are getting the same error please use the ```inventory``` file provided (```ansible-playbook --private-key=<AWS_key_file> -u ubuntu -i inventory kafka.yml```).
