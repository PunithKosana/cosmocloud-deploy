# Cosmocloud Deploy

This Helm chart deploys a frontend, backend, and Redis database in a Kubernetes cluster.

## Components
1. Backend:
   - Image: `shreybatra/sample-backend`
   - Exposed via ClusterIP at port 8000.
   - REDIS_URI environment variable configured.

2. Frontend:
   - Image: `shreybatra/sample-frontend`
   - Exposed via NodePort 31000.
   - BACKEND_URL environment variable configured.

3. Redis:
   - Image: `redis`
   - Exposed via ClusterIP at port 6379.

## Deployment
Run the following command to deploy the chart:
```bash
helm install testapp cosmocloud-deploy --atomic --timeout 30s
