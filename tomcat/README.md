## Tomcat Helm chart

https://artifacthub.io/packages/helm/kubegemsapp/tomcat

### Install
```
helm repo add bitnami https://charts.bitnami.com/bitnami
helm install my-release bitnami/tomcat
```
### Usage

Commit changes to values.yaml and generate the template to make changes.

```
helm template tomcat bitnami/tomcat --output-dir .  --version 10.3.11 -f values.yaml  ```

Do not edit the files in `tomcat/templates/` directly.