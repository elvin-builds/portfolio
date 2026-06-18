---
title: "Docker + CI/CD Pipeline"
date: 2026-05-15
summary: "Full CI/CD pipeline with GitHub Actions: lint → test → Docker multi-stage build → push to GHCR with branch protection and secret management"
tags:
  - DevOps
  - CI/CD
  - Docker
tech_stack:
  - Docker
  - GitHub Actions
  - Python
  - Flask
  - GHCR
links:
  - type: github
    url: https://github.com/elvin-builds/docker-lab
    label: Code
featured: true
status: "Complete"
role: "Solo Engineer"
highlights:
  - "Multi-stage Docker build reducing image size by 60%"
  - "Automated pipeline: lint → test → build → push on every PR"
  - "Branch protection with required status checks"
  - "Secret management via GitHub encrypted secrets"
---

End-to-end CI/CD pipeline demonstrating containerization best practices and automated deployment workflows.

## Overview

Built a complete CI/CD pipeline that automatically tests, builds, and publishes Docker images on every push. The project demonstrates production-grade practices including multi-stage builds, layer caching, and automated quality gates.

## Pipeline Flow

Developer Push → GitHub Actions → Lint (flake8) → Test (pytest) → Docker Build (multi-stage) → Push to GHCR

## Key Technical Decisions

### Multi-Stage Docker Build
Used a two-stage build to separate build dependencies from the runtime image — reducing the final image size by 60%.

### Branch Protection
GitHub branch protection rules requiring all CI checks to pass before merge.

### Secret Management
Docker registry credentials stored as GitHub encrypted secrets. Used `GITHUB_TOKEN` for GHCR authentication.

## Lessons Learned

1. Dockerfile layer ordering directly impacts build speed — put least-changing layers first
2. Multi-stage builds are essential for production — never ship build tools in runtime images
3. Branch protection + required checks = quality gate that prevents broken code from reaching main
