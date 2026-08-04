# Cloud-Native Auto Scaling Web Application on AWS

Extends an EC2 Auto Scaling + Load Balancing project with: Terraform IaC,
a Flask backend + Streamlit live dashboard, EC2 vs ECS/Fargate comparison,
CI/CD, monitoring, and load testing.

## Status

- [x] Phase 1 — Network + IAM + S3 (Terraform)
- [x] Phase 2 — Backend (Flask) + Frontend (Streamlit) + docker-compose
- [ ] Phase 3 — Test locally with docker-compose
- [ ] Phase 4 — ECR + push images
- [ ] Phase 5 — EC2 + Auto Scaling Group
- [ ] Phase 6 — ALB + ECS/Fargate + path routing
- [ ] Phase 7 — Deploy frontend (ECS Fargate)
- [ ] Phase 8 — Lambda cleanup
- [ ] Phase 9 — CI/CD (GitHub Actions)
- [ ] Phase 10 — Monitoring
- [ ] Phase 11 — Load testing
- [ ] Phase 12 — Docs + report

## Local dev

```bash
cd app
docker compose up --build
```

Then open http://localhost:8501 (frontend) — click "Fetch once" and confirm
it reaches the backend at http://localhost:5000/health.

## Terraform

```bash
cd terraform
terraform init
terraform plan
terraform apply
```

Before applying: edit `security.tf` and replace `YOUR_IP/32` with your
actual public IP.
