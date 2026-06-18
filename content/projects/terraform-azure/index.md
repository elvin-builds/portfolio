---
title: "Terraform Azure Infrastructure"
date: 2026-06-01
summary: "Azure infrastructure provisioned with Terraform — remote state, reusable modules, workspaces, and lifecycle management"
tags:
  - IaC
  - DevOps
  - Terraform
tech_stack:
  - Terraform
  - Azure
  - Azure Storage
  - Azure Container Registry
links:
  - type: github
    url: https://github.com/elvin-builds/terraform-lab
    label: Code
featured: true
status: "Complete"
role: "Solo Engineer"
highlights:
  - "Remote state with Azure Storage backend and state locking"
  - "Reusable modules for Resource Group, ACR, Storage"
  - "Workspaces for multi-environment management (dev/staging/prod)"
  - "terraform import for brownfield infrastructure adoption"
---

Production-grade Terraform project demonstrating Infrastructure as Code best practices on Azure.

## Overview

Built a modular Terraform codebase that provisions Azure infrastructure with remote state management, reusable modules, and multi-environment support via workspaces.

## Key Concepts Demonstrated

### Remote State with Locking
State stored in Azure Storage Account with blob lease locking — prevents concurrent modifications in team environments.

### Reusable Modules
Each Azure resource type wrapped in a module with inputs, outputs, and sensible defaults.

### Workspaces
`terraform workspace` used to manage dev/staging/prod environments from the same codebase. Each workspace maintains separate state.

### Count vs for_each
Both approaches demonstrated — `count` for simple duplication, `for_each` for map-based resource creation with meaningful keys.

### Import & Lifecycle
Used `terraform import` to bring existing Azure resources under Terraform management. Lifecycle rules for protecting critical resources.

## Lessons Learned

1. Always use remote state with locking in team environments
2. `for_each` is almost always better than `count` — resource keys survive reordering
3. Modules should be opinionated but configurable — sensible defaults with override capability
4. `terraform plan` before every `apply` — no exceptions
