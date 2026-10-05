# E-Commerce Cart

This project is a simple e-commerce cart app with automated CI/CD and Kubernetes deployment setup.

## Local Development

```bash
npm install
npm start
```

## CI/CD

The GitHub Actions workflow runs tests on every push and pull request to `main`, then builds and pushes a Docker image to GitHub Container Registry on merges to `main`.

## Kubernetes Deployment

Apply the manifests in `k8s/` to deploy the app:

```bash
kubectl apply -f k8s/
```

Before deployment, update the image path in `k8s/deployment.yaml` to match your GitHub username/org.
