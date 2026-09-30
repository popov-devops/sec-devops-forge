# sec-devops-forge

Infrastructure as Code and DevSecOps laboratory built on a Proxmox cluster.

## Goals

- Infrastructure provisioning with Terraform
- Configuration management with Ansible
- CI/CD with GitLab and GitLab Runner
- Network and infrastructure inventory with NetBox
- Security monitoring with Suricata, Wazuh and OpenSearch
- Isolated offensive-security lab
- Reproducible infrastructure and configuration
- Production-like operational practices

## Architecture

```text
Git
 │
 ├── GitHub
 │
 └── GitLab
      │
      └── GitLab Runner
           │
           ├── Terraform
           │    └── Proxmox
           │         └── VMs
           │
           └── Ansible
                └── VM configuration

Repository structure:
terraform/   Infrastructure provisioning
ansible/     Guest configuration
docs/        Architecture and operational documentation
scripts/     Helper and validation scripts
