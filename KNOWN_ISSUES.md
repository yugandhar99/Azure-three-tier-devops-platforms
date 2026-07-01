# Known Issues

- Azure deployment requires subscription setup, resource group, ACR, App Service, and Terraform backend configuration.
- Advanced workflows are disabled by default to avoid failing GitHub Actions checks before credentials are configured.
- Existing infrastructure modules are included, but `terraform plan/apply` should be tested locally or in Azure Cloud Shell before production usage.
