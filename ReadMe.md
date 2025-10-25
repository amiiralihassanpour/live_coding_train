# Live Coding — SRE and DevOps Journey

## Goal

The goal of this repository is to learn how to think and act like an SRE (Site Reliability Engineer) and DevOps Engineer through practical, hands-on implementation.  
This repository is based on [AhmadRafiee/RahBia-Live-Coding](https://github.com/AhmadRafiee/RahBia-Live-Coding).

---

## Steps Overview

### 1. Live Coding Introduction

- [x] Explain the live coding video path  
- [x] Project introduction and code review (Voting App)  
- [x] Infrastructure overview (VMware, Debian OS)  
- [x] Automation tool introduction (Ansible)  
- [x] Create the project on GitHub and set up storage for static files on Google Drive  

---

### 2. Linux Setup and Hardening

- [ ] Install a Linux OS (Debian)  
- [ ] Perform disk partitioning and apply required standards  
- [ ] Review the partitioning  
- [ ] Update and install basic required tools  
- [ ] Perform system hardening using the Lynis tool  
- [ ] Use Ansible to:  
  - [ ] Harden Linux servers to achieve a security score above 80  
  - [ ] Install and configure Docker  
  - [ ] Configure iptables  
  - [ ] Configure SSH  
  - [ ] Change passwords  
- [ ] Use Mitogen for Ansible  
- [ ] Create a VM template on VMware and automate VM creation using Ansible  

---

### 3. Service Deployment and Infrastructure Tools

#### Voting App Deployment

- [ ] Deploy the project as a service with a database and cache  
- [ ] Demonstrate the challenges and complexities during deployment  

#### GitLab Setup

- [ ] Set up GitLab on Docker  
- [ ] Create and register a GitLab Runner  
- [ ] Create a GitLab backup script  
- [ ] Move the backup to MinIO  
- [ ] Encrypt the backup file  
- [ ] Create a cron job for GitLab backup  

#### Nexus Setup

- [ ] Set up Nexus on Docker  
- [ ] Change the Nexus default password  
- [ ] Configure anonymous access and Realms  
- [ ] Create users, roles, and assign permissions  
- [ ] Configure repositories and blob stores:  
  - [ ] Docker proxy with Traefik configuration  
  - [ ] Docker blob store and cleanup policy  
  - [ ] Apt blob store and cleanup policy  
  - [ ] Raw blob store and cleanup policy  
  - [ ] PyPI blob store and cleanup policy  

#### Traefik and MinIO Setup

- [ ] Set up Traefik on Docker  
- [ ] Set up MinIO on Docker  
- [ ] Create a bucket  
- [ ] Create a user  
- [ ] Create a policy  
- [ ] Match user with policy  

---

### 4. Automation and CI/CD

- [ ] Write an Ansible playbook to automate all completed tasks  
- [ ] Draw a High-Level Design (HLD) diagram of services built and the journey so far  
- [ ] Review Voting App Dockerfiles, build images, and push them to a registry  
- [ ] Write a Docker Compose file to containerize the Voting App  
- [ ] Add environment variables for configurable project settings  
- [ ] Use Traefik as a reverse proxy for the entire project  
- [ ] Draw an updated HLD diagram  

---

### 5. CI/CD Pipeline and Testing

- [ ] Write CI/CD pipelines for the project with three environments (development, staging, production)  
- [ ] Implement build, test, and deployment stages  
- [ ] Add container scanning using Trivy  
- [ ] Add load test scenarios  
- [ ] Create database backup and move it to object storage  
- [ ] Test database backup and restore  
- [ ] Implement GitLab image cleanup policy  
- [ ] Encrypt and decrypt PostgreSQL backups  
- [ ] Add GitLab components and catalogs  
- [ ] Test GitLab backups  
- [ ] Create multi-project CI/CD pipelines and trigger downstream projects  

---

### 6. Monitoring, Logging, and Tracing

- [ ] Set up Prometheus stack on Docker for monitoring and alerting  
- [ ] Set up ELK stack on Docker for logging  
- [ ] Set up Loki stack on Docker for logging  
- [ ] Set up Tempo stack on Docker for tracing  
- [ ] Review resource usage using monitoring tools  
- [ ] Analyze service logs  
- [ ] Trace service requests  
- [ ] Write Ansible playbooks to automate these tasks  
- [ ] Draw updated HLD diagrams  

---

### 7. Scaling and Clustering

- [ ] Transition project infrastructure to Docker Swarm  
- [ ] Cluster PostgreSQL and Redis without orchestration  
- [ ] Cluster PostgreSQL and Redis on Swarm  
- [ ] Deploy Voting App and monitoring stacks on Swarm  
- [ ] Adjust CI/CD for Swarm deployment  
- [ ] Perform load tests and observe service limits  
- [ ] Evaluate design for Single Point of Failure (SPOF)  

---

### 8. Kubernetes and Ceph Integration

- [ ] Set up Kubernetes cluster using Kubeadm and Kubespray  
- [ ] Install add-ons using Helm, Terraform, Argo CD, and Ansible  
- [ ] Set up Ceph cluster using Cephadm and integrate with Kubernetes  
- [ ] Deploy clustered PostgreSQL and Redis on Kubernetes  
- [ ] Write manifests for the Voting App and deploy it on Kubernetes  
- [ ] Back up Kubernetes resources and etcd  
- [ ] Use GitLab CI/CD and Argo CD for GitOps deployment  
- [ ] Implement auto-scaling and perform load testing  
- [ ] Review SPOF and update clusters without downtime  

---

### 9. Advanced Monitoring and Chaos Engineering

- [ ] Federate monitoring systems  
- [ ] Cluster backend databases for monitoring (Mimir, VictoriaMetrics)  
- [ ] Use VictoriaLogs for logging and compare with Loki  
- [ ] Update and expand Ceph and Kubernetes clusters  
- [ ] Set up chaos engineering tools (LitmusChaos)  
- [ ] Perform end-to-end testing for Kubernetes (Sonobuoy) and Ceph  
- [ ] Use Grafana OnCall for shift management and alerting improvement  
- [ ] Establish monitoring and alerting for backup systems  
- [ ] Draw updated HLD diagrams  

---

### 10. Private Cloud and OpenStack

- [ ] Set up OpenStack to create a private cloud  
- [ ] Create VMs using Terraform and Ansible  
- [ ] Set up a Kubernetes cluster on OpenStack with automation  
- [ ] Deploy all previous components on Kubernetes within the private cloud  
- [ ] Configure monitoring, logging, and tracing for OpenStack  
- [ ] Update OpenStack clusters and simulate incidents  
- [ ] Perform end-to-end testing with the Rally project  
