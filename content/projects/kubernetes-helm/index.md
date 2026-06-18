---
title: "Kubernetes + Helm Deployment"
date: 2026-06-17
summary: "Kubernetes application deployment with custom Helm charts, multi-environment values, and PostgreSQL via Bitnami chart"
tags:
  - Kubernetes
  - DevOps
  - Helm
tech_stack:
  - Kubernetes
  - Helm
  - Docker
  - Nginx
  - PostgreSQL
  - Minikube
links:
  - type: github
    url: https://github.com/elvin-builds
    label: Code
featured: true
status: "Complete"
role: "Solo Engineer"
highlights:
  - "Custom Helm chart with Go templates and helper functions"
  - "Multi-environment deployment (dev/prod) via values files"
  - "Helm upgrade/rollback with revision history"
  - "PostgreSQL deployed via Bitnami Helm chart"
---

Kubernetes deployment project demonstrating container orchestration and Helm package management.

## Overview

Built Kubernetes manifests and a custom Helm chart for deploying applications with multi-environment support — from raw YAML manifests to templatized Helm releases.

## Key Concepts

### Custom Helm Chart
Built from scratch — Go template syntax, `.Values` and `.Release` objects, pipe operators with `default` and `quote` functions.

### Helper Templates
Shared label definitions in `_helpers.tpl` using `define`/`include` pattern. DRY principle — labels defined once, used everywhere.

### Conditional Resources
Ingress controlled by `if .Values.ingress.enabled` — exists in prod, absent in dev.

### Multi-Environment Values
`values-dev.yaml` (1 replica, debug on) vs `values-prod.yaml` (3 replicas, debug off, ingress enabled). Zero template changes.

### Helm Lifecycle
Full install → upgrade → rollback cycle with revision tracking. Instant rollback to any previous state.

### Public Charts
PostgreSQL deployed via Bitnami chart — one command, fully configured StatefulSet with persistent storage.

## Lessons Learned

1. Helm solves the "8 YAML files × 3 environments" problem elegantly
2. `selector.matchLabels` must be stable — never include version-dependent labels
3. `helm template` before `helm install` — always validate rendered output
4. Not everything needs to be parameterized — hardcode values that never change
