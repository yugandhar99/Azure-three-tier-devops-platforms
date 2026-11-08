# Three-Tier DevOps Platform on Azure

A production-style DevOps project for deploying a **React frontend**, **Spring Boot backend**, and **MySQL database** using **Docker**, **Terraform**, **Azure App Service**, **Azure Container Registry**, **Azure Front Door**, and secure CI/CD practices.

This project keeps the original three-tier application recipe and upgrades the DevOps layer with modern portfolio-ready practices such as OIDC-based cloud authentication notes, security scanning, SBOM workflow design, runbooks, and safe GitHub Actions validation.

## Architecture

Generated project visual assets and any existing snapshots are included below to make the repository clear and professional for GitHub visitors.

![Azure DevOps Architecture](static/images/azure-devops-architecture.png)

### Existing infrastructure snapshot

![Existing Azure architecture](infra/static/images/architecture.png)

## CI/CD and DevSecOps Flow

![Azure CI/CD DevSecOps](static/images/azure-cicd-devsecops.png)

### Existing push pipeline snapshot

![Push Pipeline](static/images/cicd/push.png)

### Existing pull request pipeline snapshot

![Pull Request Pipeline](static/images/cicd/pr.png)


## Portfolio visuals and career progression

These visuals were added so the project looks complete even when live cloud screenshots are not available. They explain the architecture, DevOps workflow, and how this project represents a step forward in cloud/platform engineering.

![Portfolio Overview](static/images/generated/azure-portfolio-overview.png)

![Career Progression](static/images/generated/azure-career-progression.png)

## What this project demonstrates

- React frontend containerization
- Spring Boot backend containerization
- MySQL database integration
- Docker Compose local development
- Terraform-based Azure infrastructure
- Azure App Service container deployment model
- Azure Container Registry image flow
- Azure Front Door style global entry point
- GitHub Actions portfolio validation
- Jenkins pipeline example
- Optional Trivy, CodeQL, Checkov, and SBOM workflow design
- AI-ready release summary script

## Project structure

```text
.
├── src/                    # Frontend, backend, database samples, Docker Compose
├── infra/                  # Terraform modules for Azure infrastructure
├── .github/                # Safe portfolio validation workflow
├── docs/                   # Runbook, workflow, GenAI, screenshot notes
├── scripts/                # AI-ready release summary helper
├── Jenkinsfile             # Jenkins CI/CD pipeline example
└── README.md
```

## Local development

```bash
cd src
docker compose up --build
```

Frontend: `http://localhost:4200`

## Azure deployment flow

1. Build frontend and backend Docker images.
2. Push images to Azure Container Registry.
3. Provision infrastructure using Terraform.
4. Deploy containers to Azure App Service.
5. Route public traffic through Azure Front Door or the configured app endpoint.

## Jenkins pipeline

A Jenkinsfile is included to show a real CI/CD flow:

```text
Checkout → Frontend Build → Backend Build → Docker Build → Trivy Scan → Push to ACR → Terraform Validate
```

The cloud deployment steps are intentionally portfolio-safe until Azure credentials, ACR name, and environment configuration are added.

## GitHub Actions note

Only a safe **Portfolio Validation** workflow runs automatically. Advanced workflows from the original project are preserved in `.github/workflows-disabled/` and can be enabled later after configuring Azure OIDC credentials, ACR, Terraform backend, and environment variables.

## Security practices

- No `.env`, `.pem`, `.tfstate`, or cloud secrets committed
- Terraform state backend example included but not active by default
- Runtime values use environment variables and Azure configuration
- OIDC-based Azure authentication documented for future deployment
- Security scanning and SBOM workflows kept as enable-later examples

## Future improvements

- Enable Azure OIDC deployment workflow
- Add Azure Monitor dashboards and alerts
- Add blue/green deployment approval gates
- Add Key Vault integration for runtime secrets
- Add full Trivy/Checkov/CodeQL workflow after secrets are configured

## Known issues

See [KNOWN_ISSUES.md](KNOWN_ISSUES.md).


---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:2C5364,100:00C9FF&height=120&section=footer&text=Let's%20Connect&fontColor=ffffff&fontSize=32&fontAlignY=70" />
</p>

<h2 align="center">🤝 Connect With Me</h2>

<p align="center">
  <em>
    Thanks for visiting this project! I’m continuously building hands-on DevOps, Cloud, Automation, and AI-enabled engineering projects to improve real-world deployment, monitoring, and infrastructure skills.
  </em>
</p>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=22&duration=2500&pause=800&color=00C9FF&center=true&vCenter=true&width=650&lines=DevOps+%7C+Cloud+%7C+Automation;CI%2FCD+%7C+Docker+%7C+Kubernetes+%7C+Terraform;Building+real-world+projects+one+commit+at+a+time" alt="Typing SVG" />
</p>

<p align="center">
  <a href="https://github.com/yugandhar99" target="_blank" rel="noopener noreferrer">
    <img src="https://img.shields.io/badge/GitHub-Follow-181717?style=flat&logo=github&logoColor=white" alt="GitHub" />
  </a>
  <a href="https://www.linkedin.com/in/yugandhar-devops" target="_blank" rel="noopener noreferrer">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://yugandhar-portfolio-psi.vercel.app/" target="_blank" rel="noopener noreferrer">
    <img src="https://img.shields.io/badge/Portfolio-View%20My%20Work-FF5722?style=flat&logo=vercel&logoColor=white" alt="Portfolio" />
  </a>
  <a href="mailto:yugandharethamukkala1999@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact%20Me-D14836?style=flat&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Focus-DevOps%20Engineering-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/Cloud-AWS%20%7C%20Azure%20%7C%20GCP-orange?style=flat-square" />
  <img src="https://img.shields.io/badge/IaC-Terraform-purple?style=flat-square" />
  <img src="https://img.shields.io/badge/Containers-Docker%20%7C%20Kubernetes-2496ED?style=flat-square" />
</p>

---

<p align="center">
  ⭐ If this project added value, feel free to star the repository and connect with me!
</p>

<p align="center">
  <strong>Built with ❤️ using modern DevOps practices</strong>
</p>

