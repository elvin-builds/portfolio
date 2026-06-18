---
title: ''
summary: ''
date: 2026-01-05
type: landing

sections:
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
          - "cloud infrastructure"
          - "CI/CD pipelines"
          - "containerized deployments"
          - "automated systems"
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

  - block: portfolio
    id: projects
    content:
      title: "Projects"
      subtitle: "Hands-on DevOps & Infrastructure work"
      count: 0
      filters:
        folders:
          - projects
      buttons:
        - name: All
          tag: '*'
        - name: DevOps
          tag: DevOps
        - name: IaC
          tag: IaC
        - name: CI/CD
          tag: CI/CD
        - name: Kubernetes
          tag: Kubernetes
      default_button_index: 0
    design:
      columns: 3
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  - block: tech-stack
    id: skills
    content:
      title: "Tech Stack"
      subtitle: "Tools I use daily to build and manage infrastructure"
      categories:
        - name: Containers & Orchestration
          items:
            - name: Docker
              icon: devicon/docker
            - name: Kubernetes
              icon: devicon/kubernetes
            - name: Helm
              icon: devicon/helm
        - name: Infrastructure as Code
          items:
            - name: Terraform
              icon: devicon/terraform
            - name: Ansible
              icon: devicon/ansible
        - name: CI/CD & Version Control
          items:
            - name: GitHub Actions
              icon: brands/github
            - name: Git
              icon: devicon/git
        - name: Cloud & Platforms
          items:
            - name: Azure
              icon: devicon/azure
            - name: AWS
              icon: devicon/amazonwebservices
            - name: Linux
              icon: devicon/linux
            - name: Nginx
              icon: devicon/nginx
        - name: Monitoring & Data
          items:
            - name: Prometheus
              icon: devicon/prometheus
            - name: Grafana
              icon: devicon/grafana
            - name: PostgreSQL
              icon: devicon/postgresql
        - name: Networking & Security
          items:
            - name: Palo Alto
              icon: shield-check
            - name: Cisco
              icon: server
            - name: VMware
              icon: devicon/vsphere
    design:
      style: grid
      show_levels: false
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  - block: resume-experience
    id: experience
    content:
      title: Experience
      date_format: Jan 2006
      items:
        - title: Infrastructure & DevOps Engineer
          company: eTopaz / BalLine
          company_url: 'https://etopaz.az'
          company_logo: ''
          location: Baku, Azerbaijan
          date_start: '2020-01-01'
          date_end: ''
          description: |2-
            * Manage production VMware vSphere infrastructure hosting 50+ VMs across multiple sites
            * Administer Microsoft 365 and Entra ID (Azure AD) for 200+ users with hybrid AD sync
            * Maintain Veeam Backup & Replication for VM and M365 data protection with SureBackup verification
            * Configure and audit Palo Alto and Cisco Firepower firewalls (17 findings, 4 Critical in recent audit)
            * Implement split-brain DNS architecture using conditional forwarders and pinpoint zones
            * Automate server provisioning with Ansible (roles, vault, templates)
            * Build CI/CD pipelines with GitHub Actions (lint → test → Docker build → push to GHCR)
            * Provision Azure infrastructure with Terraform (remote backend, modules, workspaces)
            * Deploy applications to Kubernetes using custom Helm charts with multi-environment values
    design:
      columns: '1'
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  - block: collection
    id: blog
    content:
      title: Recent Posts
      subtitle: ''
      text: ''
      filters:
        folders:
          - blog
        exclude_featured: false
      count: 3
      order: desc
    design:
      view: card
      columns: 3
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  - block: contact-info
    id: contact
    content:
      title: Get In Touch
      subtitle: "Open to remote DevOps & Cloud opportunities"
      text: |-
        I'm actively looking for remote Infrastructure / DevOps / Cloud Engineer roles.
        If you have an opportunity or just want to connect, feel free to reach out!
      email: elvin.hagverdiyev@gmail.com
      autolink: true
    design:
      columns: '1'
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  - block: cta-card
    content:
      title: "Open to Remote Opportunities"
      text: |-
        I'm looking for **remote DevOps / Cloud Engineer** roles where I can bring
        my 5+ years of infrastructure experience and cloud-native skills.
      button:
        text: 'Download Resume'
        url: uploads/resume.pdf
        new_tab: true
    design:
      card:
        css_class: 'bg-gradient-to-br from-primary-200 via-primary-100 to-secondary-200 dark:from-primary-600 dark:via-primary-700 dark:to-secondary-700'
        text_color: dark
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "6rem", "0"]
---
