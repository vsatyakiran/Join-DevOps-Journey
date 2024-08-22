---
layout: default
title: Day 10 - Infrastructure as Code with Terraform
---

# Day 10: Infrastructure as Code with Terraform

<div class="date">August 20, 2024</div>

Today, I delved into the world of Infrastructure as Code (IaC) with Terraform. Here's a summary of what I learned:

## Infrastructure as Code (IaC)

Infrastructure as Code (IaC) is the practice of managing and provisioning infrastructure through machine-readable definition files, rather than physical hardware configuration or interactive configuration tools. IaC allows you to automate the process of setting up and managing infrastructure, making it more efficient, scalable, and consistent.

**Benefits of IaC:**

- **Consistency:** Infrastructure configurations are defined in code, ensuring consistency across environments.

- **Scalability:** IaC allows you to easily scale infrastructure up or down based on demand.

- **Efficiency:** Automation reduces manual errors and speeds up the deployment process.

- **Version Control:** Infrastructure code can be versioned and tracked using tools like Git.

## What is Terraform?

Terraform is an open-source Infrastructure as Code tool created by HashiCorp. It allows you to define and provision infrastructure using a declarative configuration language. Terraform supports multiple cloud providers, on-premises infrastructure, and third-party services, making it a versatile tool for managing infrastructure.

Terraform uses HashiCorp Configuration Language (HCL) to define infrastructure configurations. HCL is a human-readable language that allows you to describe the desired state of your infrastructure in a simple and concise manner.

## Key Concepts in Terraform

- **Providers:** Providers are plugins that Terraform uses to interact with APIs of various infrastructure platforms (e.g., AWS, Azure, Google Cloud).

- **Resources:** Resources are the building blocks of infrastructure in Terraform. They represent the various components of your infrastructure (e.g., virtual machines, networks, databases).

# Terraform Workflow

The typical workflow for using Terraform involves the following steps:

1. **Define Infrastructure:** Write Terraform configuration files (.tf) to define the desired state of your infrastructure.

2. **Initialize Terraform:** Run `terraform init` to initialize the working directory and download the necessary providers.

3. **Plan Infrastructure:** Run `terraform plan` to create an execution plan that shows what Terraform will do when you apply the configuration.

4. **Apply Infrastructure:** Run `terraform apply` to apply the configuration and provision the infrastructure.

5. **Destroy Infrastructure:** Run `terraform destroy` to tear down the infrastructure and clean up resources.

## Example Terraform Configuration

Here's an example of a simple Terraform configuration that creates an AWS EC2 instance:

```hcl
provider "aws" {
  region = "us-west-2"
}

resource "aws_instance" "example" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"
}
```

# Terraform vs Anisible vs Vagrant

- **Terraform:** Terraform is an Infrastructure as Code tool that focuses on provisioning and managing infrastructure resources across various cloud providers and services.

- **Ansible:** Ansible is a configuration management tool that automates software provisioning, configuration management, and application deployment. It is more focused on configuration management rather than infrastructure provisioning.

- **Vagrant:** Vagrant is a tool for building and managing virtual machine environments in a single workflow. It is used for creating development environments that closely mirror production environments.







<div class="navigation">
    <a href="./day-9.html">← Day 9: Config Management with Ansible</a>
  <a href="../allfiles.html">Back to Home</a>
  <a href="./day-11.html">CI / CD</a>
</div>

