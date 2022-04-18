## Defense in Depth

The 7 Layers of Security

### 1. Data

access to business and customer data, and encryption to protect data.

### 2. Application 

applications are secure and free of security vulnerabilities.

### 3. Compute

Access to virtual machines (ports, on-premise, cloud)

### 4. Network

limit communication between resources using segmentation and access controls.

### 5. Perimeter

distributed denial of service (DDoS) protection to filter large-scale attacks before they can cause a denial of service for users.

### 6. Identity and access

controlling access to infrastructure and change control.

### 7. Physical

limiting access to a data center to only authorized personnel.

----

## AWS Inspector

### What is Hardening?

The act of eliminating as many security risks as possible. Hardening is common for Virtual Machines where you run a collection of security checks known as a security benchmark

AWS Inspector runs a security benchmark against specific EC2 instances.

You can run a variety of security benchmarks.

Can perform both Network and Host Assessments

* Install the AWS agent on your EC2 instances.
* Run an assessment for your assessment target.
* Review your findings and remediate security issues. 

One very popular benchmark you can run is by CIS which has 699 checks!

----

## AWS Shield

AWS Shield is a managed DDoS (Distributed Denial of Service) protection service that safeguards applications running on AWS

When you route your traffic through Route53 or CloudFront you are using AWS Shield Standard

Protects you against Layer 3, 4, and 7 attacks

* 7 Application
* 4 Transport
* 3 Network 

---- 

## Amazon Guard Duty

### What is IDS/IPS?

Intrusion Detection System and Intrusion Protection System.

A device or software application that monitors a network or systems for malicious activity or policy violations.

Guard Duty is a threat detection service that continuously monitors for malicious, suspicious activity and unauthorized behavior. It uses Machine Learning to analyze the following AWS logs:

* CloudTrail Logs
* VPC Flow Logs
* DNS logs 

It will alert you of Findings which you can automate an incident response via CloudWatch Events or with 3rd Party Services

----

## AWS WAF

AWS Web Application Firewall (WAF) protect your web applications from common web exploits

Write your own rules to ALLOW or DENY traffic based on the contents of HTTP requests

Use a ruleset from a trusted AWS Security Partner in the AWS WAF Rules Marketplace

WAF can be attached to either CloudFront or an Application Load Balancer

Protect web applications from attacks covered in the OWASP Top 10 most dangerous attacks:

1. Injection
2. Broken Authentication
3. Sensitive data exposure
4. XML External Entities (XXE)
5. Broken Access control
6. Security misconfigurations
7. Cross-Site Scripting (XSS)
8. Insecure Deserialization
9. Using Components with known vulnerabilities
10. Insufficient logging and monitoring 

----

## AWS Key Management Service

AWS Key Management Service (KMS) is a managed service that makes it easy for you to create and control the encryption keys used to encrypt your data.

* KMS is a multi-tenant HSM (hardware security module)
* Many AWS services are integrated to use KMS to encrypt your data with a simple checkbox
* KMS uses Envelope Encryption. 

**Envelope Encryption**

When you encrypt your data, your data is protected, but you have to protect your encryption key.

When you encrypt your data key with a master key as an additional layer of security.

[KMS Master Key] encrypts → [Envelope Data Key] encrypts → [Data]

----

## CloudHSM

CloudHSM is a single-tenant HSM as a service that automates hardware provisioning, software patching, high availability, and backups.

AWS CloudHSM enables you to generate and use your encryption keys on FIPS 140-2 Level 3 validated hardware.

Built on Open HSM industry standards to integrate with:

* PKCS#11
* Java Cryptography Extensions (JCE)
* Microsoft CryptoNG (CNG) libraries 

You can also transfer your keys to other commercial HSM solutions to make it easy for you to migrate keys on or off of AWS.

Configure AWS KMS to use AWS CloudHSM cluster as a custom key store rather than the default KMS key store.