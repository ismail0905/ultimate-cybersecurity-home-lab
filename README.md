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

<img src="https://github.com/user-attachments/assets/2ab76769-3ce7-4b9f-93ab-30a1e512c746" width="600"/>

🧠 Skills & Concepts Demonstrated

✅ Installing and configuring a Type 1 hypervisor (Proxmox)
✅ Creating isolated virtual networks with bridge interfaces
✅ Deploying and securing pfSense as a firewall
✅ Simulating threats and attacker behavior using Kali Linux
✅ Hosting services and preparing for SIEM integration via Ubuntu Server
✅ Laying the groundwork for SOC operations, threat detection, and response workflows

💡 What I Learned

How real-world segmentation works and why it’s critical in enterprise security
The pain (and power) of configuring firewall rules with purpose
How to think in terms of attack surfaces and defensive zones
The difference between traditional flat networks vs. segmented lab environments
Building a stable platform I can now use to simulate blue-team and red-team operations


📎 Final Thoughts

This project isn’t just a static lab — it’s a constantly evolving platform. It’s built to support upcoming projects like:
📂 Incident simulation and IR reporting
🛠️ Vulnerability scanning and risk assessments
🤖 Experimenting with AI-powered security automation tools

This home lab reflects my approach to learning: hands-on, technical, and focused on realism. It gives me a safe space to break things, fix them, and refine my understanding of how cybersecurity works in real enterprise environments.
