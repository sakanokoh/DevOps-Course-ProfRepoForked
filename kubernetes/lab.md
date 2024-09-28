# Kubernetes Lab

| **Step** | **Task** |
|----------|----------|
| 1        | Reuse your Docker lab application and database. (Ensure you update the `app/server/database.py` if you are reusing the FastAPI backend app) |
| 2        | Rebuild your Docker image with `python:3.9-alpine`. (Make changes in the Dockerfile as necessary) |
| 3        | Create the manifest files to deploy the app in Kubernetes (without volumes, PVC, or storage class): <br> - `backend-deployment.yaml` <br> - `backend-service.yaml` <br> - `backend-configmap.yaml` (if needed) <br> - `backend-secret.yaml` (if needed) <br> - `database-deployment.yaml` <br> - `database-service.yaml` <br> - `database-configmap.yaml` <br> - `database-secret.yaml` |
| 4        | Provide a `README.md` file to explain how to run the application in Kubernetes. |
| 5        | Add additional endpoints for readiness and liveness probes: <br> - `/health/ready` (for readiness) <br> - `/health/live` (for liveness) |
| 6        | Add readiness and liveness probes HTTP configurations in the `backend-deployment.yaml` manifest file. |
| 7        | Add a BusyBox init container to check the database service availability before scheduling the backend application. |
| 8        | Expose the backend server as a NodePort service. The NodePort port should be between `30000` and `30080`. |