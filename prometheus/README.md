## Prometheus Helm chart
https://github.com/prometheus-community/helm-charts/tree/main/charts/prometheus

### Install
```
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
```
### Usage

Commit changes to values.yaml and generate the template to make changes.

```
helm template prometheus prometheus-community/prometheus --output-dir . --version 15.11.0 -f values.yaml ```

Do not edit the files in `prometheus/templates/` directly.