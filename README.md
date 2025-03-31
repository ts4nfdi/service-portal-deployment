# Service Portal Deployment
Service Portal deployment configuration

## Install

```
helm install ts4nfdi-service-portal \
--namespace='ts4nfdi' \
--set-json='ingress.dns="ts4nfdi-service-portal.qa.km.k8s.zbmed.de"' \
--set-json='ingress.path="/"' \
--set-json='images.ui="ghcr.io/ts4nfdi/service-portal:main"' \
--set-json='ui.GATEWAY_BASE_URL="https://ts4nfdi-api-gateway.prod.km.k8s.zbmed.de/api-gateway"' \
--set-json='ui.SMTP_HOST_NAME="example.mailgun.org"' \
--set-json='ui.SMTP_PORT="\"123\""' \
--set-json='ui.SERVICE_EMAIL="example.mailgun.org"' \
repos/service-portal-deployment/k8s/service-portal-ui
```