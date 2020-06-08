---
title: "AWS Security Specialty - Exam Preparation Notes"
image: 
  path:  /images/AWS-CSS.webp
  thumbnail: /images/AWS-CSS.webp

categories:
  - AWS 
tags:
  - AWS
  - CERTIFICATION
  - SECURITY
  - AWS-CLI 
--- 


Note: These are notes I took during the AWS Security Specialty exam study. Hope this will be useful to somebody. 

<https://www.linkedin.com/in/gvijai/> - My Linkedin profile:

Please send me a note of any other site / links that needs to be added to this page. 


AWS Security Spciality Exam Notes: 

## Online references that I used / Online Resources to be referred.

1. <https://tutorialsdojo.com/aws-cheat-sheets/> - Tutorials Dojo - for associate / professional exam preparation.   
2. <http://jayendrapatil.com/> - Jayendra Patil's blog for all AWS / GCP Exam preparation. 
3. <https://www.udemy.com/course/aws-certified-security-specialty/> - Zeal Vora's Security Specialty - Course  
4. <https://www.whizlabs.com/aws-certified-security-specialty/practice-test/> - whizlabs Security Specialty practice exam - useful for understanding areas you need to concentrate. 
5. <https://learn.cantrill.io/p/aws-certified-solutions-architect-professional> - Adrian Cantrill's new course talks about Network and Security topics which are part of AWS CA Professional. 
6. <https://reviewnprep.com> - reviewnprep.com site provides blogs, reviews and practice exams for free on AWS, AZURE, Oracle , etc. 

### Disclaimer: I am not associated with any of the above mentioned organization / companies and I do not any way getting any benefit from these sites.  

## Exam Guide

1. <https://d1.awsstatic.com/training-and-certification/docs-security-spec/AWS%20Certified%20Security%20Specialty_Exam%20Guide_v1.6_FINAL.pdf>
2. <https://d1.awsstatic.com/training-and-certification/docs-security-spec/AWS_Certified_Security_Specialty_Exam_Guide_v1.5.pdf>


## Exam readiness

1. <https://www.aws.training/Details/eLearning?id=34786> - Exam Readiness: AWS Certified Security - Specialty

## Learning path

1. <http://jayendrapatil.com/aws-certified-security-speciality-scs-c01-exam-learning-path/>

## LAB

1. <https://amazon-run.qwiklabs.com/> - free courses .

### white papers

1. <https://d1.awsstatic.com/whitepapers/AWS_CAF_Security_Perspective.pdf>
2. <https://d1.awsstatic.com/whitepapers/compliance/AWS_CIS_Foundations_Benchmark.pdf>  - AWS CIS Foundations Benchmark
3. <https://d1.awsstatic.com/whitepapers/compliance/AWS_Security_at_Scale_Logging_in_AWS_Whitepaper.pdf> - Security at Scale: Logging in AWS
4. <https://d0.awsstatic.com/whitepapers/compliance/AWS_Auditing_Security_Checklist.pdf> - Introduction to Auditing the Use of AWS
5. <https://d1.awsstatic.com/whitepapers/Security/Networking_Security_Whitepaper.pdf> - Overview of AWS Security - Network
6. <https://d0.awsstatic.com/whitepapers/KMS-Cryptographic-Details.pdf> - AWS KMS Cryptographic Details
7. <https://d1.awsstatic.com/whitepapers/aws_security_incident_response.pdf> - AWS Security Incident Response Guide
8. <https://d0.awsstatic.com/whitepapers/aws-kms-best-practices.pdf> - AWS Security Service Best Practices 
9. <https://d1.awsstatic.com/whitepapers/Security/DDoS_White_Paper.pdf> - AWS DDOS Whitepaper 


### Videos

1. <https://www.youtube.com/user/AmazonWebServices/search?query=encryption> - AWS Encryption Videos
2. <https://www.youtube.com/user/AmazonWebServices/search?query=incident+response> - AWS Incident Response Videos
3. <https://www.youtube.com/watch?v=plv7PQZICCM> - AWS re:Inforce 2019: How Encryption Works in AWS (FND310-R)



### Links

1. <https://aws.amazon.com/compliance/shared-responsibility-model/> 
2. <https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/?p=gi> 
3. <https://aws.amazon.com/about-aws/global-infrastructure/> 
4. <https://aws.amazon.com/compliance/data-center/data-centers/> 

