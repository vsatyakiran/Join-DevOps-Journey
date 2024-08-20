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

<div class="navigation">
    <a href="./day-9.html">← Day 9: Config Management with Ansible</a>
  <a href="../allfiles.html">Back to Home</a>
  <a href="./day-11.html">CI / CD</a>
</div>

