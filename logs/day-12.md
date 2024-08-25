---
layout: default
title: Day 12 - Jenkins
---

# Day 12: Jenkins

<div class="date">August 24, 2024</div>

Today, I explored Jenkins, an open-source automation server that supports building, testing, and deploying software projects. Jenkins is widely used for implementing Continuous Integration and Continuous Deployment (CI/CD) pipelines. Here's a summary of what I learned:

## What is Jenkins?

[Jenkins](https://www.jenkins.io/) is an open-source automation server written in Java that helps automate various aspects of the software development process. It allows developers to define and run CI/CD pipelines to build, test, and deploy code changes efficiently. Jenkins provides a web-based interface for creating and managing pipelines, making it easy to set up automated workflows.

## Key Features of Jenkins

Some key features of Jenkins include:

- **Extensibility:** Jenkins supports a wide range of plugins that extend its functionality. Developers can install plugins to integrate Jenkins with other tools and services, such as version control systems, build tools, and deployment platforms.

- **Distributed Builds:** Jenkins can distribute build tasks across multiple machines, allowing developers to scale their build infrastructure based on workload and resource requirements.

- **Pipeline as Code:** Jenkins supports defining pipelines as code using the Jenkinsfile format. This allows developers to version control their pipeline configurations and automate the creation of CI/CD workflows.

- **Integration with Version Control:** Jenkins integrates with popular version control systems like Git, SVN, and Mercurial, enabling developers to trigger builds automatically when code changes are pushed to repositories.

## Setting Up Jenkins

To set up Jenkins, I followed these steps:

1. **Download and Install Jenkins:** I downloaded the Jenkins WAR file from the [official website](https://www.jenkins.io/download/) and ran it using Java to start the Jenkins server.

2. **Access Jenkins Web Interface:** I accessed the Jenkins web interface by navigating to `http://localhost:8080` in my web browser. I completed the initial setup by unlocking Jenkins using the provided password and installing recommended plugins.

3. **Create a New Pipeline:** I created a new pipeline in Jenkins by defining the pipeline script in the Jenkinsfile format. The pipeline script included stages for checking out source code, building the project, running tests, and deploying artifacts.

4. **Run the Pipeline:** I triggered the pipeline to run manually and observed the build process in the Jenkins web interface. Jenkins executed each stage of the pipeline and displayed the build status and logs for each step.

## Jenkins Plugins

Jenkins provides a vast ecosystem of plugins that enhance its capabilities. Some popular Jenkins plugins include:

- **Git Plugin:** Integrates Jenkins with Git repositories, allowing developers to trigger builds based on code changes.

- **Pipeline Plugin:** Adds support for defining pipelines as code using the Jenkinsfile format.

- **Docker Plugin:** Integrates Jenkins with Docker, enabling developers to build and deploy Docker containers as part of CI/CD workflows.

- **GitHub Integration Plugin:** Integrates Jenkins with GitHub repositories, enabling developers to trigger builds and report build status back to GitHub.

## Benefits of Jenkins

Using Jenkins for CI/CD pipelines offers several benefits, including:

- **Automation:** Jenkins automates the software delivery process, reducing manual intervention and enabling faster feedback on code changes.

- **Scalability:** Jenkins can scale to handle large build workloads by distributing tasks across multiple machines or agents.

- **Extensibility:** Jenkins' plugin ecosystem allows developers to integrate with a wide range of tools and services, customizing their CI/CD workflows to suit their requirements.

- **Visibility:** Jenkins provides a centralized dashboard for monitoring build status, logs, and trends, giving developers and teams visibility into the software delivery process.

Overall, my experience with Jenkins was insightful, and I look forward to exploring more advanced features and best practices for setting up CI/CD pipelines using Jenkins.

That's all for today. Looking forward to diving deeper into Jenkins tomorrow!

<div class="navigation">
    <a href="./day-11.html">← CI/CD</a>
  <a href="../allfiles.html">Back to Home</a>
  <a href="./day-13.html">GitHub Actions</a>
</div>

