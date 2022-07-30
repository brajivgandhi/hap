## Elastic Helm chart
https://github.com/prometheus-community/helm-charts/tree/main/charts/prometheus

### Install
```
helm repo add elastic https://helm.elastic.co
helm repo update
```
### Usage

Commit changes to es-values.yaml, filebeat-values.yaml and generate the template to make changes.

```
helm template elk elastic/elasticsearch --output-dir . --version 7.17.3 -f es-values.yaml
helm template elk elastic/filebeat --output-dir . --version 7.17.3 -f filebeat-values.yaml
helm template elk elastic/filebeat --output-dir . --version 7.17.3 -f kibana-values.yaml
``

Do not edit the files in `templates/` directly.