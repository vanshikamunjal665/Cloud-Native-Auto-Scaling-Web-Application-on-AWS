# Cloud-Native Auto Scaling Web Application on AWS

Extends an EC2 Auto Scaling + Load Balancing project with: Terraform IaC,
a Flask backend + Streamlit live dashboard, EC2 vs ECS/Fargate comparison,
CI/CD, monitoring, and load testing.


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
