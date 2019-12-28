---
title: "AWS Advanced Networking Specialty - Exam Preparation Notes"
image: 
  path:  /images/AWS-ANS.png
  thumbnail: /images/AWS-ANS.png

categories:
  - AWS 
tags:
  - AWS
  - CERTIFICATION
  - SECURITY
  - NETWORKING
--- 

# AWS Advanced Networking - Notes 
### Notes taken during the preparation for the exam.
# Exam guide 

1. <https://d1.awsstatic.com/training-and-certification/docs-advnetworking-spec/AWS%20Certified%20Advanced%20Networking%20-%20Speciality_Exam_Guide_v1.2_FINAL.pdf> - AWS Certified Advanced Networking –  Specialty (ANS-C00) Exam Guide 


# Exam Rediness free digital training 
**This one is the must for passing the exam. Most of the questions are based on the information discussed in the readiness exam course. If you have completed CSA-PRO you can compete the course and read more about Direct Connect and AWS Connectivity options and sit for the exam.**

1. <https://www.aws.training/Details/Curriculum?id=21330> - Exam Readiness: AWS Certified Advanced Networking - Specialty (Digital)



---

## Practice Exam 

1. <https://s3-us-west-2.amazonaws.com/us-west-2-tcdev/courses/ILT-DD-300-CRNETW/v1.0.0/AWSCertified-AdvancedNetworking-PracticeExam.pdf> 


## Links 


1. <https://aws.amazon.com/answers/networking/aws-multiple-data-center-ha-network-connectivity/> - **Multiple Data Center HA Network Connectivity **

2. <https://aws-de-media.s3.amazonaws.com/images/AWS_Summit_2018/June7/Coral/AWS%20Direct%20Connect%20Deep%20Dive.pdf>. - **AWS Direct Connect Deep Dive ** 

3. <https://docs.aws.amazon.com/directconnect/latest/UserGuide/getting_started.html#RedundantConnections> - **AWS DX Redundant Connection **

4. <https://aws.amazon.com/directconnect/resiliency-recommendation/> - ** dx resiliency **

5. <https://aws.amazon.com/blogs/aws/new-aws-direct-connect-gateway-inter-region-vpc-access/> - 

## Courses that I took. 

1. <https://www.udemy.com/course/aws-certified-advanced-networking-specialty/> - by Zeal Vora 
2. <https://www.udemy.com/course/awsnetworking/> - by Rick Crisci 

 ---


Domain 1:  Design and implement hybrid IT network architectures at scale 
1.1 Implement connectivity for hybrid IT
1.2 Given a scenario, derive an appropriate hybrid IT architecture connectivity solution
1.3 Explain the process to extend connectivity using AWS Direct Connect
1.4 Evaluate design alternatives that leverage AWS Direct Connect
1.5 Define routing policies for hybrid IT architectures


Module 2 

## Design and Implement Hybrid IT Architecture 

Connectivity Options 

1. VPN 
 	- AWS Managed VPN 
 	- Software VPN (Amazon EC2)
2. AWS Direct Connect 
	 - Private Connection 
	 - Separate from the internet 
	 - Consistent network experience 
	 - Connect through many locations globally 
	 - Sub-1 Gbps, 1Gbps,10 Gbps 
--- 
### VPN 

