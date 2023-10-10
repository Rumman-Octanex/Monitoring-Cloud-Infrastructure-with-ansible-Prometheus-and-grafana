# Monitoring-aws-cloud-Infrastructure-with-ansible-Prometheus-and-grafana
This project demonstrates how to set up a comprehensive infrastructure monitoring system on Amazon Web Services (AWS) using Ansible for orchestration, Prometheus for metrics collection, and Grafana for data visualization. By following this guide, you can monitor the performance and health of your AWS instances in real-time.
<<<<<<< HEAD

![monitoring aws cloud infrastructure with ansible prometheus and grafana](Images/Cloud%20Infa%20Monitoring%20.gif)

## Table of Contents

- [Installation and Setup](#installation-and-setup)
  - [Create EC2 Instance and Install Ansible](#create-ec2-instance-and-install-ansible)
  - [Install Prometheus and Grafana](#install-prometheus-and-grafana)
  - [Install and Configure Node Exporter](#install-and-configure-node-exporter)
  - [Create Grafana Dashboard](#create-grafana-dashboard)
- [Support](#support)

## Installation and Setup

### Create EC2 Instance and Install Ansible

#### Security Groups

**Master Node Security Group:**
- Open ports for SSH (22), Prometheus (9090), and Grafana (3000).

**Worker Node Security Group:**
- Open port for SSH (22) and Node Exporter (9100).

#### Creating Instances

Create a total of 3 instances (you can add more if needed):
- 1 Master/Controller Node (OS: Ubuntu)
- 2 Worker Nodes (OS: Ubuntu)

For the instance types:
- Use `t2.medium` for the Master/Controller Node.
- Use `t2.small` for the Worker Nodes.

#### Master Node User Data

When creating the Master/Controller Node, pass the following user data script. It will automatically install Ansible and create an Ansible playbook directory.
```bash
#!/bin/bash
sudo apt update -y
sudo apt install ansible -y
sudo mkdir -p /home/ubuntu/ansible-playbook
sudo reboot

![bash script](images/1.User%20Data.png)


=======
>>>>>>> 57487c78c8c1d9cdb60479e8efb32b15ce322ca6
