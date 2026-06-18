---
title: "Cloud Resume Challenge — Azure"
date: 2026-03-01
summary: "Static resume site on Azure with fully automated Terraform pipeline — Blob Storage, CDN, CosmosDB, Azure Functions"
tags:
  - IaC
  - DevOps
  - Terraform
tech_stack:
  - Terraform
  - Azure
  - Python
  - Azure Functions
  - CosmosDB
  - Azure CDN
  - Azure Blob Storage
links:
  - type: github
    url: https://github.com/elvin-builds/cloud-resume-azure
    label: Code
featured: true
status: "Complete"
role: "Solo Engineer"
highlights:
  - "Fully automated Terraform pipeline — zero manual Azure Portal clicks"
  - "Multi-module Terraform: Storage, CosmosDB, Function App, CDN"
  - "Visitor counter API via Azure Functions + CosmosDB"
  - "Resolved Azure Free Trial subscription limitations iteratively"
---

The Cloud Resume Challenge completed on Azure with a fully automated Terraform pipeline.

## Overview

Built a static resume website hosted on Azure with a serverless visitor counter. The entire infrastructure provisioned via Terraform with multi-module architecture.

## Architecture
Custom Domain → Azure CDN/Front Door (HTTPS) → Azure Blob Storage (Static Site) → Azure Functions (Visitor Counter API) → CosmosDB (Counter Storage)
## Key Technical Decisions

### Full Terraform Automation
Everything provisioned via Terraform — including CDN custom domain configuration and CosmosDB throughput settings. Zero Portal clicks.

### Multi-Module Architecture
Separate modules for Storage, CosmosDB, Function App, and CDN — clean separation of concerns and reusability.

### Azure Free Trial Limitations
Worked within Free Trial constraints, iteratively resolving subscription-level limitations for CDN, CosmosDB RU allocation, and Function App SKU restrictions.

## Lessons Learned

1. Azure Free Trial has non-obvious limitations that only surface during `terraform apply`
2. Multi-module Terraform is cleaner but requires careful output/variable wiring
3. CDN + custom domain + HTTPS certificate provisioning is the hardest part to automate
4. Iterative problem-solving matters more than getting it right on the first try
