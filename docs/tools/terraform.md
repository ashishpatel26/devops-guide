# Terraform Cheat Sheet

Terraform is an Infrastructure as Code (IaC) tool.

## Basic Commands

| Command | Description |
| :--- | :--- |
| `terraform init` | Initialize the working directory |
| `terraform plan` | Show changes to be applied |
| `terraform apply` | Apply the changes |
| `terraform destroy` | Destroy the infrastructure |
| `terraform validate` | Check if configuration is valid |

## Example: Create a Local File

Save as `main.tf`:

```hcl
resource "local_file" "example" {
  content  = "Hello, DevOps!"
  filename = "${path.module}/hello.txt"
}
```

Run:

```bash
terraform init
terraform apply
```