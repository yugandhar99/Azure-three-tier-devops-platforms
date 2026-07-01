# GitHub Upload Steps

Create an empty GitHub repository named:

```text
three-tier-devops-azure
```

Do not add README, `.gitignore`, or license from the GitHub website because this project already includes them.

Open CMD inside the extracted project folder and run:

```bash
git init
git add .
git commit -m "Initial commit - Azure three-tier DevOps platform three-tier DevOps platform"
git branch -M main
git remote add origin https://github.com/yugandhar99/three-tier-devops-azure.git
git push -u origin main
```

Only the safe Portfolio Validation workflow runs automatically. Advanced workflows are available in `.github/workflows-disabled/` and can be enabled later.
