<h3>Type of cloud - </h3>
<li>Public</li>
<li>Private</li>
<li>Hybrid</li>

<hr>

<h3>AWS IAM </h3> Identity and access management - For Authentication and Authoritation

- Users
- Policies
- Groups
- Roles - created for temparory purpose

<hr>

<h3>AWS EC2 (Elastic Cloud Compute)</h3>

<b>problems</b>-

- Timely Upgrade
- Security issues
- Server goed down

<h3>Types of EC2 Instances -</h3>

- General purpose
- Compute Optimized
- Memory Optimized
- Storage Optimized
- Accelarted Optimized

<b>To change permission of the file</b>

```bash
Chmod 600
```

chmod stand for "change mode"
6 set read and write permissionfor the owner of the file
0 set no permissionfor the grps or others


<b>For doing SSH -</b>

```bash
ssh -i "key" ubuntu@"public_ip"
```


<b>For update </b>

```bash
sudo apt update
```

<b>Switch to root user </b>

```bash
sudo su -
```

<b>For logut</b> 

```bash
logout
```

<b>For update in root user</b> 

```bash
apt update
```


<hr>

<h3>VPC - Virtual Private Cloud </h3>
 VPC is a secure, isolated private cloud hosted within a public cloud.

<p>The VPC has one subnet in each of the Availability Zones in the Region, EC2 instances in each subnet, 
and an internet gateway to allow communication between the resources in your VPC and the internet.</p>

<b>Subnets</b> :- A subnet is a range of IP addresses in your VPC. A subnet must reside in a single Availability Zone.
After you add subnets, you can deploy AWS resources in your VPC.

<b>Request route </b>- internet gateway ==> public subnet ==>load balancer ==> route table ==> security grp ==>Application

<b>NAT</b> -  it mask ur outgoing ip address.

<b>VPC Flowlog - </b>

Security grp added at EC2 instance level.
<span>1- Inbound traffic</span>
<span>2- Outbound traffic</span>

<p>Default security grp allow all outbound traffic expect port 25(mail service).</p>
<p>Default security grp denies all inbound traffic.</p>

<b>NACL - Network access control list</b>
<p>optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets.</p>

<b>NACL added at the subnet level.</b>
<p>NACL is act as first level of defence.If u block something at nacl level then it will not work if it allowd at security grps level.</p>
 
<hr>

<h3>Route 53</h3>  
<b>DNS[Domain name service] - maps domain name with ip address</b>

- Domain registration
- DNS routing
- Health checking -Route 53 sends automated requests over the internet to a resource, such as a web server, to verify that it's reachable, available, and functiona</span>
 
<b>In gerneral - DNS maps with Load balancer IP address</b>

<hr>

- For connecting to a private subnet server we can use "bastion-host"
<hr>

<h3>Load balancer </h3>

- Application Load balancer</span>
- Network load balancer</span>
- Gateway load balancer</span>

<hr>

<h3>NAT Gateway - Network address translation</h3>
<p>You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances.</p>

<p><b>VPC peering </b>- use for communication between 2 private different subnet instance.</p>

<p>Strict network access for VPC - Using NACL(at subnet level)</p>

<p><b>VPC endpoint</b> - securely access aws services within the VPC.(S3 ,DynamoDb)</p>
<hr>

<h3>AWS S3 - Simple storage service</h3>

<b>Advantage </b>

- Availability and Durability
- Scalability
- Security
- Cost Effective
- Performance

<b>Security</b>

- Bucket policies
- Access control
- Encryption

<b>Storage Class</b>

- S3 Standard (least access time)
- S3 Standard-IA
- One Zone-IA
- S3 Glacier
- S3 Glacier Instant Retrieval
- S3 Glacier Flexible Retrieval
- S3 Glacier Deep Archive
- S3 Outposts
- S3 Intelligent Tiering

<hr>

<h3>IAC - Infracture as a code</h3> 

- AWS CLI (Python utility)
- Terraform
- Cloud Formation
- CDK


### AWS CLI - use only for quick and short action

```bash
aws configure
```

```bash
aws s3 ls
```

<h3>AWS CFT - Cloud formation template (Infrastructure as code-Ias)</h3>

- use to create lagre infrastructuer in aws.
- act as a middle man b/w cloud and user.
- CFT support Json and YMAL template.
- Convert templates into a API calls.

### CFT template writing style

- Declarative 
- Versioned
 
### CFT job -

- Creating Infra
- Drift Detection - configuration changes were made to your stack resources outside of CloudFormation via the AWS Management Console, CLI, and SDKs.
- Drift is the difference between the expected configuration values of stack resources defined in CloudFormation templates and the actual configuration values of these resources in the corresponding CloudFormation stacks.
<hr>

<h3>AWS Code Commit :</h3>

<h3>AWS Code Pipeline :</h3>

<h3>AWS Codebuild :</h3>

<h3>AWS Code deploy :</h3>
