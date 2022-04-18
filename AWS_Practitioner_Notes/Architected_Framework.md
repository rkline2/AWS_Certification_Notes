## AWS Well-Architected Framework

The AWS Well-Architected Framework is a Whitepaper created by AWS to help customers build using best practices defined by AWS.

The framework is divided into 6 sections called pillars which address different aspects of "lenses" that can be applied to a cloud workload.


### AWS Well-Architected Framework

* General Definitions
* General Design Principles
* The Review Process 

If the Foundation is Not Solid Structural Problems will Arise

### 6 Pillars

* Operational Excellence    - Run and monitor systems
* Security                  - Protect data and systems, mitigate risk
* Reliability               - Mitigate and recover from disruptions
* Performance Efficiency    - Use computing resources effectively
* Cost Optimization         - Get the lowest price
* [New] Sustainability      - Use environmental best practices

### General Definitions

* Component               - Code, Configuration, and AWS Resource against a requirement
* Workload                - A set of components that work together to deliver business value
* Milestones              - Key changes of your architecture through product life cycle
* Architecture            - How components work together in a workload
* Technology Portfolio    - A collection of workloads required for the business to operate

----

## AWS Well-Architected – On Architecture

The AWS Well-Architected Framework is designed around a different kind of team structure.

Enterprises generally have centralized teams with specific roles whereas AWS has distributed teams with flexible roles.

Distributed teams can come with new risks, AWS mitigates these with Practices, Mechanisms, and Leadership Principles

### On-Premise Enterprise

**Centralized team** consisting of:

* Technical Architect (infrastructure)
* Solution Architect (software)
* Data Architect
* Networking Architect
* Security Architect 

VS

### Amazon Web Services

**Distributed teams** consisting of:

* Practices
    * Team Experts (Raise the Bar) 
* Mechanisms
    * Automated Checks for Standards 
* *Amazon Leadership Principle 

Supported by a virtual community of SMEs, Principle Engineers

----

## AWS Well-Architected – General Design Principles

### Stop guessing your capacity needs

    eg. Cloud computing you use as little or much-based on demand.

### Test systems at production scale

    eg.  Clone production env to testing, Teardown testing not in use to save money.

### Automate to make architectural experimentation easier

    eg. Using CloudFormation with ChangeSets, StackUpdate, and Drift Detection

### Allow for evolutionary architectures

    eg. CI/CD, rapid or nightly releases, Lambdas deprecating run-times forcing you to evolve

### Drive architectures using data

    eg. CloudWatch, Cloud Trail automatically turned on collecting data

### Improve through game days

    eg. simulate traffic on production or purposely kill EC2 instances to see test recovery 

----

## Operational Excellence Design Principles

### Perform operations as code

    Apply the same engineering discipline you would to application code to your cloud infrastructure. By treating your operations as code you can limit human error and enable consistent responses to events.

    eg. Infrastructure as Code

### Make frequent, small, reversible changes

    Design workloads to allow components to be updated regularly.

    eg. rollbacks, incremental changes, Blue/Green, CI/CD

### Refine operations procedures frequently

    Look for continuous opportunities to improve your operations

    eg. Use game days to simulate traffic or event failure on your production workloads

### Anticipate failure

    Perform post-mortems on system failures to better improve, write test code, kill production serves to test recovery

### Learn from all operational failures

    Share lessons learned in a knowledge base for operational events and failures across your entire organization

----

## Security Design Principles

### Implement a strong identity foundation

    Implement the Principle of Least Privilege (PoLP). Use Centralized identity. Avoid Long-lived credentials

### Enable traceability

    Monitor alert and audit actions and changes to your environment in real-time Integrate log and metric collection and automate investigation and remediation

### Apply security at all layers

    Take Defense-in-depth approach with multiple security controls for everything eg. Edge Network, VPC, Load Balancing Instances, OS, Application Code

### Automate security best practices

### Protect data in transit and at rest

### Keep people away from data

### Prepare for security events

    Incident management systems and investigation policy and processes. Tools to detect, investigate and recover from incidences 

----

## Reliability Design Principles

### Automatically recover from failure

    Monitor Key Performance Indicators (KPIs) and trigger automation when a threshold is breached.

### Test recovery procedures

    Test how your workload fails, and you validate your recovery procedures. You can use automation to simulate different failures or to recreate scenarios that led to failures before.

### Scale horizontally to increase aggregate system availability

    Replace one large resource with multiple small resources to reduce the impact of a single failure on the overall workload. Distribute requests across multiple, smaller resources to ensure that they don’t share a common point of failure.

### Stop guessing capacity

    In on-premise it takes a lot of guesswork to determine the elasticity of your workload demands. With Cloud, you don’t need to guess how much you need because you can request the right size of resources on-demand.

### Manage change in automation

    Making changes via Infrastructure as Code will allow for a formal process to track and review infrastructure

----

## Performance Efficiency Design Principles

### Democratize advanced technologies:

    Focus on product development rather than procurement, provisioning, and management of services. Take advantage of advanced technology specialized and optimized for your use-case with on-demand cloud services.

### Go global in minutes

    Deploying your workload in multiple AWS Regions around the world allows you to provide lower latency and a better experience for your customers at minimal cost.

### Use serverless architectures:

    Serverless architectures remove the need for you to run and maintain physical servers for traditional compute activities. Removes the operational burden of managing physical servers, and can lower transactional costs because managed services operate at cloud scale.

### Experiment more often:

    With virtual and automatable resources, you can quickly carry out comparative testing using different types of instances, storage, or configurations.

### Consider mechanical sympathy

    Understand how cloud services are consumed and always use the technology approach that aligns best with your workload goals. For example, consider data access patterns when you select database or storage approaches.

----

## Cost Optimization Design Principles

### Implement Cloud Financial Management:

    Dedicate time and resources to build capability Cloud Financial Management and Cost Optimization tooling.

### Adopt a consumption model

    Pay only for the computing resources that you require and increase or decrease usage depending on business requirements

### Measure overall efficiency

    Measure the business output of the workload and the costs associated with delivering it. Use this measure to know the gains you make from increasing output and reducing costs.

### Stop spending money on undifferentiated heavy lifting

    AWS does the heavy lifting of data center operations like racking, stacking, and powering servers. It also removes the operational burden of managing operating systems and applications with managed services. This allows you to focus on your customers and business projects rather than on IT infrastructure.

### Analyze and attribute expenditure

    The cloud makes it easier to accurately identify the usage and cost of systems, which then allows transparent attribution of IT costs to individual workload owners. This helps measure return on investment (ROI) and gives workload owners an opportunity to optimize their resources and reduce costs.