# ArgoCD Helm Project

## Overview

This project leverages ArgoCD and Helm to manage Kubernetes applications. The repository is organized to define, deploy, and manage applications using Helm charts, with ArgoCD ensuring continuous delivery and deployment.

## Project Structure

```
.
├── cluster
│   ├── applications
│   │   └── app1.yaml
│   └── root.yaml
├── HelmCharts
│   └── Chart1
│       ├── Chart.yaml
│       ├── templates
│       │   ├── deployment.yaml
│       │   ├── hpa.yaml
│       │   └── service.yaml
│       └── values.yaml
└── README.md
```

### Directory Breakdown

- **cluster**: Contains ArgoCD application definitions.
  - **applications**: Contains individual application manifests.
    - `app1.yaml`: Manifest for `app1` defining its source, project, and sync policies.
  - `root.yaml`: Defines the root ArgoCD application to manage the overall application tree.

- **HelmCharts**: Houses Helm charts for the applications.
  - **Chart1**: Example Helm chart for an application.
    - `Chart.yaml`: Metadata for the Helm chart.
    - `templates`: Contains Kubernetes resource templates.
      - `deployment.yaml`: Template for Kubernetes Deployment.
      - `hpa.yaml`: Template for Horizontal Pod Autoscaler.
      - `service.yaml`: Template for Kubernetes Service.
    - `values.yaml`: Default configuration values for the Helm chart.

## Technologies

- **Kubernetes**: Ensure you have a running Kubernetes cluster.
- **ArgoCD**: Install and configure ArgoCD in your Kubernetes cluster.
- **Helm**: Install Helm for managing Helm charts.
