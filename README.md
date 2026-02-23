# Platform Repository

This repository contains the platform configuration and application manifests.

## Structure

```
├── argocd/                  # ArgoCD Application definitions
├── crossplane/              # Crossplane Compositions and XRDs
│   ├── definitions/         # CompositeResourceDefinitions (XRDs)
│   └── compositions/        # Compositions (self-hosted, gcp, aws)
├── infrastructure/          # Shared infrastructure per environment/stage
└── environments/            # Application deployments and observability
    └── local/                  # local environment
        └── dev/          # dev stage
        └── test/          # test stage
```

## Environments & Stages

### local
- **Observability**: shared stack in `dxp-local-observability`
- **dev** → https://kubernetes.default.svc (namespace: dxp-dev-apps)
  - Shared resources: postgres, rabbitmq
- **test** → https://kubernetes.default.svc (namespace: dxp-test-apps)
  - Shared resources: postgres

## Available Features

- **postgres** (database)
- **rabbitmq** (messaging)
