Please note that these playbooks are provided without support and are intended to be a guideline. Any issues encountered can be reported via the GitHub issues and will be addressed on a best effort basis. Pull requests are also encouraged.

# Introduction

Ansible provides a simple way to deploy, manage, and configure the Confluent Platform services. This repository provides playbooks and templates to easily spin up a Confluent Platform installation. Specifically this repository:

* Installs Confluent Platform packages
* Starts services using systemd scripts
* Provides configuration options for plaintext, SSL, and SASL_SSL communication amongst the services

The services that can be installed from this repository are:

* ZooKeeper
* Kafka
* Schema Registry
* REST Proxy
* Confluent Control Center
* Kafka Connect (distributed mode)

# Documentation

You can find the documentation for running this playbook at https://docs.confluent.io/current/tutorials/cp-ansible/docs/index.html.

gcloud compute instances create kafka-ansible-1 --image=ubuntu-1804-bionic-v20181029 --boot-disk-size=100GB --private-network-ip=10.60.8.200 --zone=asia-southeast1-a --tags=data,ssh --network=v-network-staging-network --subnet=v-network-data-staging-subnetwork --no-address --image-project=ubuntu-os-cloud

gcloud compute instances create kafka-ansible-2 --image=ubuntu-1804-bionic-v20181029 --boot-disk-size=100GB --private-network-ip=10.60.8.201 --zone=asia-southeast1-a --tags=data,ssh --network=v-network-staging-network --subnet=v-network-data-staging-subnetwork --no-address --image-project=ubuntu-os-cloud

gcloud compute instances create kafka-ansible-3 --image=ubuntu-1804-bionic-v20181029 --boot-disk-size=100GB --private-network-ip=10.60.8.202 --zone=asia-southeast1-a --tags=data,ssh --network=v-network-staging-network --subnet=v-network-data-staging-subnetwork --no-address --image-project=ubuntu-os-cloud

gcloud compute instances create kafka-ansible-3 --image=ubuntu-1804-bionic-v20181029 --boot-disk-size=100GB --private-network-ip=10.60.8.202 --zone=asia-southeast1-a --tags=data,ssh --network=v-network-staging-network --subnet=v-network-data-staging-subnetwork --no-address --image-project=ubuntu-os-cloud

gcloud compute instances create schema-registry-ansible --image=ubuntu-1804-bionic-v20181029 --boot-disk-size=10GB --private-network-ip=10.60.8.203 --zone=asia-southeast1-a --tags=data,ssh --network=v-network-staging-network --subnet=v-network-data-staging-subnetwork --image-project=ubuntu-os-cloud

gcloud compute instances create host-control-ansible --image=ubuntu-1804-bionic-v20181029 --boot-disk-size=10GB --private-network-ip=10.60.8.204 --zone=asia-southeast1-a --tags=data,ssh --network=v-network-staging-network --subnet=v-network-data-staging-subnetwork --image-project=ubuntu-os-cloud

gcloud compute instances create connect-ansible --image=ubuntu-1804-bionic-v20181029 --boot-disk-size=10GB --private-network-ip=10.60.8.205 --zone=asia-southeast1-a --tags=data,ssh --network=v-network-staging-network --subnet=v-network-data-staging-subnetwork --image-project=ubuntu-os-cloud

gcloud compute instances create ksql-ansible --image=ubuntu-1804-bionic-v20181029 --boot-disk-size=10GB --private-network-ip=10.60.8.206 --zone=asia-southeast1-a --tags=data,ssh --network=v-network-staging-network --subnet=v-network-data-staging-subnetwork --image-project=ubuntu-os-cloud


deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main

sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367
sudo apt-get update
sudo apt-get install ansible
https://github.com/quyetnguyen0989/cp-ansible.git