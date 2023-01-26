This repository accompanies my answer to <https://stackoverflow.com/q/75218872/147356>.

## Deploying

Assuming that you already have Traefik configured as an Ingress service, you can deploy the services by running:

```
kubectl apply -k services
```

## Notes

I tested this out on a Kind cluster deployed using the configuration in `kind.yaml`:

```
kind create cluster --config kind.yaml
```

I have my local system set up so that once things are deployed I can access Traefik at `192.168.1.201:80` and `192.168.1.201:443`. You would probably need to update this file and the NodePort configuration in `traefik-ingress/kustomization.yaml`.
