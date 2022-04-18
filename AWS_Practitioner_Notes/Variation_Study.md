## SNS vs SQS

The Both Connect Apps via Messages

### Simple Notifications Service

Pass Along Messages eg. PubSub

Send notifications to subscribers of topics via multiple protocols. eg, HTTP, Email, SQS, SMS

SNS is generally used for sending plain text emails which are triggered via other AWS Services. The best example of this is billing alarms.

Can retry sending in case of failure for HTTPS

Really good for webhooks, simple internal emails, triggering Lambda functions

### Simple Queue Service

Queue Up Messages, Guaranteed Delivery

Places messages into a queue. Applications pull queue using AWS SDK

* Can retain a message for up to 14 days
* Can send them in sequential order or in parallel
* Can ensure only one message is sent
* Can ensure messages are delivered at least once 

Really good for delayed tasks, queueing up emails

----

## SNS vs SES vs PinPoint vs Workmail

They All Send Emails

### Simple Notifications Service

Practical and Internal Emails

Send notifications to subscribers of topics via multiple protocols. eg, HTTP, Email, SQS, SMS

SNS is generally used for sending plain text emails which are triggered via other AWS Services. The best example of this is billing alarms.

Most exam questions are going to be talking about SNS because lots of services can trigger SNS for notifications.

You Need to Know what are Topics and Subscriptions regarding SNS

### Simple Email Service

Transactional Emails

Emails that should be triggered based on in-app actions: Signup, Reset Password, Invoices…

* A cloud-based email service. eg. SendGrid
* SES sends HTML emails, SNS cannot.
* SES can receive inbound emails
* SES can create Email Templates
* Custom domain name email
* Monitor your email reputation 

### Amazon PinPoint

Promotional Emails

Emails for marketing

* Create email campaigns
* Segment your contacts
* Create customer journeys via emails
* A/B emailing testing 

### Amazon Workmail

Email Web Client

Similar to Gmail and Outlook. Create company emails, read, write and send emails from a Web Client within AWS Management Console

----

## Amazon Inspector vs AWS Trusted Advisor

Both are security tools and they both perform audits

### Amazon Inspector

Audits a single EC2 instance that you’ve selected

Generates a report from a long list of security checks i.e 699 checks.

### Trusted Advisor

Trusted Advisor doesn’t generate out a PDF report.

Gives you a holistic view of recommendations across multiple services and best practices

eg. You have open ports on these security groups

You should enable MFA on your root account when using Trusted advisor.

----

## Elastic Transcoder vs MediaConvert

Both services transcode videos

### Elastic Transcoder

The Old Way

Elastic Transcoder was the original transcoding service. It may have programmatic APIs or workflows not available in MediaConvert.

It exists due to legacy customers still using the platform

* Transcodes videos to streaming formats 

### AWS Elemental MediaConvert

The New Way

MediaConvert is a more robust transcoding service that can perform various operations during transcoding.

* Transcodes videos to streaming formats
* Overlays images
* Insert videos clips
* Extracts captions data
* Robust UI 

----

## AWS Artifact vs Amazon Inspector

Both Artifact and Inspector compile out PDFs

### AWS Artifact

Why should an enterprise trust AWS?

Generates a security report that’s based on global compliance frameworks such as:

* Service Organization Control (SOC)
* Payment Card Industry (PCI) 

### Amazon Inspector

How do we know this EC2 instance is Secure? Prove It?

Runs a script that analyzes your EC2 instance, then generates a PDF report telling you which security checks passed.

Audit tool for the security of EC2 instances

----
## ELB vs ALB vs NLB vs GWLB vs CLB

Elastic Load Balancer (ELB) has 4 different types of possible load balancers.

### Application Load Balancer (ALB)

Layer 7 - HTTP/S
Routing Rules

* create rules to change routing based on information found in an HTTP/S request 

Can attach an AWS WAF

### Network Load Balancer (NLB)

Layer 3 and 4 – TCP and UDP

Where extreme performance is required for TCP and TLS traffic

Capable of handling millions of requests per second while maintaining ultra-low latencies

Optimized for sudden and volatile traffic patterns while using a single static IP address per Availability Zone

### Gateway Load Balancer (GWLB)

When you need to deploy a fleet of third-party virtual appliances that support GENEVE

### Classic Load Balancer (CLB)

Layer 3,4 and 7

Intended for applications that were built within the EC2-Classic network

Doesn’t use Target Groups

Retires on Aug 15, 2022
