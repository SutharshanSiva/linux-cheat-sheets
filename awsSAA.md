[Back](README.md) to README.md

# AWS Certified Solutions Architect - Associate Level

####  Helpful Links

[https://aws.amazon.com/certification/certified-solutions-architect-associate/](https://aws.amazon.com/certification/certified-solutions-architect-associate/)

[https://aws.amazon.com/certification/certification-prep/](https://aws.amazon.com/certification/certification-prep/)

[https://aws.amazon.com/vpc/faqs/](https://aws.amazon.com/vpc/faqs/)

[https://www.certmetrics.com/amazon/](https://www.certmetrics.com/amazon/)

#### Read the following from AWS documentation: FAQ, What is, Getting started

| Compute | Network & Content Deliver | Management Tools |
| :---: | :---: | :---: |
| [x] EC2 | [] VPC | []CloudWatch |
| [x] EC2 Container Service | [] CloudFront | [] CloudFormation |
| [x] Elastic Beanstalk | [] Route 53 | |
| [x] Lamda | | |
| [ ] Batch | | |

| Storage | Security, Identity & Compliance | Messaging |
|:---:| :---: | :---: |
| [x] S3 | [] IAM | [] Simple Queue Service |
| [] EFS | | [] Simple Notification Service |
| [] EBS | | |
| [] Glacier | | |
| [] Storage Gateway | | |

| Database |
| :---: |
| [x] RDS |
| [x] DynamoDB |
| [] ElasticCache |
| [] Redshift |

###  EC2 notes  ###
Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. 

The use of a placement group is ideal _______
 - When your fleet of EC2 instances requires high network throughput and low latency within a single availability zone.


### S3 notes  ###
Amazon S3 is a repository for Internet data. Amazon S3 provides access to reliable, fast, and inexpensive data storage infrastructure. It is designed to make web-scale computing easy by enabling you to store and retrieve any amount of data, at any time, from within Amazon EC2 or anywhere on the web

Cross Origin Resource Sharing - Need to enable it on the resources bucket and state the URL fo the origin that will be calling the bucket.

[http://mybucketname.s3-website.eu-west-2.amazonaws.com](http://mybucketname.s3-website.eu-west-2.amazonaws.com)
[http://s3.eu-west-2.amazonaws.com/mybucketname](http://s3.eu-west-2.amazonaws.com/mybucketname)

 - Cross Region replication only replicates new files and versions.  If an existing file is updated the with versioning on it will replicate older versions of the file.
 - When deleting an object you can enable MFA Authentication - versioning enabled.
 - All regions provide read-after-write consistency for PUTS of new objects and eventual consistency for overwrite PUTS and DELETES
 - Default provision 100 buckets per AWS account

#### Encryption data in-transaction
 - CMK - 
 - Client-side master keys
 - SSL AWS encryption

#### Encryption data at requests
 - AES-256
 - x-amz-server-side-encryption request header to upload requests


### IAM notes  ###
AWS Identity and Access Management (IAM) enables you to securely control access to AWS services and resources for your users. Using IAM, you can create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources.
 - AWS account default limit of 20 EC2 instances.
 - Use an IAM role to manage temporary credentials for applications that run on an EC2 instance. When you use a role, you don''t have to distribute long-term credentials to an EC2 instance.


### DynamoDB
Your design team is about to implement an urgently needed collection and analysis solution. The data you will collect from an array of 50,000 anonymous data collectors will be summarized each day but rarely used again. The data will be pulled from collectors approximately once an hour. The Dev responsible for the DynamoDB design is concerned about how to design the Partition and Local keys to ensure efficient use of the DynamoDB tables. What advice would you provide.
 - Create a new table each day, and reconfigure the old table for infrequent use after the summation is complete.

You are working with the S3 API and receive an error message: 409 Conflict. What is the possible cause of this error?
 - Youre attempting to remove a bucket without emptying the contents of the bucket first.


### SWF Notes
In SWF, what does a "domain" refer to?
 - A collection of related workflows

### SQS Notes
What is long polling used for?


### Exam Sample
Amazon Glacier is designed for: (Choose 2 answers)
- A. active database storage.
- B. infrequently accessed data.
- C. data archives.
- D. frequently accessed data.
- E. cached session data.

Your web application front end consists of multiple EC2 instances behind an Elastic Load Balancer. You
configured ELB to perform health checks on these EC2 instances. If an instance fails to pass health
checks, which statement will be true?

- A. The instance is replaced automatically by the ELB.
- B. The instance gets terminated automatically by the ELB.
- C. The ELB stops sending traffic to the instance that failed its health check.
- D. The instance gets quarantined by the ELB for root cause analysis.

You are building a system to distribute confidential training videos to employees. Using CloudFront, what method could be used to serve content that is stored in S3, but not publically accessible from S3
directly?

- A. Create an Origin Access Identity (OAI) for CloudFront and grant access to the objects in your S3
bucket to that OAI.
- B. Add the CloudFront account security group “amazon-cf/amazon-cf-sg” to the appropriate S3 bucket
policy.
- C. Create an Identity and Access Management (IAM) User for CloudFront and grant access to the
objects in your S3 bucket to that IAM User.
- D. Create a S3 bucket policy that lists the CloudFront distribution ID as the Principal and the target
bucket as the Amazon Resource Name (ARN).

Which of the following will occur when an EC2 instance in a VPC (Virtual Private Cloud) with an
associated Elastic IP is stopped and started? (Choose 2 answers)

- A. The Elastic IP will be dissociated from the instance
- B. All data on instance-store devices will be lost
- C. All data on EBS (Elastic Block Store) devices will be lost
- D. The ENI (Elastic Network Interface) is detached
- E. The underlying host for the instance is changed

In the basic monitoring package for EC2, Amazon CloudWatch provides the following metrics:

- A. web server visible metrics such as number failed transaction requests
- B. operating system visible metrics such as memory utilization
- C. database visible metrics such as number of connections
- D. hypervisor visible metrics such as CPU utilization

Which is an operational process performed by AWS for data security?

- A. AES-256 encryption of data stored on any shared storage device
- B. Decommissioning of storage devices using industry-standard practices
- C. Background virus scans of EBS volumes and EBS snapshots
- D. Replication of data across multiple AWS Regions
- E. Secure wiping of EBS data when an EBS volume is unmounted

To protect S3 data from both accidental deletion and accidental overwriting, you should:

- A. enable S3 versioning on the bucket
- B. access S3 data using only signed URLs
- C. disable S3 delete using an IAM bucket policy
- D. enable S3 Reduced Redundancy Storage
- E. enable Multi-Factor Authentication (MFA) protected access

# ANSWERS
- B/C
- C
- A
- A/B
- D
- E
- A


#### Free services  
 - Amazon VPC, Autoscaling.  Cloud Formation, Not ELB.
 - Managed services: DynamoDB, CloudFormation, Redshift, kenesis
 - Serverless: Elastic Beanstalk, Lamda

### http codes
An HTTP 404 status code means communication with the service was successful, but the request received a "not found" response. MissingSecurityHeader is an error message received if the S3 API call is missing security API information which prevents the request from being executed successfully. 400 bad request would be the HTTP response code for MissingSecurityHeader.

- 2xx successful completion
- 3xx redirect
- 4xx client side
- 5xx server side
- 400	Bad Request Exception	No
- 403	Access Denied Exception	No
- 404	Not Found Exception	No
- 409	Conflict Exception	No
- 429	Limit Exceeded Exception	No
- 429	Too Many Requests Exception	Yes
- 502	Bad Gateway Exception, usually for an incompatible output returned from a Lambda proxy integration backend and occasionally for out-of-order invocations due to heavy loads.	No
- 503	Service Unavailable Exception	Yes
- 504	Endpoint Request Timed-out Exception	Yes

### ECS 
- S3 URLs pre-signed
- AWS regions

### SWF - Domain, workers, deciders - true
### SQS 

SQS messages can contain up to 256KB of data. This data can include any information needed. In order to work around the limit issue, the message can contain information on how to access the larger dataset from another service such as S3 or DynamoDB.

##### First AWS Service
- Long polling max timeout 20seconds
- 14 days max retention period
- default visibility timeout 30 second.
- Max visibility timeout 12hours
- ChangeMessageVisibility

### SDKs - perl not supported

### CloudFormation
There is no limit to the number of templates, however there is a limit of 200 stacks per AWS account.

What section of the CloudFormation would you edit in order to allow the user to specify the PEM key-name at start time?
 - Parameters

### Elastic Beanstalk
 - Apache Tomcat for Java applications
 - Apache HTTP Server for PHP applications
 - Apache HTTP Server for Python applications
 - Nginx or Apache HTTP Server for Node.js applications
 - Passenger or Puma for Ruby applications
 - Microsoft IIS 7.5, 8.0, and 8.5 for .NET applications
 - Java SE
 - Docker
 - Go
