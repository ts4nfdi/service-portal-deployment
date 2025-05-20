# Service Portal Deployment
Service Portal deployment configuration

## Install

```
helm install ts4nfdi-service-portal \
--namespace='ts4nfdi' \
--set-json='ingress.dns="ts4nfdi-service-portal.qa.km.k8s.zbmed.de"' \
--set-json='images.ui="ghcr.io/ts4nfdi/service-portal:main"' \
--set-json='ingress.path="/"' \
repos/service-portal-deployment/k8s/service-portal-ui
```