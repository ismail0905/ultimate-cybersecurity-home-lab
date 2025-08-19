# ultimate-cybersecurity-home-lab
A hands-on cybersecurity lab built from scratch to simulate real-world enterprise environments.

🧠 Ultimate Cybersecurity Home Lab

 By Ismail Odawa

 📌 Overview

This project is a fully virtualized, self-hosted cybersecurity home lab built from scratch to simulate a real-world enterprise network. The goal was to establish a robust environment to develop and demonstrate skills in SOC operations, network segmentation, system isolation, vulnerability management, firewall administration, and SIEM prep work — all critical areas in the cybersecurity space.
It’s designed to be modular and expandable, forming the foundation for follow-up projects including full-scale incident response, vulnerability scanning pipelines, and even AI-driven security automation.

🧰 Lab Environment Setup
The lab was built on a dedicated machine:
🖥️ Hardware: HP Elite desktop, 32GB RAM, 1TB SSD
🧩 Hypervisor: Proxmox VE (bare-metal install)

👇 Core virtual machines:
VM	Purpose
pfSense	Firewall + router managing VLAN-style segmentation
Kali Linux	Attacker/red-team VM used to simulate threats
Ubuntu Server	Docker host, logging environment, future SIEM target

🌐 Network Architecture & Design
Key Concepts Implemented:
VLAN-style isolation using Proxmox virtual bridges (vmbr0, vmbr1, etc.)
pfSense routes traffic and enforces firewall rules between segments
Each VM sits on its own “zone” to reflect LAN, DMZ, and external attack surfaces
Network segmentation allows for realistic monitoring, logging, and threat emulation

## 🧱 Architecture Diagram

![Architecture Diagram](https://github.com/user-attachments/assets/2ab76769-3ce7-4b9f-93ab-30a1e512c746)



