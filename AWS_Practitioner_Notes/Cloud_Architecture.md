## Cloud Architecture Terminologies

### What is a Solutions Architect?

    A role in a technical organization that architects a technical solution using multiple systems via researching, documentation, experimentation.

----

### What is a Cloud Architect?

    A solutions architect that is focused solely on architecting technical solutions using cloud services.

A cloud architect needs to understand the following terms and factor them into their design architecture based on the business requirements.

* **Availability** - Your ability to ensure service remains available e.g. Highly Available (HA)
* **Scalability** - Your ability to grow rapidly or unimpeded
* **Elasticity** - Your ability to shrink and grow to meet the demand
* **Fault Tolerance** - Your ability to prevent a failure
* **Disaster Recovery** - Your ability to recover from a failure e.g. High Durable (DR) 

A Solutions Architect needs to always consider the following business factors:

* (Security) How secure is this solution?
* (Cost) How much is this going to cost? 

----

## High Availability  

### What is High Availability (HA)?

    Your ability for your service to remain available by ensuring there is no single point of failure and/or ensure a certain level of performance
    
### How can you achieve High Availability?

    Running your workload across multiple Availability Zones ensures that if 1 or 2 AZs become unavailable your service/applications remain available.

### How can High Availability be implemented on AWS?

    Using Elastic Load Balancer would assist in implementing High Availability

### Elastic Load Balancer

A load balancer allows you to evenly distribute traffic to multiple servers in one or more data center. If a data center or server becomes unavailable (unhealthy) the load balancer will route the traffic to only available data centers with servers.​

----

## High Scalability

### What is High Scalability?

    Your ability to increase your capacity based on the increasing demand of traffic, memory and computing power

### How is High Scalability defined?

* Vertical Scaling is known as Scaling Up (When Upgrade to a bigger server)
* Horizontal Scaling is known as Scaling Out (When Add more servers of the same size) 

----

## High Elasticity

### What is High Elasticity?

    Your ability to automatically increase or decrease your capacity based on the current demand of traffic, memory and computing power

### How is Elasticity achieved?

    Elasticity relies on Horizontal Scaling. Vertical Scaling is generally hard for traditional architecture so you’ll usually only see horizontal scaling described with Elasticity.

**Scaling Out** — Add more servers of the same size

**Scaling In** — Removing more servers of the same size

### How can Elasticity be implemented in AWS?

    Auto Scaling Groups (ASG) - are an AWS feature that will automatically add or remove servers based on scaling rules you define.

----

## High Durability

    Your ability to recover from a disaster and to prevent the loss of data solutions that recover from a disaster is known as Disaster Recovery (DR)

----

## Disaster Recovery Options

There are multiple options for recovery that trade cost vs time to recover.

### Backup & Restore

RPO/RTO (Hours)

You back up your data and restore it to new infrastructure

* Lower priority use cases
* Restore data after the event
* Deploy resources after the event
* Cost $ 

### Pilot Light

RPO/RTO (10 mins)

Data is replicated to another region with minimal services running

* Less stringent RTO & RPO
* Core Services
* Start & scale resources after the event
* Cost $$ 

### Warm Standby

RPO/RTO (Minutes)

Scaled-down copy of your infrastructure running ready to scale up

* Business Critical Services
* Scale resources after the event
* Cost $$$ 

### Multi-site Active/active

RPO/RTO (Real-time)

Scaled up copy of your infrastructure in another region

* Zero downtime
* Near-zero loss
* Cost $$$$ 

