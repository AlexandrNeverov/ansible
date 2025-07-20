# 🐳 Ansible-Docker-Swarm kit

![Admin Terraform Bootstrap EC2 Demo](https://raw.githubusercontent.com/AlexandrNeverov/ansible_docker_setup/main/image.png)

[![Ansible](https://img.shields.io/badge/Ansible-Docker--Swarm--Provisioning-EE0000?style=for-the-badge&logo=ansible&logoColor=white)](https://github.com/AlexandrNeverov/ansible_docker_setup)
[![Docker](https://img.shields.io/badge/Docker-Container--Platform-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-Tested--on--Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)](https://ubuntu.com/)
[![CI Ready](https://img.shields.io/badge/CI--Ready-Automated--Setup-brightgreen?style=for-the-badge)]()

> Provision a fully working Docker Swarm node with Docker Engine, Compose v2, and Portainer — using one Ansible playbook.

---

### ✨ Why This Matters

Installing Docker CE, Compose v2, Swarm mode, and Portainer usually involves a long sequence of shell commands, package installations, and security configurations. Mistakes are easy, automation is tricky, and reusability is low.

**`ansible-docker-swarm-kit`** eliminates this pain by fully automating the process with Ansible:

- 🧩 Installs Docker CE and containerd from Docker’s official APT repo  
- 🧰 Adds Docker Compose v2 as a binary  
- 🌀 Bootstraps Docker Swarm (if not yet active)  
- 🚀 Deploys Portainer CE as a Docker container  
- 🧭 Inventory-based provisioning with SSH private key auth  

This is ideal for:

- 🧪 Testing Docker in clean environments  
- 🛠️ DevOps labs, demos, and bootstrap nodes  
- 💡 Repeatable setup for Swarm-based projects or local learning  
- 🐧 Ubuntu EC2 hosts, Raspberry Pi servers, or any SSH-accessible node

---

### ✅ Features

• 📦 Installs Docker CE, containerd.io, and CLI dependencies
• 🧱 Installs Docker Compose v2 as a standalone binary
• 🔐 Adds GPG key and sets up official Docker APT repo
• 🌀 Auto-initializes Docker Swarm if not active
• 🧰 Creates named Docker volume for Portainer
• 🚀 Launches Portainer CE as a container on port 9000
• 🧩 Inventory-driven structure for reproducible deployment
• 🧭 Role-based modular design with separation of concerns

---

### 📁 Project Structure Overview

| File / Folder          | Purpose                                                        |
|------------------------|----------------------------------------------------------------|
| `playbooks/site.yml`   | Main playbook: Docker + Compose + Swarm + Portainer setup      |
| `roles/docker/`        | Role with tasks for install, verification, volume, container   |
| `inventory/hosts.ini`  | Target host info (IP, user, SSH key path)                      |
| `requirements.yml`     | Ansible Galaxy collections (if needed)                         |
| `ansible.cfg`          | Configures Ansible behavior and paths                          |
| `image.png`            | Optional architecture diagram or screenshot                    |

---

### 🚀 Quick Start

1. ✅ Ensure target node is Ubuntu-based and reachable via SSH  
2. 🔑 Set up your `inventory/hosts.ini` with public IP and SSH key  
3. ▶️ Run the playbook:

```bash
ansible-playbook -i inventory/hosts.ini playbooks/site.yml
```

2. Create Zero-Node (zero_node_aws.sh):
```bash
curl -v https://raw.githubusercontent.com/AlexandrNeverov/zero-node-stack-full/refs/heads/main/boot/create_zero_node_aws.sh | bash - 
```

3. Install DevOps Tool-Kit (setup_zero_node_tools.sh):
```bash
curl -v https://raw.githubusercontent.com/AlexandrNeverov/zero-node-stack-full/refs/heads/main/boot/setup_zero_node_tools.sh | bash - 
```

4. Create HCL Vault (hcl_vault.sh):
```bash
curl -v https://raw.githubusercontent.com/AlexandrNeverov/zero-node-stack-full/refs/heads/main/boot/hcl_vault.sh | bash -
```

4. Create HCL Vault (hcl_vault.sh):
```bash
curl -v https://raw.githubusercontent.com/AlexandrNeverov/zero-node-stack-full/refs/heads/main/boot/hcl_vault.sh | bash -
```

5. Setup Terraform:
```bash
curl -v https://raw.githubusercontent.com/AlexandrNeverov/zero-node-stack-full/refs/heads/main/boot/setup_zero_terraform.sh | bash -
```

6. Setup Ansible (setup_zero_ansible):
```bash
curl -v https://raw.githubusercontent.com/AlexandrNeverov/zero-node-stack-full/refs/heads/main/boot/setup_zero_ansible.sh | bash -
```

---

## 📄 License

MIT – free to use, modify, share.

---

## 👨‍💻 Author

**Alex Neverov**  
Platform Engineer · DevOps Engineer · Cloud & Infrastructure Automation · Industry PhD

- **GitHub:** [AlexandrNeverov](https://github.com/AlexandrNeverov)  
- **LinkedIn:** [linkedin.com/in/alexneverov](https://www.linkedin.com/in/alexneverov)  
- **Upwork:** [upwork.com/freelancers/~01c616035669bbf379](https://www.upwork.com/freelancers/~01c616035669bbf379)  
- **Website:** [neverov-it.com](https://neverov-it.com) · [neverov-science.com](https://neverov-science.com)  
- **Email:** [alex@neverov-it.com](mailto:alex@neverov-it.com) · [nev.al.vic@gmail.com](mailto:nav.al.vic@.com)
- **Phone:** +1 (754) 236‑5715
