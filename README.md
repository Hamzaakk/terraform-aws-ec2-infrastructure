# Terraform AWS EC2 Infrastructure
- **this repo for aws ec2 instance for Devops Redit-clone project**

This project provisions an AWS EC2 instance with a specified configuration using Terraform. The EC2 instance is preconfigured to set up Jenkins and SonarQube using a user-provided installation script.

---

## Features

- **AWS EC2 Instance:**
  - Instance Type: `t2.large`
  - Preconfigured for Jenkins and SonarQube using the `install.sh` script.
  - Root volume size: 40GB.

- **AWS Security Group:**
  - Allows inbound traffic on the following ports:
    - SSH (22)
    - HTTP (80)
    - HTTPS (443)
    - Jenkins (8080)
    - SonarQube (9000)
    - Custom (3000)
  - All outbound traffic is allowed.

- **Provider Configuration:**
  - Supports configuration of AWS access and secret keys.
  - Customizable AWS region.

---

## Prerequisites

1. **Terraform Installed:** Ensure Terraform is installed on your system. [Download Terraform](https://www.terraform.io/downloads).
2. **AWS Account:** An active AWS account with the necessary permissions to create resources (EC2, Security Groups, etc.).
3. **Key Pair:** Create an EC2 key pair in your AWS account and update the `key_name` in the configuration.
4. **Installation Script:** Ensure `install.sh` exists in the project directory with the desired configuration.

---

## Usage

### 1. Clone the Repository
```bash
git clone https://github.com/Hamzaakk/terraform-aws-ec2-infrastructure.git
cd terraform-aws-ec2-infrastructure
