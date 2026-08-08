---
title: "Declarative Infrastructure & Cloud-Native Homelab"
date: 2026-07-01
summary: "Automated multi-node environment featuring Proxmox VE, Kubernetes, Ansible, Terraform, and Traefik."
tags:
  - Infrastructure
  - Systems
tech_stack:
  - Proxmox VE
  - Docker
  - Ansible
  - Terraform
  - Traefik
  - OPNSense
  - OpenWrt
  - TrueNAS
featured: true
status: "Active"
role: "Infrastructure Engineer"
duration: "Ongoing"
team_size: 1
highlights:
  - "Declarative provisioning via Terraform & Ansible"
  - "Automated reverse proxy & dynamic TLS certs via Traefik"
  - "Hardened edge networking with OPNSense and WireGuard VPN"
---

A complete Infrastructure-as-Code (IaC) repository managing home automation, self-hosted services, and cloud-native testbeds. Built to simulate enterprise-grade, high-availability data center operations on personal hardware.

## Architecture Overview

This project represents a fully declarative on-premise infrastructure pipeline. It automates virtual machine deployment, network routing, container orchestration, and secret management across physical and virtual hosts.

## Core Implementations

### Virtualization & Storage

- **Hypervisor:** Proxmox VE running multiple Linux nodes (Debian/Ubuntu Server).
- **Storage Backbone:** TrueNAS providing NFS/SMB shares with ZFS arrays for data redundancy and rapid backup integration.

### Automation & Configuration Management

- **Terraform:** Utilized for the rapid and reproducible provisioning of Proxmox VMs and LXC containers.
- **Ansible:** Playbooks handle OS hardening, SSH key distribution, and service configuration to eliminate configuration drift.

### Networking & Security

- **Edge Routing:** OPNSense acts as the primary firewall, managing strict ingress/egress rules.
- **Mesh VPN:** Integration of WireGuard and Tailscale for secure, remote administrative access without exposing internal ports.
- **Switch Configuration:** Specific VLAN IDs are routed for isolated management, IoT, and guest networks, while ensuring unused port assignments are strictly left at their default states for security.
- **Reverse Proxy:** Traefik handles all ingress traffic, routing to specific internal services and automatically managing Let's Encrypt TLS certificates.

### Containerization Deep Dive

- **Docker Workloads:** Services are containerized for portability.
- **Security Stance:** Strict adherence to container security, ensuring the Docker socket is explicitly _not_ mapped to containers unless absolutely required, preventing privilege escalation.

## Topology Sketch

```text
┌────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│ OPNSense (Edge)│───▶│ Traefik Ingress  │───▶│ Docker / LXC    │
│ + WireGuard VPN│    │ (TLS Management) │    │ (App Workloads) │
└───────┬────────┘    └──────────────────┘    └─────────────────┘
        │
┌───────▼────────┐                            ┌─────────────────┐
│ Managed Switch │───────────────────────────▶│ TrueNAS Storage │
│ (VLAN Tagging) │                            │ (ZFS / NFS)     │
└────────────────┘                            └─────────────────┘
```
