# Shank-VPN
Your Own Custom  free VPN setup
# 🚀 Deploy OpenVPN Access Server on AWS EC2

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?logo=amazon-aws&style=for-the-badge)
![Linux](https://img.shields.io/badge/Linux-Ubuntu-blue?logo=linux&style=for-the-badge)
![SSH](https://img.shields.io/badge/SSH-Terminal-222?logo=gnome-terminal&style=for-the-badge)
![VPN](https://img.shields.io/badge/OpenVPN-Secure-orange?logo=openvpn&style=for-the-badge)

---

## 📌 Project Overview

This project sets up a *secure VPN server on AWS EC2* using *OpenVPN Access Server*. It allows you to connect any device to the cloud and route all traffic through the VPN, enhancing security and enabling region-based browsing.

---

## 🧰 Tech Stack

- ☁ Amazon Web Services (AWS)
- 🐧 Ubuntu EC2 Instance
- 🔐 OpenVPN Access Server
- 📦 SSH for remote access
- 🔒 SSL for secure web admin

---

## 📸 Project Snapshots

### 🟠 Screenshot of the AWS Console homepage displaying general navigation and service options
![AWS Console](1.jpg)

---

### 🔑 AWS Marketplace listing for "OpenVPN Access Server" with detailed product features and licensing info
![SSH Login](2.jpg)

---

### 🛡️ OpenVPN Admin Dashboard
![Admin Panel](assets/admin-login.png)

---

### 📥 VPN Profile Download
![VPN Profile](assets/vpn-profile.png)

---

### ✅ VPN Client Connected
![VPN Connected](assets/vpn-connected.png)


---

## ⚙ Step-by-Step Setup

### 🔸 1. Launch EC2 via AWS Marketplace

1. Search for *OpenVPN Access Server* in AWS Marketplace
2. Click *Continue to Subscribe* and then *Launch through EC2*
3. Choose:
   - Instance type: t2.medium (or t2.micro for test)
   - Key pair: Create or select .pem key
   - Security group: Open ports 22 (SSH), 943, 443

### 🔸 2. Connect to EC2 via SSH

```bash
# Move your downloaded key to a secure location
mv ~/Downloads/openvpn-key.pem ~/.ssh/

# Set correct permissions
chmod 400 ~/.ssh/openvpn-key.pem

# Connect to your EC2 instance
ssh -i ~/.ssh/openvpn-key.pem openvpn@<ec2-public-ip>
