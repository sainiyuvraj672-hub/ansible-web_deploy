# 🚀 Ansible Website Deployment Automation

This project showcases a **production-ready Ansible automation workflow** for deploying and managing a static website across **multiple Linux servers**. It supports both **RedHat-based** and **Debian-based** systems and evolves from a basic playbook into a **clean, scalable, role-based architecture**.

---

## 📌 Project Overview

The primary goal of this project is to **automate web server configuration and website deployment** using Ansible.  
It demonstrates real-world DevOps practices such as:

- OS-aware automation
- Security configuration
- Modular Ansible roles
- Post-deployment validation

The project started as a single monolithic playbook and was later refactored into a **role-driven, maintainable setup** suitable for production environments.

---

## ✨ Key Features

- **Multi-OS Support**  
  - RHEL / CentOS (`yum`, `httpd`)
  - Debian / Ubuntu (`apt`, `apache2`)

- **Security Automation**  
  - Firewalld rule management
  - SELinux policy configuration

- **Scalable Architecture**  
  - Refactored into reusable Ansible roles

- **Reliability Checks**  
  - Uses the `uri` module to verify `HTTP 200 OK` after deployment

---

## 🛠️ Tech Stack

- **Automation:** Ansible  
- **Web Server:** Apache (`httpd` / `apache2`)  
- **Operating Systems:**  
  - RedHat / CentOS  
  - Debian / Ubuntu  
- **Infrastructure:** Multi-node Linux lab environment  

---

## 📁 Project Structure

```plaintext
.
├── ansible.cfg            # Ansible configuration settings
├── inventory.ini          # Managed hosts and groups
├── site.yml               # Main deployment playbook
├── index.html             # Website homepage
├── sample_status.html     # Secondary status page
├── roles/                 # Modular Ansible roles
│   ├── webserver/         # Apache installation & configuration
│   ├── firewall/          # Firewall and port management
│   └── selinux/           # SELinux policy handling
└── nagios.yml             # Monitoring integration playbook
