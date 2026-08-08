---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
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
          tag: '*'
        - name: Infrastructure as Code
          tag: Infrastructure
        - name: Systems & Development
          tag: Systems
        - name: Research & Telecom
          tag: Research
      default_button_index: 0
      # Archive link auto-shown if more projects exist than 'count' above
      # archive:
      #   enable: false # Set to false to explicitly hide
      #   text: "Browse All" # Customize text
      #   link: "/work/" # Custom URL
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
      subtitle: "Technologies I use to build things"
      categories:
        - name: Operating Systems
          items:
            - name: Debian
              icon: devicon/debian
            - name: Ubuntu Server
              icon: devicon/ubuntu
            - name: Proxmox VE
              icon: devicon/proxmox
            - name: Windows Server
              icon: devicon/windows11
            # - name: VMware ESXi
            #   icon: devicon/vsphere
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
            # - name: OpenVPN
            #   icon: brands/openvpn
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
        - title: Senior Software Engineer
          company: Tech Corp
          company_url: ""
          company_logo: ""
          location: San Francisco, CA
          date_start: "2023-01-01"
          date_end: ""
          description: |2-
            * Lead development of microservices architecture serving 1M+ users
            * Improved API response time by 40% through optimization
            * Mentored team of 5 junior developers
            * Tech stack: React, Node.js, PostgreSQL, AWS
        - title: Full-Stack Developer
          company: Startup Inc
          company_url: ""
          company_logo: ""
          location: Remote
          date_start: "2021-06-01"
          date_end: "2022-12-31"
          description: |2-
            * Built and deployed 3 production applications from scratch
            * Implemented CI/CD pipeline reducing deployment time by 60%
            * Collaborated with design team on UI/UX improvements
            * Tech stack: Next.js, Express, MongoDB, Docker
        - title: Junior Developer
          company: Web Agency
          company_url: ""
          company_logo: ""
          location: New York, NY
          date_start: "2020-01-01"
          date_end: "2021-05-31"
          description: |2-
            * Developed client websites using modern web technologies
            * Maintained and updated legacy codebases
            * Participated in code reviews and agile ceremonies
            * Tech stack: React, WordPress, PHP, MySQL
    design:
      columns: "1"
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  # Recent Blog Posts
  # - block: collection
  #   id: blog
  #   content:
  #     title: Recent Posts
  #     subtitle: 'Thoughts on web development, tech, and more'
  #     text: ''
  #     filters:
  #       folders:
  #         - blog
  #       exclude_featured: false
  #     count: 3
  #     order: desc
  #   design:
  #     view: card
  #     columns: 3
  #     background:
  #       color:
  #         light: "#f5f5f5"
  #         dark: "#08080c"
  #     spacing:
  #       padding: ["4rem", "0", "4rem", "0"]

  # Contact Section
  - block: contact-info
    id: contact
    content:
      title: Get In Touch
      subtitle: "Let's build something amazing together"
      text: |-
        I'm always interested in hearing about new opportunities.
        Whether you're looking to hire, collaborate, or just want to say hi, feel free to reach out!
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
        I'm currently looking for **software engineering** opportunities.

        Let's connect and discuss how I can help your team.
      button:
        text: "Download Resume"
        url: uploads/resume.pdf
        new_tab: true
    design:
      card:
        # Light mode: soft pastel theme gradient | Dark mode: rich deep gradient
        css_class: "bg-gradient-to-br from-primary-200 via-primary-100 to-secondary-200 dark:from-primary-600 dark:via-primary-700 dark:to-secondary-700"
        text_color: dark
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "6rem", "0"]
---
