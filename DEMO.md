# Codefresh demo

## Architecture

CI pipeline:
- build > test in composition > update environment repo

GitOps pipeline:
- environment repo webhook > codefresh pipeline to sync to argo > ArgoCD applies manifest

Also implemented but not utilized in pipeline:

- Corrected helm chart to use v3
    - not deployed by ArgoCD correctly
    - possibly still due to version mismatch or local charts
- Codefresh Runner 
    - not utilized due to speed/cost