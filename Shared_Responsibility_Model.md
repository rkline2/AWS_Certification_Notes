## Shared Responsibility Model

**The Shared Responsibility Model** is a **cloud security framework** that defines the security obligations of the customer versa for the Cloud Service Provider (CSP) e.g. AWS.

Each CSP has its own variant of the Shared Responsibility Model but they are all generally the same.

### AWS Shared Responsibility Model

    The type of cloud deployment model and/or the scope of the cloud service category can result in specialized Shared Responsibility Models.

### Reference

[Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/)

----

## AWS Shared Responsibility Model

Customers are responsible for Security **in** the cloud

IN:

    * Data
    * Configuration

AWS is responsible for Security **of** the cloud

OF: 

    * Hardware 
    * Operation of Managed Services
    * Global Infrastructure

----

## Shared Responsibility Model - Compute

Let us take a look at compute as a comparison example of the Shared Responsibility Model

### **Infrastructure as a Service (IaaS)**

**Bare Metal** (EC2 Bare Metal Instance)

* Customer:
    * The Host OS Configuration
    * Hypervisor 

* AWS
    * Physical machine 

**Virtual Machine** (Elastic Cloud Compute (EC2))

* Customer:
    * The Guest OS Configuration
    * Container Runtime 

* AWS
    * Hypervisor, Physical machine 

**Containers** (AWS Elastic Container Service(ECS))

* Customer:
    * Configuration of containers
    * Deployment of Containers
    * Storage of containers 

* AWS
    * The OS, The Hypervisor, Container Runtime 


--################--

### **Platform as a Service (PaaS)**

Managed Platform (AWS Elastic Beanstalk)

* Customer:
    * Uploading your code
    * Some configuration of environment
    * Deployment strategies
    * Configuration of associated services 

* AWS
    * Servers, OS, Networking, Storage, Security 

--################--

### **Software as a Service (SaaS)**

Content Collaboration (Amazon WorkDocs)

* Customer:
    * Contents of documents
    * Management of files
    * Configuration of sharing access controls 

* AWS
    * Servers, OS, Networking, Storage, Security 

--################--

### **Function as a Service (FaaS)**

Functions
* AWS Lambda 

Customer:
* Upload your code 

AWS
* Deployment, Container Runtime, Networking, Storage, Security, Physical Machine, (basically everything) 

----

Shared Responsibility Model - Architecture

**Less Responsibility ↑**

Amplify Serverless Framework

Lambda Serverless Architecture

Fargate Serverless Containers

ECS/EKS Containers

Elastic Beanstalk  Platform as a Service 

EC2 Infrastructure as a Service

**More Responsibility ↓**

--################--

Serverless / Functions

    No more servers, just worry about data and code

Microservices / Containers

    Mix and match languages, better utilization of resources

Traditional / VMs

    Global workforce is most familiar with this kind of architecture and lots of documentation, frameworks, and support.
