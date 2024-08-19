---
layout: default
title:  Day 9: Config Management with Ansible
---

# Day 9: Config Management with Ansible

<div class="date">August 18, 2024</div>

Today, I learned about Ansible, a configuration management tool that allows you to automate the provisioning, configuration, and deployment of infrastructure and applications. Here's what I learned:


## Configuration Management

If there are multiple servers it is difficult to manage/configure each server individually. It is where configuration management used to configure multiple servers at once.

**Tools:** Puppet, Chef, Ansible are some tools that are used for configuration management.

## What is Ansible?

Ansible is an open-source automation tool that simplifies IT orchestration, configuration management, and application deployment. It uses a simple and human-readable language called YAML to define playbooks that describe the desired state of your infrastructure. Ansible can be used to automate tasks such as installing software, configuring servers, and deploying applications.

Ansible automates the management of remote systems and controls their desired state.

Most Ansible environments have three main components:

**Control node:** A system on which Ansible is installed. You run Ansible commands such as ansible or ansible-inventory on a control node.

**Inventory:** A list of managed nodes that are logically organized. You create an inventory on the control node to describe host deployments to Ansible. stores the ip address of target server

**Managed node:** A remote system, or host, that Ansible controls. Managed nodes are also sometimes called "hosts." Ansible is not installed on managed nodes.

## Key Concepts in Ansible

### 1. Inventory

- **Description:** A list of hosts or nodes that Ansible manages.

### 2. Playbooks

- **Description:** YAML files that define a set of tasks to be executed on hosts.

### 3. Tasks

- **Description:** Individual actions or commands to be executed on hosts.

### 4. Roles

- **Description:** Organizational units for playbooks that group related tasks together.

### 5. Modules

- **Description:** Reusable units of code that perform specific tasks on hosts.

### 6. Handlers 

- **Description:** Tasks that are triggered by other tasks and run only if the task has made changes.

### 7. Facts

- **Description:** Information about the managed nodes that Ansible gathers and stores.

# Installing Ansible

You can install Ansible on Linux, macOS, and Windows systems. Here's how to install Ansible on different operating systems:

### On macOS

You can install Ansible on macOS using the following commands:

```bash
brew install ansible
```

### On Linux

You can install Ansible on Linux using the package manager of your distribution.


### On Ubuntu

You can install Ansible on Ubuntu using the following commands:

```bash
sudo apt update
sudo apt install ansible
```

### On CentOS

You can install Ansible on CentOS using the following commands:

```bash
sudo yum install epel-release
sudo yum install ansible
```

After installing Ansible, you can verify the installation by running the following command:

```bash
ansible --version
```

This command will display the Ansible version and other information about the installation.

### On Windows

You can install Ansible on Windows using the Windows Subsystem for Linux (WSL) or a virtual machine running a Linux distribution.

# Ansible Playbooks

Ansible playbooks are YAML files that define a set of tasks to be executed on hosts. Playbooks are used to automate infrastructure configuration, application deployment, and other tasks. Here's an example of an Ansible playbook that installs Nginx on a group of hosts:

```yaml
---

- name: Install Nginx
  hosts: webservers
  tasks:
    - name: Install Nginx
      apt:
        name: nginx
        state: present
```

In this playbook:

- `name`: Name of the playbook.
- `hosts`: Group of hosts to run the tasks on.
- `tasks`: List of tasks to be executed.
- `apt`: Ansible module to install packages on Debian-based systems.

You can run an Ansible playbook using the `ansible-playbook` command:

```bash
ansible-playbook playbook.yml
```

# Ansible Configuration

Ansible uses a configuration file called `ansible.cfg` to define settings such as the inventory file location, remote user, and SSH private key. You can create a configuration file in the following format:

```ini
[defaults]
inventory = /path/to/inventory
remote_user = username
private_key_file = /path/to/private_key
```

You can place this configuration file in the Ansible project directory or in the `/etc/ansible/` directory.

# Ansible Inventory

The Ansible inventory file is used to define the hosts or nodes that Ansible manages. You can create an inventory file in the following format:

```ini
[webservers]
web1 ansible_host= 
web2 ansible_host=
```

In this inventory file:

- `[webservers]`: Group name for the hosts.
- `web1`, `web2`: Hostnames of the servers.
- `ansible_host`: IP address of the server.

You can define multiple groups and hosts in the inventory file to manage different sets of servers.

# Ansible commands

To run Ansible ad-hoc commands, you can use the `ansible` command:

```bash
ansible webservers -m ping
```

This command will ping the hosts in the `webservers` group to check if they are reachable.


## Running Ansible Playbooks

To run an Ansible playbook, you can use the `ansible-playbook` command:

```bash
ansible-playbook playbook.yml
```

This command will execute the tasks defined in the playbook on the specified hosts.

# Resources

- [Ansible Documentation](https://docs.ansible.com/)

<hr>

# Interview Question

1. What is the programming language ansible use?

A. Ansible uses YAML (Yet Another Markup Language) for writing playbooks. YAML is a human-readable data serialization language that is commonly used for configuration files and data exchange. It is easy to read and write, making it a good choice for defining the desired state of infrastructure in Ansible playbooks.  

2. Ansible connects to Linux using SSH protocol, connects to windows using Win RM protocol

3. Puppet vs Ansible 

A. **Puppet** is a configuration management tool that uses a declarative language to define the desired state of systems. It uses a client-server architecture where the Puppet master server manages the configuration of client nodes. Puppet is well-suited for managing large and complex infrastructures.

**Ansible** is a configuration management tool that uses an agentless architecture and SSH to manage systems. It uses a push mechanism to apply configurations to remote systems. Ansible is well-suited for automating tasks and managing small to medium-sized infrastructures.

4. Is ansible a push mechanism or pull mechanism?

   - **push mechanism :** Push mechanism is where the control machine pushes the configuration to the target machine.
   - **pull mechanism :** Pull mechanism is where the target machine pulls the configuration from the control machine.

A. Ansible is a push mechanism 


5. What is the difference between Ansible and Jenkins?

A. Jenkins is a continuous integration and continuous deployment tool, while Ansible is a configuration management tool.

6. What is the difference between Ansible and Terraform?

A. Ansible is a configuration management tool that automates the management of remote systems, while Terraform is an infrastructure as code tool that automates the provisioning of cloud resources.

7. What is the difference between Ansible and Docker?

A. Ansible is a configuration management tool that automates the management of remote systems, while Docker is a containerization platform that allows you to package and run applications in containers.

8. What is the difference between Ansible and Kubernetes?

A. Ansible is a configuration management tool that automates the management of remote systems, while Kubernetes is a container orchestration platform that automates the deployment, scaling, and management of containerized applications.


## Conclusion

Ansible is a powerful tool for automating infrastructure and application deployment tasks. By using Ansible playbooks, you can define the desired state of your infrastructure and easily manage configuration changes across your environment.

<div class="navigation">
    <a href="day-8.html">First APP in AWS</a>
    <a href="../allfiles.html"> All Files </a>
    <a href="day-10.html">Terraform</a>
</div>
