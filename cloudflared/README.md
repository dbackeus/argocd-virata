# Cloudflared

ArgoCD config for deploying https://github.com/cloudflare/cloudflared

## Prerequisites

Assumes a Secret called `tunnel-credentials` exists in the `cloudflared` namespace of your cluster containing the contents of the JSON file created when running `cloudflared tunnel create`, eg:

```bash
kubectl -n cloudflared create secret generic tunnel-credentials \
  --from-file=credentials.json=/Users/<yourusername>/.cloudflared/<tunnel-ID>.json
```
