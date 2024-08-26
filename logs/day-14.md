---
layout: default
title: Day 14 - Self-hosted Runners in GitHub Actions
---

# Day 14: Self-hosted Runners in GitHub Actions

<div class="date">August 26, 2024</div>

Today, I explored self-hosted runners in GitHub Actions and learned how to set up and use them in my CI/CD workflows. Self-hosted runners allow developers to run workflows on their own infrastructure, providing more control and customization over the execution environment. Here's a summary of what I learned:

## What are GitHub hosted Runners?

[GitHub Actions](https://docs.github.com/en/actions) provides a CI/CD service that allows developers to automate workflows directly from their GitHub repositories. GitHub Actions workflows are defined in YAML files and can be triggered by various events, such as pushes, pull requests, and issue comments. By using GitHub-hosted runners, developers can execute workflows in virtual environments provided by GitHub, which come pre-installed with common tools and dependencies.

GitHub-hosted runners are convenient for running workflows without the need to manage infrastructure, as GitHub takes care of provisioning and maintaining the runner environments. However, there are limitations to GitHub-hosted runners, such as restrictions on resource usage, software configurations, and network access. In cases where workflows require specific hardware, software, or security configurations, self-hosted runners can be used.


## What are Self-hosted Runners?

[Self-hosted runners](https://docs.github.com/en/actions/hosting-your-own-runners/about-self-hosted-runners) in GitHub Actions are custom execution environments that can be hosted on your own infrastructure, such as virtual machines, containers, or physical servers. Self-hosted runners allow you to run workflows in your own environment, providing more control over the hardware, software, and security configurations.

Self-hosted runners can be used to:

- Run workflows that require specific hardware or software configurations not available in GitHub-hosted runners.

- Execute workflows on private networks or behind firewalls that restrict external access.

- Customize the execution environment with specific tools, libraries, or dependencies required by your workflows.

- Scale the execution capacity based on your project's needs by adding or removing self-hosted runners.

## Setting Up Self-hosted Runners for AWS EC2 Ubuntu Instance

To set up self-hosted runners for a repository, I followed these steps:

1. **Create an EC2 Instance:** I launched an Ubuntu EC2 instance on AWS to host the self-hosted runner. The instance was configured with the necessary resources and security settings.

2. **Install and Configure the Runner:** I installed the GitHub Actions self-hosted runner software on the EC2 instance and registered it with my GitHub repository. The runner was configured with the necessary access tokens and settings to communicate with GitHub Actions.

3. **Run Workflows on Self-hosted Runner:** I updated my workflow files to specify that certain jobs should run on the self-hosted runner. By using labels and runner selection criteria, I directed specific jobs to execute on the self-hosted runner instead of the default GitHub-hosted runners.

4. **Monitor and Manage Runners:** I monitored the status and performance of the self-hosted runner using the GitHub Actions interface. I could view the runner's activity, logs, and resource utilization to ensure smooth execution of workflows.

## Key Considerations for Self-hosted Runners

When using self-hosted runners in GitHub Actions, it's important to consider the following:

- **Security:** Ensure that the self-hosted runner environment is secure and isolated from external threats. Use best practices for securing the infrastructure, managing access controls, and monitoring activity.

- **Maintenance:** Regularly update and maintain the self-hosted runner software to ensure compatibility with GitHub Actions. Monitor for updates, security patches, and performance improvements.

- **Scalability:** Plan for scaling the self-hosted runner capacity based on the project's needs. Add or remove runners as needed to handle increased workflow demands or optimize resource utilization.

- **Cost:** Consider the cost implications of running self-hosted runners on cloud infrastructure. Monitor resource usage, optimize configurations, and adjust capacity to minimize costs while meeting performance requirements.

Overall, self-hosted runners in GitHub Actions provide a flexible and customizable way to execute workflows in your own environment. By leveraging self-hosted runners, developers can tailor the execution environment to their specific requirements, improve workflow performance, and enhance security and control over the CI/CD process.

## Resources

- [GitHub Actions Documentation - Self-hosted Runners](https://docs.github.com/en/actions/hosting-your-own-runners/about-self-hosted-runners)

- [GitHub Actions Self-hosted Runner Repository]()

<div class="navigation">
    <a href="./day-13.html">← GitHub Actions</a>
  <a href="../allfiles.html">Back to Home</a>
  <a href="./day-15.html">Project Management Tools</a>
</div>