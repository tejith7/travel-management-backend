# Travel Management - GitHub-ready Repo

This repository skeleton includes:
- `backend/` - placeholder Spring Boot backend (sample `Dockerfile` provided)
- `frontend/` - placeholder frontend (sample `Dockerfile` provided)
- `charts/travel-management/` - Helm chart to deploy frontend & backend
- `docker-compose.yml` - local compose for dev
- `.github/workflows/ci.yml` - GitHub Actions workflow to build Docker images and push to registry (configure secrets)
- `README.md` - this file

**How to use**
1. Replace code in `backend/` and `frontend/` with your projects.
2. Update image names in `charts/travel-management/values.yaml`.
3. Build and push images (or use GitHub Actions):
   - Create Docker Hub (or other) repo and set `REGISTRY`, `REGISTRY_USER`, `REGISTRY_PASSWORD` secrets in GitHub.
4. Deploy with Helm:
   ```bash
   helm install travel ./charts/travel-management --values charts/travel-management/values.yaml
   ```

**Helpful commands**
- Build Docker images locally:
  ```bash
  docker build -t yourrepo/travel-backend:latest backend/
  docker build -t yourrepo/travel-frontend:latest frontend/
  ```
- Run docker-compose locally:
  ```bash
  docker-compose up --build
  ```