1. https://aws.amazon.com/blogs/publicsector/building-a-cloud-specific-incident-response-plan/ - Building a Cloud-Specific Incident Response Plan

#### Compliance

1. <https://aws.amazon.com/compliance/programs/> - Compliance Program
2. <https://www.atlas.aws/> - Compliance Center
3. <https://aws.amazon.com/compliance/resources/ >- Compliance Best Practices and Workbooks
4. <https://d1.awsstatic.com/whitepapers/compliance/AWS_CIS_Foundations_Benchmark.pdf> - AWS CIS Foundations Benchmark

1. <https://aws.amazon.com/articles/tips-for-securing-your-ec2-instance/> - Securing Your EC2 Instance
2. <https://docs.aws.amazon.com/inspector/latest/userguide/inspector_rule-packages.html> - Amazon Inspector Assessments
3. <https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-best-practices.html> - AWS Systems Manager Use Cases





## Services :

1. https://aws.amazon.com/artifact/ - is a no-cost, self-service portal for access to the AWS security and compliance reports and select online agreements. Reports available include our Service Organization Control (SOC) reports, Payment Card Industry (PCI) reports, and certifications from accreditation bodies across geographies and compliance verticals.



## Security Of the cloud

### Data center security

### Compliance and Governance

### DDOS Protection

1. Amazon Route 53 is a highly available and scalable DNS service that can be used to direct traffic to your web application. It includes many advanced features like traffic flow, latency-based routing, weighted round-robin, Geo DNS, health checks, and monitoring. You can use these features to improve the performance of your web application and to avoid site outages. Route 53 is hosted at numerous AWS edge locations, creating a global surface area capable of absorbing large amounts of DDoS traffic.

2. Amazon CloudFront is a content delivery network (CDN) service that can be used to deliver data, including your entire website, to end users. CloudFront only accepts HTTPS and HTTP well-formed connections to prevent many common DDoS attacks. These capabilities can greatly improve your ability to continue serving traffic to end users during larger DDoS attacks.


3. AWS Shield is a managed DDoS protection service that safeguards web applications that run on AWS. AWS Shield provides always-on detection and automatic inline mitigations that minimize application downtime and latency.

#### Service  

1. AWS WAF - AWS Web Application Firewall (WAF) helps protect your web applications from common web exploits that could affect application availability, compromise security, or consume excessive resources. AWS WAF gives you control over which traffic to allow or block by defining customizable web security rules.



## Security in the cloud

### Links

1. https://docs.aws.amazon.com/general/latest/gr/rande.html#ct_region
2. https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/

### AWS IAM

#### Services
1. AWS Secrets Manager is designed to centrally manage secrets used to access resources on AWS, on-premises, and third-party services. Secrets can be database credentials, passwords, third-party API keys, and even arbitrary text. Secrets Manager enables you to replace hardcoded credentials in your code with an API call to Secrets Manager to retrieve the secret programmatically. Also, you can configure Secrets Manager to automatically rotate the secret for you according to a schedule that you specify.
2. AWS Single Sign-On (SSO) is a cloud SSO service that allows for the central management of SSO access to multiple AWS accounts and business applications. It enables users to sign in to a user portal with their existing corporate credentials and access all of their assigned accounts and applications from one place. AWS SSO includes built-in SAML integrations to many business applications. AWS SSO may be integrated with Microsoft Active Directory, which means your employees can sign in to your AWS SSO user portal using their corporate Active Directory credentials.

3. The AWS Security Token Service (STS) is a web service that enables you to request temporary, limited-privilege credentials for IAM users who are taking on a different role or for users who are being federated. A scenario in which someone, or something, needs access to your account to perform a specific task that is not done on a daily basis would be a great candidate for temporary credentials.

4. AWS Directory Service for Microsoft Active Directory, also known as AWS Managed Microsoft AD, enables your domain workloads and AWS resources to use managed Active Directory in the AWS Cloud. AWS Managed Microsoft AD is built on actual Microsoft Active Directory and does not require you to synchronize or replicate data from your existing Active Directory to the cloud.

5. AWS Organizations lets you centrally manage and enforce policies for multiple AWS accounts. This service allows grouping accounts into organizational units and use service control policies to centrally control AWS services across multiple AWS accounts. With Organizations, you can also automate the creation of new accounts through APIs and simplify billing by allowing you to set up a single payment method for all the accounts in your organization through consolidated billing. Organizations is available to all AWS customers at no additional charge.

