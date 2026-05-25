# EKS CI/CD Pipeline with GitHub Actions, Helm & OIDC

A production-ready CI/CD pipeline that automatically builds, 
pushes, and deploys a containerized application to AWS EKS 
using GitHub Actions, Docker, Helm, and OIDC authentication.

## Architecture

GitHub Push → GitHub Actions → ECR → EKS (via Helm)

## Tools Used

- Docker & Multi-stage builds
- Kubernetes & Helm
- GitHub Actions (OIDC — no static AWS keys)
- AWS EKS & ECR
- Nginx Ingress Controller

## What This Solves

Startups using static AWS credentials in GitHub secrets are 
one leaked key away from a full account compromise. This 
pipeline uses OIDC identity federation — no long-lived 
credentials stored anywhere.

## Project Structure

\`\`\`
.github/workflows/  → CI/CD pipeline
app/                → Flask app + Dockerfile
helm/app-chart/     → Kubernetes Helm chart
\`\`\`

## How To Deploy

1. Create EKS cluster
2. Set up OIDC trust between GitHub and AWS IAM
3. Add AWS_ROLE_ARN to GitHub secrets
4. Push to main branch — pipeline runs automatically

## Contact

Available for freelance DevOps projects.
📩 devops.rishabhmishra@gmail.com
