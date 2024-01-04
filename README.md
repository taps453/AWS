Type of cloud -  Public , Private , Hybrid

<h2>AWS</h2>

AWS IAM (Identity and access management) - for Authentication and Authoritation

- Users
- Policies
- Groups
- Roles - created for temparory purpose

----------------------------------------------------------------------------------------------------------------
AWS EC2 (Elastic Cloud Compute) -

problems(Timely Upgrade , Security issues ,server goed down)

Types of EC2 Instances -
- General purpose
- Compute Optimized
- Memory Optimized
- Storage Optimized
- Accelarted Optimized

Chmod 600 - to change permission of the file
chmod stand for "change mode"
6 set read and write permissionfor the owner of the file
0 set no permissionfor the grps or others

ssh -i "key" ubuntu@"public_ip"

for update - "sudo apt update"

switch to root user - "sudo su -"
for logut "logout"
for update in root user - "apt update"


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
VPC -(vpc is a secure, isolated private cloud hosted within a public cloud)
Virtual Private Cloud 

The VPC has one subnet in each of the Availability Zones in the Region, EC2 instances in each subnet, 
and an internet gateway to allow communication between the resources in your VPC and the internet.

Subnets :- A subnet is a range of IP addresses in your VPC. A subnet must reside in a single Availability Zone.
After you add subnets, you can deploy AWS resources in your VPC.

Request route - internet gateway ==> public subnet ==>load balancer ==> route table ==> security grp ==>Application

NAT -  it mask ur outgoing ip address.
VPC Flowlog - 

Security grp added at EC2 instance level.
Inbound traffic
Outbound traffic

Default security grp allow all outbound traffic expect port 25(mail service).
Default security grp denies all inbound traffic.

NACL - Network access control list
-optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets.

NACL added at the subnet level.
-NACL is act as first level of defence.If u block something at
nacl level then it will not work if it allowd at security grps level.
 
 
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Route 53 - DNS(Domain name service)-maps domain name with ip address
- Domain registration, 
- DNS routing
- Health checking -Route 53 sends automated requests over the internet to a resource, such as a web server, to verify that it's reachable, available, and functiona
 
In gerneral - (DNS maps with Load balancer IP address)

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
For connecting to a private subnet server we can use "bastion-host"

(Day 7 project)
Load balancer - 
-Application Load balancer
-Network load balancer
-Gateway load balancer

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
NAT Gateway - Network address translation
You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances.

VPC peering - use for communication between 2 private different subnet instance.

strict network access fro VPC - Using NACL(at subnet level)

VPC endpoint - securely access aws services within the VPC.(S3 ,DynamoDb)
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

AWS S3 - Simple storage service

Advantage - 
-Availability and Durability
-Scalability
-Security
-Cost Effective
-Performance

Security - 
-Bucket policies, Access control, Encryption

Storage Class -  
-S3 Standard (least access time)
-S3 Standard-IA
-One Zone-IA
-S3 Glacier
-S3 Glacier Instant Retrieval
-S3 Glacier Flexible Retrieval
-S3 Glacier Deep Archive
-S3 Outposts
-S3 Intelligent Tiering
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Automation tools - 
-AWS CLI (Python utility)
-Terraform
-Cloud Formation
-CDK

AWS CLI - (use only for quick and short action)
aws configure 
aws s3 ls
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
AWS CFT - Cloud formation template - Infrastructure as code-Ias
- use to create lagre infrastructuer in aws
- act as a middle man b/w cloud and user
- CFT support Json and YMAL template.
- Convert templates into a API calls.

 
 --Declarative 
 --versioned
 
CFT job -
-Creating Infra
-Drift Detection - configuration changes were made to your stack resources outside of CloudFormation via the AWS Management Console, CLI, and SDKs.
-Drift is the difference between the expected configuration values of stack resources defined in CloudFormation templates and the actual configuration values of these resources in the corresponding CloudFormation stacks
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

AWS Code Commit - (Git)

AWS Code Pipeline - 

AWS Codebuild - 
AWS Code deploy -
