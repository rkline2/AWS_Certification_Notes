## Logging Services

Amazon Web Services (AWS) provides service-specific operational metrics and log files to give customers insight into how the service is operating.

### CloudTrail

[CloudTrail](https://aws.amazon.com/cloudtrail/?nc2=type_a) - logs all API calls(SDK, CLI) between various AWS services

Questions that CloudTrail can answer:

*Who create this bucket?* - detect developer mis-configuration

*Who spun up that expensive EC2 instance?* - Detect malicious actors

*Who launched this SageMaker notebook?* - Automate responses

### CloudWatch

[CloudWatch](https://aws.amazon.com/es/cloudwatch/) - is a collection of multiple services

* CloudWatch Logs : Performance data about AWS Services eg. CPU Utilization, Memory, Network in Application Logs eg. Rails, Nginx Lambda Logs

* CloudWatch Metrics: Represents a time-ordered set of data points. A variable to monitor

* CloudWatch Events: trigger an event based on a condition eg. every hour take a snapshot of the server

* CloudWatch Alarms: triggers notifications based on metrics

* CloudWatch Dashboard: create visualizations based on metrics

### X-Ray

[AWS X-Ray](https://docs.aws.amazon.com/xray/latest/devguide/aws-xray.html) is a distributed tracing system. You can use it to pinpoint issues with your microservices. See how data moves from one app to another, how long it took to move, and if it failed to move forward.

----

## AWS CloudTrail

AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account.

AWS CloudTrail is used to monitor API calls and Actions made on an AWS account.

Easily identify which users and accounts made the call to AWS eg.

* Where — Source IP Address
* When — EventTime
* Who — User, UserAgent
* What — Region, Resource, Action 

CloudTrail is already logging by default and will collect logs for the last 90 days via Event History

If you need more than 90 days you need to create a Trail

Trails are output to S3 and do not have GUI like Event History. To analyze a Trail you’d have to use Amazon Athena.
