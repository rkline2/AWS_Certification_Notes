## EC2 Overview

**[Elastic Compute Cloud (EC2)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html)** allows you to launch Virtual Machines (VM)​. When we launch a Virtual Machine we call it an ”instance”​.

### What is a Virtual Machine?​

    A Virtual Machine (VM) is an emulation of a physical computer using software. ​

    Server Virtualization allows you to easily create, copy, resize or migrate your server.​

    Multiple VMs can run on the same physical server so you can share the cost with other customers.​

    Imagine if your server or computer was an executable file on your computer

An **Amazon Machine Image (AMI)** is a predefined configuration for a Virtual Machine.  

    EC2 is considered the backbone of AWS because the majority of 
    AWS services are using EC2 as their underlying servers. eg. S3, RDS, DynamoDB, Lambdas  

EC2 is a highly configurable server where you can choose AMI that affects options such as:​

* The amount of CPUs​
* The amount of Memory (RAM)​
* The amount of Network Bandwidth​
* The Operation System (OS) eg. Windows 10, Ubuntu, Amazon Linux 2​
* Attach multiple virtual hard-drives for storage eg. Elastic Block Store (EBS)​

----

## Containers

    virtualizing an Operation System (OS) to run multiple workloads on a single OS instance. Containers are generally used in micro-service architecture (when you divide your application into smaller applications that talk to each other) 

**[Elastic Container Service (ECS)](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html)** - is a **container orchestration service** that support Docker containers. Launches a cluster of server(s) on EC2 instances with Docker installed. When you need Docker as a Service, or you need to run containers.​

**[Elastic Container Registry (ECR)](https://docs.aws.amazon.com/AmazonECR/latest/userguide/Registries.html)** - is **repository for container images**. In order to launch a containers you need an image.​ An image just means a saved copy. A repository just means a storage that has version control.​

**[ECS Fargate](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html)** - is a **serverless orchestration container service**. It is the same as ECS expect you pay-on-demand per running container (With ECS you have to keep a EC2 server running even if you have no containers running) AWS manages the underlying server, so you don’t have to scale or upgrade the EC2 server.

**[Elastic Kubernetes Service (EKS)](https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html)** - is a fully **managed Kubernetes service**. Kubernetes (K8) is an open-source orchestration software that was created by Google and is generally the standard for managing microservices. When you need to run Kubernetes as a Service.​

## Serverless

    when the underlying servers are managed by AWS. You don’t worry or configure servers. 

**[AWS Lambdais](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)** a **serverless functions service**. You can run code without provisioning or managing servers. You upload small pieces of code, choose much memory and how long function is allowed to run before timing out. You a charged based on the runtime of the serverless function rounded to the nearest 100ms.​

## Virtual Machines

    an emulation of a physical computer using software 

**[Amazon LightSail](https://aws.amazon.com/lightsail/)** - is the **managed virtual server service**. It is the “friendly” version of EC2 Virtual Machines

----

## High Performance Computing (HPC)

### [The Nitro System](https://aws.amazon.com/ec2/nitro/)

A combination of dedicated hardware and lightweight hypervisor enabling faster innovation and enhanced security. All new EC2 instance types use the Nitro System.​

* Nitro Cards — specialized cards for VPC, EBS and Instance Storage and controller card​
* Nitro Security Chips — Integrated into motherboard. Protects hardware resources.​
* Nitro Hypervisor — lightweight hypervisor Memory and CPU allocation Bare Metal-like performance​ 

### [Bare Metal Instance](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/instance-types.html)

You can launch EC2 instance that have no hypervisor so you can run workloads directly​

on the hardware for maximum performance and control. The M5 and R5 EC2 instances run are bare metal.​

* **Bottlerocket** is a Linux-based open-source operation system that is purpose-built by AWS for running containers on Virtual Machines or bare metal hosts 

[What is High Performance Computing (HPC)?](https://aws.amazon.com/hpc/)​

A cluster of hundreds of thousands of servers with fast connections between each of them with the purpose of boosting computing capacity. When you need a supercomputer to perform computational problems to large to fix on a standard computers or would take to long.

* **AWS ParallelCluster** is an AWS-supported open source cluster management tool that makes it easy for you to deploy and manage High Performance Computing (HPC) clusters on AWS. 

----

## What is Edge Computing?​

    When you push your computing workloads outside of your networks to run close to the destination location.​

    eg. Pushing computing to run on phones, IoT Devices, or external servers not within your cloud network.​

## What is Hybrid Computing?​

    When you’re able to run workloads on both your on-premise datacenter and AWS Virtual Private Cloud (VPC)

[AWS Outposts](https://aws.amazon.com/outposts/) - is physical rack of servers that you can put in your data center. AWS Outposts allows you to use AWS API and Services such as EC2 right in your datacenter.

[AWS Wavelength](https://aws.amazon.com/wavelength/) - AWS Wavelength allows you to build and launch your applications in a telecom datacenter. By doing this your applications with have ultra-low latency since they will be pushed over a the 5G network and be closest as possible to the end user.

[VMWare Cloud on AWS](https://docs.vmware.com/en/VMware-Cloud-on-AWS/index.html) - allows you to manage on-premise virtual machines using VMWare as EC2 instances.​ The data-center must being using VMWare for Virtualization.

[AWS Local Zones](https://aws.amazon.com/about-aws/global-infrastructure/localzones/) - are edge datacenters located outside of an AWS region so you can use AWS closer to end destination.​ When you need faster computing, storage and databases in populated areas that are outside of an AWS Region​

----

## Cost & Capacity Management

**Cost Management** - How do we save money?​

**Capacity Management** - How do we meet the demand of traffic and usages though adding or upgrading servers?

**[EC2 Spot Instances, Reserved Instanced and Savings Plan](https://aws.amazon.com/ec2/pricing/)​** - Ways to save on computing, by paying up in full or partially, by committing to a yearly contracts or by being flexible about availability and interruption to computing service.

**[AWS Batch](https://docs.aws.amazon.com/batch/latest/userguide/what-is-batch.html)** - plans, schedules, and executes your batch computing workloads across the full range of AWS compute services, can utilize Spot Instance to save money.​

**[AWS Compute Optimizer](https://aws.amazon.com/compute-optimizer/)** - Suggests how to reduce costs and improve performance by using machine learning to analyze you previous usage history

**[EC2 Autoscaling Groups (ASGs)​](https://docs.aws.amazon.com/autoscaling/ec2/userguide/AutoScalingGroup.html)** - Automatically adds or remove EC2 servers to meet the current demand of traffic. Will save you money and meet capacity since you only run the amount of servers you need.​

**[Elastic Load Balancer (ELB)](https://aws.amazon.com/elasticloadbalancing/)** - Distributes traffic to multiple instance, can re-route traffic from unhealthy instance to healthy instances.​ Can route traffic to EC2 instances running in different Availability Zones ​

**[Elastic Beanstalk (EB)](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/Welcome.html)** - is for easily deploying web-applications without developers having to worry about setting up and understanding the underlying AWS Services. Similar to Heroku. ​
