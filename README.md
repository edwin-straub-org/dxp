# Platform Repository

This repository contains the platform configuration and application manifests.

## Structure

```
├── argocd/                  # ArgoCD Application definitions
├── crossplane/              # Crossplane Compositions and XRDs
├── infrastructure/          # Shared infrastructure per environment/stage
└── environments/            # Application deployments
    └── local/                  # local environment
        └── dev/          # dev stage
        └── test/          # test stage
```

## Environments & Stages

### local
- **dev** → https://kubernetes.default.svc (namespace: dxp-dev-apps)
  - Shared resources: postgres, rabbitmq
- **test** → https://kubernetes.default.svc (namespace: dxp-test-apps)
  - Shared resources: postgres

## Available Features

- **postgres** (database)
- **rabbitmq** (messaging)
