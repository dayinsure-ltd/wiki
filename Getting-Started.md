# Getting Started

This page covers everything you need to get set up as a new engineer.

## Prerequisites

- [ ] GitHub account added to the org
- [ ] Cloud provider access granted
- [ ] VPN credentials issued
- [ ] Development environment configured

## Required Tools

| Tool | Purpose | Install |
|------|---------|---------|
| `gh` | GitHub CLI | `brew install gh` |
| `terraform` | Infrastructure as code | `brew install terraform` |
| `kubectl` | Kubernetes CLI | `brew install kubectl` |
| `helm` | Kubernetes package manager | `brew install helm` |
| `k9s` | Kubernetes terminal UI | `brew install k9s` |
| `docker` | Containers | [Docker Desktop](https://www.docker.com/products/docker-desktop/) |

## Repository Overview

| Repo | Description |
|------|-------------|
| `app-frontend` | Frontend web application |
| `api-core` | Core backend API |
| `api-support` | Support and internal API |
| `infra-modules` | Reusable Terraform modules |
| `infra-root` | Root infrastructure configuration |
| `cicd` | Shared CI/CD templates and Docker base images |

## First Steps

1. Clone the repos you need
2. Run `gh auth login` to authenticate with GitHub
3. Review the `README.md` in each repo for local setup instructions
4. Join the relevant Slack/Teams channels

## See Also

- [Infrastructure](Infrastructure)
- [Contributing](Contributing)
