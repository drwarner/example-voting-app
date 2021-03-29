# Codefresh demo

## Architecture

CI pipeline:
- build > test in composition (required for merge to master) > update environment repo

GitOps CD pipeline:
- [environment repo](https://github.com/drwarner/k8s-example-voting-app) webhook > codefresh pipeline to sync to argo > ArgoCD applies manifest


Also implemented but not utilized in pipeline:

- Corrected helm chart to use v3
    - not deployed by ArgoCD correctly
    - possibly still due to version mismatch or local charts
- Codefresh Runner 
    - not utilized due to speed/cost