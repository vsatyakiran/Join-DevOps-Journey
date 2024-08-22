---
layout: default
title: Day 3 - Virtual Machines
---

# Day 3: Virtual Machines and How to create VM on AWS

<div class="date">August 11, 2024</div>

## What are Virtual Machines?

VMs are software computers that provide same functunality as physical computers. It has CPU, RAM, storage, and network interfaces. VMs run on a hypervisor which is installed on a physical server. Each VM runs its own operating system and applications.

## Virtualization and Containerization

- **Virtualization:** Virtualization is the process of creating a virtual version of a physical resource, such as a server, storage device, or network. Virtualization allows multiple virtual machines to run on a single physical machine, enabling greater resource utilization and flexibility.

- **Containerization:** Containerization is a lightweight form of virtualization that allows applications to be packaged with their dependencies and run in isolated environments called containers. Containers are portable, scalable, and efficient, making them ideal for microservices architectures and cloud-native applications.

## Virtual Machines vs. Containers

![VM vs. Container](https://miro.medium.com/v2/resize:fit:1400/1*LnOVwjRvYpC75s-2W8hPTQ.png)

- **Virtual Machines:** VMs are software computers that provide same functunality as physical computers. It has CPU, RAM, storage, and network interfaces. VMs run on a hypervisor which is installed on a physical server. Each VM runs its own operating system and applications.

- **Containers:** Containers are lightweight and portable units of software that package applications and their dependencies together. Containers share the host operating system's kernel and run as isolated processes, making them more efficient and faster to deploy than virtual machines.

<hr> 

- **Bare Metal Server:** A bare-metal server is a physical server that is dedicated to a single tenant. Unlike virtual servers, which share physical hardware with other tenants, bare-metal servers provide exclusive access to the underlying hardware. They are `not virtual servers` running in mutiple piece of shared hardware.

- **HyperVisor:** A hypervisor, also known as a "Virtual Machine Monitor(VMM) or Virtualizer", is a software that creates and runs virtual machines. It allows multiple operating systems to share a single hardware host. Each operating system runs on its own virtual machine. `e.g. VMware, VirtualBox, Hyper-V.` Each VM is called a `guest machine.`

- **Guest Os:** The operating system that runs on a virtual machine is called a guest operating system. It is established and managed by virtual software also known as VMM or hypervisor.

## How to create a Virtual Machine on AWS?

1. **Sign in to the AWS Management Console.**
2. **Open the Amazon EC2 console at [https://console.aws.amazon.com/ec2/](https://console.aws.amazon.com/ec2/).**
3. **In the navigation pane, choose `Instances`, and then choose `Launch Instance`.**
4. **Choose an Amazon Machine Image (AMI):** Select an AMI that meets your requirements, such as an Amazon Linux 2 AMI or a Microsoft Windows Server AMI or any other.
5. **Choose an Instance Type:** Select an instance type based on your requirements, such as t2.micro, t3.medium, m5.large, etc.
6. **Configure the Instance:**  Configure the instance details, such as the number of instances, network settings, IAM role, etc.
7. **Add Storage:** Add storage volumes to the instance, such as EBS volumes.
8. **Add Tags:** Add tags to the instance for easier identification and management.
9. **Configure Security Group:** Configure the security group to control inbound and outbound traffic to the instance.
10. **Review Instance Launch**
11. **Choose `Launch`**

## How to connect to a Virtual Machine?

1. **Connect using SSH:** If you are using a Linux instance, you can connect to the instance using SSH. Use the following command to connect to the instance:

```bash
ssh -i /path/my-key-pair.pem ec2-user@public-DNS-name
```

2. **Connect using RDP:** If you are using a Windows instance, you can connect to the instance using Remote Desktop Protocol (RDP). Use the following steps to connect to the instance:

- **Get the public DNS name of the instance from the console.**
- **Open the Remote Desktop client on your local machine.**
- **Enter the public DNS name of the instance and click `Connect`.**
- **Enter the username and password for the instance.**

## Key Concepts in Virtualization

- **Hypervisor** 
- **Virtual Machine**
- **Bare Metal Server**
- **Guest OS**

  <a href="../day-2.html" >SDLC</a>
  <a href="../allfiles.html">View All Entries</a>
  <a href="./day-4.html" >Linux</a>

