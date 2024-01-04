<h3>Type of cloud - </h3>
<li>Public</li>
<li>Private</li>
<li>Hybrid</li>
<hr>
<h2>AWS</h2>

<h3>AWS IAM </h3> - (Identity and access management) - for Authentication and Authoritation

- Users
- Policies
- Groups
- Roles - created for temparory purpose

<hr>
<h3>AWS EC2 (Elastic Cloud Compute)</h3>

<b>problems</b> - (Timely Upgrade , Security issues ,server goed down)

<h3>Types of EC2 Instances -</h3>
1- General purpose
2- Compute Optimized
3- Memory Optimized
4- Storage Optimized
5- Accelarted Optimized

```bash
<b>Chmod 600</b> - To change permission of the file
chmod stand for "change mode"

6 set read and write permissionfor the owner of the file
0 set no permissionfor the grps or others
```

<b>For doing SSH -</b>

```bash
ssh -i "key" ubuntu@"public_ip"
```
<h3>Linux Commands</h3>
For update - <b>sudo apt update</b>
Switch to root user -<b> sudo su -</b>
For logut <b>logout</b>
For update in root user - <b>apt update</b>

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

<h3>Route 53</h3> - 
<b>DNS(Domain name service) - maps domain name with ip address</b>
<span>- Domain registration</span>
<span>- DNS routing</span>
<span>- Health checking -Route 53 sends automated requests over the internet to a resource, such as a web server, to verify that it's reachable, available, and functiona</span>
 
<b>In gerneral - (DNS maps with Load balancer IP address)</b>

<hr>

<b>For connecting to a private subnet server we can use <i>"bastion-host"</i></b>
<hr>

<h3>Load balancer - </h3>
<span>1- Application Load balancer</span>
<span>2- Network load balancer</span>
<span>3- Gateway load balancer</span>

<hr>

<h3>NAT Gateway - Network address translation</h3>
<p>You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances.</p>

<p><b>VPC peering </b>- use for communication between 2 private different subnet instance.</p>

<p>Strict network access for VPC - Using NACL(at subnet level)</p>

<p><b>VPC endpoint</b> - securely access aws services within the VPC.(S3 ,DynamoDb)</p>
<hr>

<h3>AWS S3 - Simple storage service</h3>

<b>Advantage - </b>
<span>1- Availability and Durability</span>
<span>2- Scalability</span>
<span>3- Security</span>
<span>4- Cost Effective</span>
<span>5- Performance</span>

<b>Security - </b>
<span>1- Bucket policies</span>
<span>2- Access control</span> 
<span>3- Encryption</span>

<b>Storage Class -</b>
<span>1- S3 Standard (least access time)</span>
<span>2- S3 Standard-IA</span>
<span>3- One Zone-IA</span>
<span>4- S3 Glacier</span>
<span>5- S3 Glacier Instant Retrieval</span>
<span>6- S3 Glacier Flexible Retrieval</span>
<span>7- S3 Glacier Deep Archive</span>
<span>8- S3 Outposts</span>
<span>9- S3 Intelligent Tiering</span>
<hr>

<h3>IAC - Infracture as a code</h3> 
<span>1- AWS CLI (Python utility)</span>
<span>2- Terraform</span>
<span>3- Cloud Formation</span>
<span>4- CDK</span>

```bash
AWS CLI - (use only for quick and short action)

aws configure 
aws s3 ls
```

<h3>AWS CFT</h3> - Cloud formation template - Infrastructure as code-Ias
<span>1- use to create lagre infrastructuer in aws</span>
<span>2- act as a middle man b/w cloud and user</span>
<span>3- CFT support Json and YMAL template.</span>
<span>4- Convert templates into a API calls.</span>

 <b>CFT template writing style</b>
<span> 1- Declarative </span>
 <span>2- Versioned</span>
 
CFT job -
<span>1- Creating Infra</span>
<span>2- Drift Detection - configuration changes were made to your stack resources outside of CloudFormation via the AWS Management Console, CLI, and SDKs.</span>
<span>3- Drift is the difference between the expected configuration values of stack resources defined in CloudFormation templates and the actual configuration values of these resources in the corresponding CloudFormation stacks.</span>
<hr>

<h3>AWS Code Commit :</h3>

<h3>AWS Code Pipeline :</h3>

<h3>AWS Codebuild :</h3>

<h3>AWS Code deploy :</h3>
