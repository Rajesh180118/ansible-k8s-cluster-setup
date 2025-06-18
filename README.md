# ansible-k8s-cluster-setup

An automated solution for installing and configuring a Kubernetes cluster using Ansible.

## 📌 Overview

This repository contains Ansible playbooks to set up a Kubernetes cluster using `kubeadm`. It supports multi-node configurations with one or more master and worker nodes. The goal is to simplify the provisioning process, ensure repeatability, and reduce manual intervention during Kubernetes setup.

## 🚀 Features

- Install Docker or container runtime
- Configure sysctl and kernel modules
- Disable swap memory
- Install Kubernetes components (`kubeadm`, `kubelet`, `kubectl`)
- Initialize master node and join worker nodes
- Supports Ubuntu/CentOS-based systems

## 🧰 Prerequisites

- Ansible installed on control machine
- SSH access to all target nodes
- Passwordless sudo access
- Inventory file configured with IP addresses of master and worker nodes

## 📂 Structure
.
├── inventory/
│ └── hosts # Inventory file with node IPs
├── playbooks/
│ ├── setup.yml # Common system setup
├── roles/
│ └── tasks
|      |── main.yml
├── README.md
