# Nexterm Helm Chart Unofficial

![Version](https://img.shields.io/github/v/release/vuisme/nexterm-helmchart)
[![Release Charts](https://github.com/vuisme/nexterm-helmchart/actions/workflows/release-helm-repo.yml/badge.svg)](https://github.com/vuisme/nexterm-helmchart/actions/workflows/release-helm-repo.yml)
The Nexterm Helm Chart provides Helm charts for deploying the Nexterm application on Kubernetes.

## Version

The current version of the Helm chart is ![Version](https://img.shields.io/github/v/release/vuisme/nexterm-helmchart).

## Build Status

[![Release Charts](https://github.com/vuisme/nexterm-helmchart/actions/workflows/release-helm-repo.yml/badge.svg)](https://github.com/vuisme/nexterm-helmchart/actions/workflows/release-helm-repo.yml)

This badge indicates the current build status of the Helm chart. For detailed information about builds, check [Actions](https://github.com/vuisme/nexterm-helmchart/actions).

## Installation Guide

To install the Nexterm Helm Chart, you need Helm installed on your system. If Helm is not installed, please refer to the [Helm documentation](https://helm.sh/docs/intro/install/) for instructions.

### Installing the Chart

1. **Add the chart repository to Helm:**

   ```bash
   helm repo add nexterm https://vuisme.github.io/nexterm-helmchart
   ```

2. **Update the repository:**

   ```bash
   helm repo update
   ```

3. **Install the Helm chart:**

   ```bash
   helm install my-nexterm nexterm/nexterm-helmchart
   ```

   Replace `my-nexterm` with the name you want to give your release.

### Configuration

You can configure the values of the Helm chart by creating a custom `values.yaml` file. Below is an example configuration:

   ```yaml
   replicaCount: 2
   image:
     repository: nexterm/nexterm-app
     tag: latest
   service:
     type: ClusterIP
     port: 80
   ```

After creating the `values.yaml` file, you can install the chart with custom configuration using the command:

   ```bash
   helm install my-nexterm nexterm/nexterm-helmchart -f values.yaml
   ```

## Uninstalling

To uninstall a Helm chart release, use the following command:

   ```bash
   helm uninstall my-nexterm
   ```

## References

- [Helm Documentation](https://helm.sh/docs/)
- [Kubernetes Documentation](https://kubernetes.io/docs/)

## Contact

If you encounter any issues or have questions, please open an issue on [GitHub](https://github.com/vuisme/nexterm-helmchart/issues).

---

Happy deploying!