6. Amazon Cognito lets you add user sign-up, sign-in, and access controls to your web and mobile apps. You can define roles and map users to different roles so your app can access only the resources that are authorized for each user. User sign in can be done either by a third-party identity provider, or directly via Amazon Cognito.

### Detective Controls

### Infrastucture Protection


#### Services

1. AWS Firewall Manager is a security management service that allows you to centrally configure and manage AWS WAF rules across your accounts and applications. Firewall Manager is able to bring new applications and resources into compliance with a common set of security rules from the start.
2. AWS Direct Connect is a cloud service solution that is used to establish a dedicated and secure network connection from your premises to AWS. Using AWS Direct Connect, you can establish private connectivity between AWS and your data center, office, or colocation environment. In many cases, this can reduce your network costs, increase bandwidth throughput, and provide a more consistent network experience than internet-based connections.
3. AWS CloudFormation automates and simplifies the task of repeatedly creating and deploying AWS resources in a consistent manner.  With AWS CloudFormation, you can ensure that all of your security and compliance controls are deployed along with your new environment.

4. Amazon Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS. It assesses applications for vulnerabilities or deviations from best practices. After performing an assessment, Amazon Inspector produces a detailed list of security findings prioritized by level of severity.


### Data Protection


#### Services

1. AWS CloudHSM provides hardware security modules (HSM) in the AWS Cloud. An HSM is a computing device that processes cryptographic operations and provides secure storage for cryptographic keys. CloudHSM allows you to generate, store, import, export, and manage cryptographic keys, including symmetric keys and asymmetric key pairs.
2. Amazon S3 Glacier is a storage service optimized for infrequently used data, also called cold data. This service provides durable and extremely low-cost storage with security features for data archiving and backup. Amazon S3 Glacier stores data as archives within vaults.  You can enforce compliance controls for individual Amazon S3 Glacier vaults with a vault lock policy.
3. AWS Certificate Manager (ACM) handles the complexity of creating and managing public SSL/TLS certificates for your AWS based websites and applications. ACM can also be used to issue private SSL/TLS X.509 certificates that identify users, computers, applications, services, servers, and other devices internally.
4. Amazon Macie uses machine learning to automatically discover, classify, and protect sensitive data in AWS. Macie recognizes sensitive data such as personally identifiable information (PII) or intellectual property. It provides you with dashboards and alerts that give visibility into how this data is being accessed or moved.

5. AWS Key Management Service (AWS KMS) is a managed service that allows you to create and control the keys used in data encryption. If you want a managed service for creating and controlling encryption keys, but do not want or need to operate your own hardware security module (HSM), consider using AWS KMS. You can use the key management and cryptographic features directly in your applications or through AWS services that are integrated with AWS KMS, including AWS CloudTrail, which helps meet your auditing, regulatory, and compliance needs.


### Incident Response


#### Services

1. AWS Step Functions lets you coordinate multiple AWS services into serverless workflows so you can build and update apps quickly. Workflows are made up of a series of steps, with the output of one step acting as the input into the next. Step Functions can be used to design and run workflows that stitch together services such as AWS Lambda and AWS CloudFormation to respond to an incident in the cloud.


### AWS Well-Architected Tool


1. https://docs.aws.amazon.com/wellarchitected/latest/userguide/wellarchitected-ug.pdf - AWS Well-Architected Tool User Guide


----


Zeal Vora

170 Min . 65 Questions

1. Intro to Domain1

## Incident Response

--- Theory

Case Study : Hacked Server

AWS Abuse Reports

### AWS GuardDuty


### Incident Response - uae cases

1. Exposed aws access and secret keys
2. compromised ec2 instances.


#### aws keys
make inactive -- keys
aws sts get-session-token - for temp key
attach explicit deny policy

#### ec2 compromised
Lock the instance down.
only access to ec2 instance should be for forensic purposes. - automation is a key

EBS Snapshot and Memory dump
Perform Forensics and Terminate the Instances.
RCA release. - terminate instance.


### Incident Response in cloud

### Pentest

https://aws.amazon.com/security/penetration-testing/

### inspector
limited OS support - https://docs.aws.amazon.com/inspector/latest/userguide/inspector_supported_os_regions.html





--------

AWS Encryption

https://www.youtube.com/watch?v=gTZgxsCTfbk


why encrypt

- compliance
- best practice in secuirty
- protect myself from cloud provider and other customer

