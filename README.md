# AWS Remote Server Setup Guide

This project provides a comprehensive guide to establish and manage a secure remote server on **AWS EC2**. It covers the essentials from instance creation to secure remote access using SSH.

---

## 🌟 Features
- **Create and configure an AWS EC2 instance** for remote access.
- **Secure server setup** with SSH key-based authentication.
- **Firewall rules** to allow SSH traffic and restrict unwanted access.
- **Best practices** for remote server management.

---

## 🛠 Prerequisites
Before you begin, ensure you have the following:
- An **AWS account**.
- Installed CLI tools:  
  - [AWS CLI](https://aws.amazon.com/cli/)  
  - [OpenSSH](https://www.openssh.com/)
- Basic knowledge of Linux commands.

---

## 📖 Setup Guide

### 1. **Launch an EC2 Instance**
1. Log in to the [AWS Management Console](https://aws.amazon.com/console/).
2. Navigate to **EC2 Dashboard** > **Instances** > **Launch Instance**.
3. Choose an Amazon Machine Image (AMI), such as **Ubuntu 22.04 LTS**.
4. Select an instance type (e.g., `t2.micro` for free-tier).
5. Configure security groups:
   - Allow **SSH (port 22)** from your IP address only.
6. Download the private key (`.pem` file) when prompted.

---

### 2. **Connect to the EC2 Instance**
1. Open a terminal and navigate to the directory containing your `.pem` file.
2. Change the permissions of the private key file:
   ```bash
   chmod 400 your-key.pem
