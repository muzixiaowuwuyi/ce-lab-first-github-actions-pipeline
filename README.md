# Lab M5.01 - First GitHub Actions Pipeline
 
## What This Repository Does
Demonstrates a GitHub Actions CI pipeline for Terraform that automatically
runs formatting checks, validation, and planning on every push and pull request.
 
## Pipeline Steps
1. **Checkout** — clones the repository
2. **Setup Terraform** — installs Terraform 1.6.0
3. **Format Check** — runs `terraform fmt -check`
4. **Init** — initializes providers (no backend)
5. **Validate** — checks configuration syntax
6. **Plan** — generates an execution plan
 
## Terraform Resources
- S3 bucket with versioning, encryption, and public access block
- Lifecycle rules for cost optimization (feature branch)
 
## How to Use
\`\`\`bash
# Clone and init
git clone <your-repo-url>
cd ce-lab-first-github-actions-pipeline
terraform init
 
# Run locally
terraform fmt -check
terraform validate
terraform plan
\`\`\`
 
## Secrets Required
| Secret | Description |
|--------|-------------|
| `AWS_ACCESS_KEY_ID` | IAM access key |
| `AWS_SECRET_ACCESS_KEY` | IAM secret key |