## minimize unauthorized physical access to data in the cloud.

### data in transport
- on the wire
- on the disk on a truck

### data at rest


### data in use
- Datacenter physical security

## Data in Transport Security

## VPN - L4
### AWS Managed VPN
### AWS VPN Cloud Hub
### 3rd Party Software VPN Applianc


using TLS for data Confidentiality and integrity

### AWS Certificate Manager

s2n

## Data at Rest encryption primer
### Clientool-side encryption
encrypt before submitting to AWS .



###Server-side

encrypt data after received by service
integrate with AWS KMS



------

Exam readiness

https://www.aws.training/Details/eLearning?id=34786



1. self paced Labs - https://amazon.qwiklabs.com/catalog?locale=en
2. Sample question
3. aws security resources
4. security blogs


## 1. Incident Response

- Isolate

incident indicator
- Logs and monitor
- billing activity
- threat intelligene
- aws support
- public response

###  compromised incident

- remove from ASG, ISOLate by SG , using forensic

### Exposed Access key

- disable - invalidate credentials
- REvoke Privilege Access - DENY IAM policy DNY
- track user associated with access keys.
- verify integrity , cloud trail , config

#### AWS Config Rules
- AWS Managed Rules
- require minimal to no configuration
Custom Rules
- Use AWS Lamda function
-

#### AWS Guard Duty
- collects data from CT,DNS Logs, VPC Flow logs
- continously monitors for mailicious or unauthorized behavious to help protect your AWS accounts workloads
- Detailed Security alert to


## 2. Logging and Monitoring
1. Design and implement security monitoring and alerting.
2. Troubleshoot security monitoring and alerting.
3. Design and implement a logging solution.
4. Troubleshoot logging solutions.


- AWS Cloudwatch
- AWS Config
- AWS CloudTrail
- AWS Inspector - CVE, CIS ,Security Best Practies.
- AWS Shared REsponsiblity - in

- Athena S3 search  using SQL


## Infrastucture Security

1. Design edge security on AWS.
2. Design and implement a secure network infrastructure
3. Troubleshoot a secure network infrastructure.
4. Design and implement host-based security.

- AWS Route 53 - HA 100%.
- AWS WAF - protection web attack.
- AWS Cloudfront -
- AWS Shield and advanced

#### DDOS Mitigation.
 ELB, Cloudwatch , EC2 ASG, AWS Shiled,Route 53,AWS WAF, CloudFront

#### Design and implement a secure network infrastructure
1. Network ACL VS SG
2. Network - stateless
2. SG - Stateful , No DENY Rule.

#### Design and implement host-based security.

## Identity and Access Management

1. Design and implement a scalable authorization and authentication system to access AWS resources.
2. Troubleshoot an authorization and authentication system to access AWS resources.

- AWS Managed Policy
- Customer Managed Policy
- Inline Policy

#### IAM Permission
- Explocitly denied - denied then
- EAR - Effect,Action,Resource then Condition,Principle optional

##### root account
- no root account for day to day.
- strong password
- enable MFA

#### AWS Directory Service
- AWS Managed MS AD - in cloud
- AD Connector - for on-premises users to need access AWS services via AD
- simple AD - low-scale , low-cost basic AD Capability

## Data Protection 22%

- Encryption

KMS and Cloud HSM

#### KMS
- Only Symmetric

- Policy based and Grants based

#### Data at Transit
- TLS
- X.509 used within PKI
#### AWS Certifcate Manager ---
- Single interface to manage both public and private certificate
- make easy to deploy certificates
- protects and store private certificate
- automatic renewal - minimize downtime.

#### Strategies for data at rest
- information disclosure
- Data Integrity Compromise
- Accidental Deletion
- system /HW/SW availability


#### CSE vs SSE

#### CSE
- encrypt before sending to AWS
- Data stored in encrypted state
- user managed

#### SSE
- AWS Encrypts data on your behalf after it has been received.
- Transparent to end user
- AWS rotates master key on regular basis.
-

### S3 data access protection

- object ACL
- bucket ACL
- bucket policies
- IAM user policies

### RDS data protection
- encryption must be enabled at creation of DB.
- TDE optional for some DB.

### Dynamodb

### Glacier

- Vault Lock
-- Time-based retention
-- MFA auth
-- immutable
-- WORM

### AWS Secret Manager
- Rotate secrets safely
- manage access
