---
title: "Energy & Resilience Analysis of 5G Cloud-Native Service Meshes"
date: 2025-10-27
summary: "Assessing trade-offs of Service Mesh integration and DDoS mitigation in a cloud-native 5G Open5GS core."
tags:
  - Research
  - Infrastructure
tech_stack:
  - Open5GS
  - Kubernetes
  - Docker
  - Istio
  - Prometheus
  - Python
featured: true
status: "Completed"
role: "Lead Researcher"
duration: "2023 - 2025"
team_size: 1
highlights:
  - "Evaluated energy overhead and throughput impact during DDoS attacks"
  - "Benchmarked containerized 5G Core Network Functions (NFs)"
  - "Published in National & Kapodistrian University of Athens Digital Library"
---

Master’s thesis research investigating the performance overhead, energy consumption, and mitigation mechanics of Service Meshes deployed over a cloud-native 5G core network.

## Research Context

Modern 5G deployments rely heavily on Service-Based Architectures (SBA) running over Kubernetes. While deploying a Service Mesh (like Istio or Linkerd) provides crucial zero-trust security and observability, it injects proxy sidecars into every pod, resulting in compute and energy overhead.

This study specifically evaluates how these sidecars affect CPU utilization, power metrics, and network latency when mitigating active Distributed Denial-of-Service (DDoS) vectors across Service-Based Interfaces (SBI).

## Technical Implementation

### Environment Setup

- **5G Core:** Containerized deployment utilizing Open5GS running over a localized Kubernetes cluster.
- **Service Mesh:** Implementation of Istio to manage traffic shaping, mTLS, and network policies between Network Functions (NFs).

### Telemetry & Benchmarking

- **Data Collection:** Automated metric collection scripts written in Python, interfacing directly with Prometheus.
- **Stress Testing:** Simulated traffic stress and active DDoS vectors to capture power and throughput profiles under adverse network conditions.

## Key Findings

The research successfully mapped the specific trade-offs between zero-trust security enforcement and server power consumption, providing actionable data for telecom operators balancing security with OPEX.

- **Thesis Document:** [Pergamos Library Repository](https://pergamos.lib.uoa.gr/item/uoadl:5311065)
- **Code Repository:** [GitHub - Thesis Open5GS Work](https://github.com/katerinagiann/Thesis_Open5GS)

```

```
