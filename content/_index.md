---
# Leave the homepage title empty to use the site title
title: ""
summary: ""
date: 2026-08-06
type: landing

sections:
  # Developer Hero - Gradient background with name, role, social, and CTAs
  - block: dev-hero
    id: hero
    content:
      username: me
      greeting: "Hi, I'm"
      show_status: true
      show_scroll_indicator: true
      typewriter:
        enable: true
        prefix: "I build"
        strings:
          - "automated infrastructures"
          - "cloud-native ecosystems"
          - "resilient network architectures"
          - "high-availability environments"
        type_speed: 70
        delete_speed: 40
        pause_time: 2500
      cta_buttons:
        - text: View My Work
          url: "#projects"
          icon: arrow-down
        - text: Get In Touch
          url: "#contact"
          icon: envelope
    design:
      style: centered
      avatar_shape: circle
      animations: true
      background:
        color:
          light: "#fafafa"
          dark: "#0a0a0f"
      spacing:
        padding: ["6rem", "0", "4rem", "0"]

  # Filterable Portfolio - Alpine.js powered project filtering
  - block: portfolio
    id: projects
    content:
      title: "Featured Projects"
      subtitle: "A selection of my work"
      count: 0
      filters:
        folders:
          - projects
      buttons:
        - name: All
          tag: "*"
        - name: Infrastructure as Code
          tag: Infrastructure
        - name: Systems & Development
          tag: Systems
        - name: Research & Telecom
          tag: Research
      default_button_index: 0
    design:
      columns: 3
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  # Visual Tech Stack - Icons organized by category
  - block: tech-stack
    id: skills
    content:
      title: "Tech Stack"
      subtitle: "Technologies I use to build and automate apps"
      categories:
        - name: Operating Systems & Hypervisors
          items:
            - name: Debian
              icon: devicon/debian
            - name: Ubuntu Server
              icon: devicon/ubuntu
            - name: Proxmox VE
              icon: devicon/proxmox
            - name: Windows Server
              icon: devicon/windows11
        - name: Languages
          items:
            - name: YAML
              icon: devicon/yaml
            - name: Bash Scripting
              icon: devicon/bash
            - name: Python
              icon: devicon/python
            - name: Go
              icon: devicon/go
        - name: Version Control - Containerization - Orchestration
          items:
            - name: Git
              icon: devicon/git
            - name: Docker
              icon: devicon/docker
            - name: Kubernetes
              icon: devicon/kubernetes
            - name: Helm
              icon: devicon/helm
        - name: Networking & Security
          items:
            - name: Cloudflare
              icon: devicon/cloudflare
            - name: OPNSense
              icon: devicon/opnsense
            - name: Nginx
              icon: devicon/nginx
            - name: Traefik
              icon: devicon/traefikproxy
        - name:
          items:
            - name: Authentik
              icon: brands/authentik
            - name: Vaultwarden
              icon: brands/vaultwarden
            - name: Wireguard
              icon: brands/wireguard
            - name: Tailscale
              icon: brands/tailscale
        - name: Storage - Backups - Databases
          items:
            - name: TrueNAS
              icon: brands/truenas
            - name: Mongo DB
              icon: devicon/mongodb
            - name: PostgreSQL
              icon: devicon/postgresql
            - name: Redis
              icon: devicon/redis
        - name: CI/CD - Provisioning - Configuration
          items:
            - name: GitHub Actions
              icon: devicon/githubactions
            - name: Jenkins
              icon: devicon/jenkins
            - name: Ansible
              icon: devicon/ansible
            - name: Terraform
              icon: devicon/terraform
        - name: Monitoring
          items:
            - name: Prometheus
              icon: devicon/prometheus
            - name: Grafana
              icon: devicon/grafana
            - name: InfluxDB
              icon: devicon/influxdb
            - name: Slack
              icon: devicon/slack
    design:
      style: grid
      show_levels: false
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  # Experience Timeline
  - block: resume-experience
    id: experience
    content:
      title: Experience
      date_format: Jan 2006
      items:
        - title: Information Systems Consultant & IT Specialist
          company: 96 High Military Command (Hellenic Armed Forces)
          company_url: ""
          company_logo: ""
          location: Chios, Greece
          date_start: "2026-02-25"
          date_end: "2026-08-25"
          description: |2-
            * **Disaster Recovery Architecture:** Designed and deployed a robust DR solution utilizing Veeam to automate backups from VMware ESXi to a TrueNAS storage environment.
            * **Infrastructure & Network Management:** Administered a Windows Server infrastructure supporting 1,000+ personnel. Maintained and troubleshot the military Local Area Network (LAN), optimizing edge hardware.
            * **Security & Operations:** Enforced strict military-grade security policies and handled classified information while providing Tier 1/2 helpdesk support.
        - title: DevOps Engineer
          company: Fogus Innovations & Services P.C.
          company_url: "https://fogus.gr/"
          company_logo: ""
          location: Athens, Greece
          date_start: "2023-06-01"
          date_end: "2026-01-31"
          description: |2-
            * **Infrastructure Automation:** Engineered automated CI/CD deployment pipelines and custom scripting workflows using Bash and Python.
            * **High-Availability Architecture:** Provisioned, hardened, and maintained on-premise Linux server environments, applying cloud-native fault-tolerance practices.
            * **Systems Optimization:** Troubleshot complex OS-level, virtualization, and networking bottlenecks to ensure continuous service availability.
        - title: Junior DevOps Engineer
          company: Upstream S.A.
          company_url: "https://www.upstreamsystems.com/"
          company_logo: ""
          location: Athens, Greece
          date_start: "2022-05-03"
          date_end: "2023-05-02"
          description: |2-
            * **Operational Automation:** Developed a Python automation tool for the integrity checking of campaign draw results, eliminating manual overhead.
            * **Observability Migration:** Led a migration project from Tableau to Grafana utilizing Helm and the Prometheus Postgres exporter, drastically improving UI loading times from 4 minutes to 15 seconds.
    design:
      columns: "1"
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "1rem", "0"]

  # Education Timeline
  - block: resume-experience
    id: education
    content:
      title: Education
      date_format: Jan 2006
      items:
        - title: M.Sc. in Computer, Telecommunications & Network Engineering
          company: National and Kapodistrian University of Athens
          company_url: "https://www.di.uoa.gr/eng"
          company_logo: ""
          location: Athens, Greece
          date_start: "2023-10-01"
          date_end: "2025-10-27"
          description: |2-
            * **Thesis:** Assessing the Energy and Resilience Trade-offs of Service Mesh Integration and DDoS Mitigation in a Cloud-Native 5G Environment.
            * Published in the Pergamos Digital Library.
        - title: B.Sc. in Informatics and Telecommunications
          company: National and Kapodistrian University of Athens
          company_url: "https://www.di.uoa.gr/en"
          company_logo: ""
          location: Athens, Greece
          date_start: "2017-10-02"
          date_end: "2022-07-04"
          description: |2-
            * **Thesis:** Performance analysis of LoRa and LoRaWAN communications.
    design:
      columns: "1"
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["1rem", "0", "4rem", "0"]

  # Contact Section
  - block: contact-info
    id: contact
    content:
      title: Get In Touch
      subtitle: "Let's build something robust together"
      text: |-
        Whether you want to discuss infrastructure architecture, network security, or open-source deployments, feel free to reach out!
      email: giannisfotis@gmail.com
      autolink: true
    design:
      columns: "1"
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  # CTA Card
  - block: cta-card
    content:
      title: "Open to Opportunities"
      text: |-
        I'm currently targeting **cloud and platform engineering** roles in the Netherlands, Ireland, or Denmark from 2027 onwards.

        Let's connect and discuss how I can help your infrastructure scale.
      button:
        text: "Download Resume"
        url: uploads/resume.pdf
        new_tab: true
    design:
      card:
        css_class: "bg-gradient-to-br from-primary-200 via-primary-100 to-secondary-200 dark:from-primary-600 dark:via-primary-700 dark:to-secondary-700"
        text_color: dark
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "6rem", "0"]
---
