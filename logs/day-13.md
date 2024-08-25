---
layout: default
title: Day 13 - GitHub Actions
---

# Day 13: GitHub Actions

<div class="date">August 25, 2024</div>

Today, I explored GitHub Actions, a CI/CD service provided by GitHub that allows developers to automate workflows directly from their GitHub repositories. GitHub Actions enables developers to build, test, and deploy code changes using custom workflows defined in YAML files. Here's a summary of what I learned:

## What are GitHub Actions?

[GitHub Actions](https://docs.github.com/en/actions) is a CI/CD service provided by GitHub that allows developers to automate various tasks directly from their GitHub repositories. With GitHub Actions, developers can define custom workflows in YAML files to build, test, package, release, and deploy code changes. Workflows in GitHub Actions are triggered by events such as pushes, pull requests, issue comments, and more.

Generally workflows are defined in `.github/workflows` directory in the repository. Each workflow is defined in a YAML file and consists of one or more jobs. Each job runs on a separate virtual machine or container and can contain multiple steps. Steps are individual tasks that execute commands or actions, such as checking out code, running tests, or deploying artifacts.

## Key Features of GitHub Actions

Some key features of GitHub Actions include:

- **Integration with GitHub:** GitHub Actions is tightly integrated with GitHub repositories, allowing developers to trigger workflows based on various events within the repository, such as code pushes, pull requests, and issue comments.

- **Customizable Workflows:** Developers can define custom workflows in YAML files, specifying the sequence of jobs, steps, and actions to be executed. Workflows can be tailored to suit specific project requirements and automate complex CI/CD processes.

- **Reusable Actions:** GitHub Actions provides a marketplace of pre-built actions that developers can use in their workflows. Actions are reusable units of code that perform specific tasks, such as building Docker images, deploying to cloud platforms, or sending notifications.

- **Matrix Builds:** GitHub Actions supports matrix builds, allowing developers to run the same job with different configurations, such as different versions of programming languages or operating systems.

## Setting Up GitHub Actions

To set up GitHub Actions for a repository, I followed these steps:

1. **Create a Workflow File:** I created a new workflow file in the `.github/workflows` directory of the repository. The workflow file defined the jobs, steps, and actions to be executed when triggered.

2. **Define Workflow Triggers:** I specified the events that would trigger the workflow, such as pushes to specific branches, pull requests, or issue comments.

3. **Configure Jobs and Steps:** I defined the jobs and steps within the workflow, specifying the tasks to be executed in each job. I used pre-built actions from the GitHub Marketplace to perform common tasks like building, testing, and deploying code.

4. **Run the Workflow:** I triggered the workflow manually or by pushing code changes to the repository. GitHub Actions executed the workflow, running the defined jobs and steps on virtual machines or containers.

## GitHub Actions Marketplace

The GitHub Actions Marketplace provides a wide range of pre-built actions that developers can use in their workflows. Some popular categories of actions include:

- **Build and Test:** Actions for building and testing code, running automated tests, and generating code coverage reports.

- **Deployment:** Actions for deploying code changes to various platforms, such as cloud providers, container registries, and serverless environments.

- **Notifications:** Actions for sending notifications via email, Slack, or other communication channels based on workflow events.

- **Security:** Actions for scanning code for vulnerabilities, checking dependencies, and enforcing security policies.

Overall, GitHub Actions provides a powerful platform for automating CI/CD processes and improving the efficiency of software development workflows. I look forward to exploring more advanced features and use cases of GitHub Actions in future projects.

## Resources

- [GitHub Actions Documentation](https://docs.github.com/en/actions)


<div class="navigation">
    <a href="./day-12.html">← GitHub Actions</a>
  <a href="../allfiles.html">Back to Home</a>
  <a href="./day-14.html">GitHub Project</a>
</div>
