# Kubernetes YAML Files

This repository stores Kubernetes manifests for multiple applications.

## App Port Summary

| App | Component | Container Port | Service Port | NodePort | Manifest Paths |
| --- | --- | --- | --- | --- | --- |
| `arecgis` | Frontend (`react`) | `80` | `80` | `31123` | `arecgis/frontend.yaml`, `arecgis/svc-frontend.yaml` |
| `arecgis` | Backend (`backend`) | `3001` | `3001` | `31122` | `arecgis/backend.yaml`, `arecgis/svc-backend.yaml` |
| `umans` | Frontend (`umans-frontend`) | `80` | `80` | `31125` | `umans/frontend.yaml`, `umans/svc-frontend.yaml` |
| `umans` | Backend (`umans-backend`) | `3001` | `3001` | `31124` | `umans/backend.yaml`, `umans/svc-backend.yaml` |
| `COE.Vantage` | Frontend (`coe-vantage-frontend`) | `80` | `80` | `30080` | `COE.Vantage/frontend.yaml` |
| `COE.Vantage` | Backend (`coe-vantage-backend`) | `4000` | `4000` | `30081` | `COE.Vantage/backend.yaml` |
| `MSB.io` | File API (`file-api`) | `3000` | `3000` | `31300` | `MSB.io/deployment.yaml`, `MSB.io/service.yaml` |

## Notes

- Deployments define container ports with `containerPort`.
- Services expose workloads internally and externally with `port`, `targetPort`, and `nodePort`.
- Some app directories include config/job manifests that do not expose additional service ports.
