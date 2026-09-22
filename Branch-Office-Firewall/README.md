# Branch Office Firewall with Cisco ASA

## 📌 Project Overview

This project implements a secure branch office network using **Cisco Packet Tracer** and a **Cisco ASA 5506-X firewall**.

The network is divided into three security zones:

- **Inside Network** – Internal users and office computers
- **Outside Network** – External/Internet network
- **DMZ (Demilitarized Zone)** – Publicly accessible servers

The Cisco ASA firewall is placed between these networks to control and secure communication using firewall rules, access control, and network address translation.

## 🎯 Objectives

- Design a secure branch office network topology.
- Configure a Cisco ASA 5506-X firewall.
- Separate the network into Inside, Outside, and DMZ zones.
- Control traffic between different security zones.
- Protect the internal network from unauthorized external access.
- Provide controlled access to servers in the DMZ.
- Configure and test network connectivity using Cisco Packet Tracer.

## 🏗️ Network Architecture

The network consists of three major zones:

### 1. Inside Network

**Network:** `10.0.0.0/24`

The Inside network contains the internal office users and computers.

Components:
- Internal Router
- Switch
- PC0
- PC1
- PC2
- PC3
- PC4

### 2. Outside Network

**Network:** `192.168.1.0/24`

The Outside network represents the external/Internet side of the organization.

Components:
- Outside Router
- Switch
- External PCs
- Google/Internet simulation server

### 3. DMZ Network

**Network:** `172.16.0.0/24`

The DMZ contains servers that need to provide services to users while remaining separated from the internal network.

Servers include:

- Web Server – `172.16.0.10`
- DNS Server – `172.16.0.11`
- DHCP Server – `172.16.0.12`
- Email Server – `172.16.0.13`

## 🔥 Firewall

The central security device is a **Cisco ASA 5506-X**.

The ASA connects:

```text
                 OUTSIDE
             192.168.1.0/24
                    |
                    |
             Cisco ASA 5506-X
              /             \
             /               \
        INSIDE              DMZ
    10.0.0.0/24         172.16.0.0/24
        |                    |
     PCs/Users            Servers