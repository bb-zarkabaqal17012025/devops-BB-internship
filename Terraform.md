# Terraform Basics

Terraform is an open-source Infrastructure as Code (IaC) tool developed by HashiCorp that enables users to define, provision, and manage infrastructure using a declarative configuration language called HCL (HashiCorp Configuration Language).

## Why Use Terraform?

1. **Infrastructure as Code (IaC)** – Automates infrastructure management.
2. **Declarative Configuration** – Defines the desired state of infrastructure.
3. **Multi-Cloud Support** – Works with AWS, Azure, GCP, Kubernetes, etc.
4. **State Management** – Keeps track of infrastructure state.
5. **Modular and Reusable** – Facilitates code reuse for maintainability.

## Key Concepts

### 1️⃣ Providers
Terraform interacts with cloud platforms through Providers (e.g., AWS, Azure, GCP). Each provider requires authentication.

```hcl
provider "aws" {
  region = "us-east-1"
}
```

### 2️⃣ Resources
A resource is a component of infrastructure (e.g., EC2 instance, S3 bucket).

```hcl
resource "aws_instance" "my_instance" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"
}
```

### 3️⃣ Variables
Variables allow parameterization in Terraform configurations.

```hcl
variable "instance_type" {
  default = "t2.micro"
}

resource "aws_instance" "example" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = var.instance_type
}
```

### 4️⃣ Outputs
Outputs display or export values from Terraform.

```hcl
output "instance_ip" {
  value = aws_instance.example.public_ip
}
```

### 5️⃣ State File
Terraform maintains a state file (`terraform.tfstate`) that records the current state of resources.

## Terraform Workflow

1. **Initialize Terraform** (downloads providers and sets up the environment):
   ```sh
   terraform init
   ```

2. **Plan Changes** (shows the execution plan):
   ```sh
   terraform plan
   ```

3. **Apply Changes** (provisions resources):
   ```sh
   terraform apply
   ```

4. **Destroy Resources** (removes infrastructure):
   ```sh
   terraform destroy
   ```