1. Site-to-Site VPN 
2. Client-to-Site VPN 
---
### VGW - ipsec only
- only one per VPC 
- ASN(BYO-ASN) 
- detach and attach to another VPC. 
- Two Endpoints ( Cross - AZ's) 
- facilitate two tunnels 
- Preshared Key for each tunnel
- AS Path or 
- Set Metric or AS long path for patch selection. 
- CloudHub 
- VGW , will not initiate IPSEC Negotiation. 
- DPD - 10 sec sends DPD "R-U-THERE" will take down tunnel. ( three successive DPD) 

#### What can access via VPN ? 
- Any AWS resource with Private IP (with Exceptions)
- Amazon EC2, RDS, RedShofts,AWS Lamda 

#### What can't access via VPN?
- NLB, EFS
- VPC Endpoints (Interface or Gateway Endpoints)
- Private Link Endpoints 
- VPC DNS IP
- AWS Public IP Range 

#### VPN Monitoring 
- CloudWatch - TunnelState,TunnelDatain,TunnelDataOut
- 1.25 Gbps Max 
---	

### AWS EC2 - your own (ipsec or SSL) 
- Self-managed endpoint 
- supports BYOY ( Market Place)
- In-line Gateway (Single point for all traffic)
- Self Managed HA and Scalability 
- Max 2 to 2.5 Gbps 

#### What Can Access ? 
- Any AWS resource with Private IP (with Exceptions)
- Amazon EC2, RDS, RedShofts,AWS Lamda 
if EC2 instance can NAT all ingress 
- NLB , EFS, VPC Endpoints  can be accessible . 

#### Scalability 
- Horizontal Scaling EC2 VPN 

--- 

### Client-to-Site 
- VGW doesn't support Client-to-site VPN 
- use Thirdparty Market Place 

--- 
## AWS Direct Connect 

- Establish private dedicated connectivity. 
- Consistent Connection , network experience. 

--- 

Module 3 

##Configure Networking Integration with Application Server

1. Route 53 
2. ELB 
3. Amazon Cloudfront 
4. Lamda@Edge 

## Route 53 
- Highly available and scalable DNS 
- Domain Registration 
- private hosted zone and public 

- Health check webserver/ip - http/https/tcp/string matching 
- status of cloudwatch alarm 
- status of other health checks 

### Route 53 Traffic Policy 

- Simple 
- Failover ( using health check) 
- weighted ( 95% and 5% , blue green )
- combined policy 
- geo-fencing - geolocation 
- Latency 
- geoproximity 
- Multi value 

### Route 53 in VPC and Hybrid DNS 

- use simple ad / AD server for forwarding VPC DNS request using DNS forwader 
- use dhcp-option-set 
<https://aws.amazon.com/blogs/security/how-to-set-up-dns-resolution-between-on-premises-networks-and-aws-using-aws-directory-service-and-amazon-route-53/> 

#### on-prem to AWS Route 53 resolve
![](https://dmhnzl5mp9mj6.cloudfront.net/security_awsblog/images/DrewDennis_architectureimage_a.png) 

#### AWS to on-prem DNS resolve 

![](https://dmhnzl5mp9mj6.cloudfront.net/security_awsblog/images/DrewDennis_flowofDNSrequestsoriginatingfrominsideVPCwithSimpleAD.png) 

---

## ELB 

- Classic LB 
	- tcp/HTTP/HTTPS ver 1 
	- ec2 classic 
	- Layer 4 
- Network LB 
 	- Layer 4 
 	- Millions of request per second,ultra low latency 
 	- Static ip address from AZ 
 	- Add ability to External IP 
- Application LB 
	- Layer 7 
	- ideal for HTTP/HTTPS 
	- Routing hostname/path based 


### Classic LB 
- choose instance not ip addess only one port per instance .
- no support hostname / path based routing 

### Application LB 
- Supports multiple domains. ( host headers )
- Choose instance,ip via Target group. 
- URL/Domain/Path based routing/rule  to TargetGroups
- ASG via Target Group ( CPU,memory)
- Fully integrates with ECS . managing target groups,paths and targets. ( NLB also)
- Dynamic port mapping for ECS Register Service 
- Host-based Routing - host field in the HTTP header 
- Patch based Routing 
- WAF ( whitelist,backlist IP, SQL injection,etc)
- ACM for SSL 
- Cipher (TLS 1 , 1.1,1,2 ) - Security Policy 
- Xforwarded for - ip address for client ip (nginx,apache needs config change)
- SNI (bind multiple SSL Certificates) 
- non SNI Client use dedicated IP. 
- supports wildcard certs.
- Listener and Healthcheck 


### Network LB 

- Layer 4 ( TCP only ) 
- **Doesn't have security group**    <https://aws.amazon.com/premiumsupport/knowledge-center/security-group-load-balancer/> 
- Asymetric route 
- handles millions of request per seconds. 
- ultra low latency 
- Static and Elastic IP support 
- Source/Client IP Preserved ( EC2/ECS only not IP target) 
- Integrated with ASG and ECS 
- Healthchecks at TCP/Application Level (http/https) 
- Static ip single per AZ. 
- Elastic IP Address per AZ single 
- helps white-list for firewall. 
- Cross-Zone LB ( enable it) 
- target ip can be used RFC1918,RFC (direct connect / vpn) 

![AWS LB Comparison ](https://d1o2okarmduwny.cloudfront.net/wp-content/uploads/2017/11/network-load-balancers.002.jpeg) 


###HealthChecks 

-HTTP,HTTPS, TCP HC - customize frequency,failure threshold 
- Customize list of successful response code for example 200-300. 
- check failures available via API and management console 
- healtch check per target group not per instance. 
- CW Metrics - ActiveFlowCount , NewFlowCount,TCP_ELB_reset_Count,HealthyHostCount,unhealthyhostCount
---

##CloudFront 

- Latency based routing 
- collapse multiple request for the same object.
- tcp window scaling 
- persistent TCP connection to origin 
- AWS backbone network 
- SSL/TLS Optimizations 
- Static / Dynamic content 
- Supports WAF,Shield,Lamda@Edge 
- Distribution WEB,RMTP 
### Distribution / Behaviors 

- Path pattern matching 
- origin selection 
- Headers - headers forward , cache behavior , user-agent 
- query strings/cookies 
- signed URL / Cookies - Cloudfront KeyPair by root of the account
- SSL Certificate - with ACM | BYO - SNI or Dedicated IP. 
- protocol enforcement - HTTP or HTTPS or both , Matchviewer , HTTP -> HTTPS 
- TTL -
- Gzip compression 
- Geographical restictions -

--- 

Module 4 

## Design and Implement for Security and Compliance 

##Security
- IAM 
- Layers of Access Control 
###  IDS / IPS 
- Hosted IDS/IPS 
- Third party SaaS Providers 

### inline WAF 
- reverse Proxy 
- 

### AWS WAF 
- Layer 7 
- ip address 


## Monitoring and Compliance 






