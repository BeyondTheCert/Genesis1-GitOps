# Genesis1 GitOps

This repository contains the GitOps configuration for the Genesis1 homelab Kubernetes cluster managed by ArgoCD.

## Cluster Overview

| Node | Role | Hardware |
|------|------|----------|
| master | Control Plane | ThinkPad T480s |
| master2 | Control Plane | ThinkPad T480 |
| worker1 | Worker | ThinkCentre M720q |
| worker2 | Worker | ThinkCentre M720q |

## Stack

| Component | Purpose | Access |
|-----------|---------|--------|
| Kubernetes v1.32 | Container orchestration | - |
| Calico | Pod networking | - |
| MetalLB | Load balancer | 192.168.1.240-250 |
| Nginx Ingress | Traffic routing | - |
| cert-manager | TLS automation | - |
| ArgoCD | GitOps deployments | argocd.beyondthecert.dev |
| Prometheus | Metrics collection | - |
| Grafana | Observability dashboards | grafana.beyondthecert.dev |
| Cloudflare Tunnel | Public access | - |
| Sealed Secrets | Secret management | - |

## Applications

| App | Path | URL |
|-----|------|-----|
| Blog | apps/blog | beyondthecert.dev |
| Immich | apps/immich | Coming soon |

## Repository Structure
## Related Repositories

- [Kubernetes The Homelab Way](https://github.com/BeyondTheCert/Kubernetes-The-Homelab-Way) — Step by step guide to building this cluster
- [beyondthecert.dev](https://beyondthecert.dev) — Blog

## Infrastructure

Infrastructure components are managed via Helm and are intentionally kept outside GitOps for stability. Applications and workloads are managed through this repo via ArgoCD.

## Author

Claude R. Hector | Platform Engineer | beyondthecert.dev
