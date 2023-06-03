


## AWS Cloud Notes
<br><br>


[Project Management 01  ](./pm-01.md).
[Project Management 02  ](./pm-02.md).
[Security 02  ](./sec-02.md).
[Security 03  ](./sec-03.md). 

[Java Spring 01  ](./spring-01.md). 
[Java Spring 02  ](./spring-02.md).
[Java Spring 03  ](./spring-03.md).
[AWS 01  ](./aws01.md).
[AWS 02  ](./aws-02.md).
[AWS 03  ](./aws-03.md).
[AWS 04  ](./aws-04.md). 
<br><br><br><br>

### AWS Networking ###






The following are examples of VPC that can be created in AWS :

VPC with a Single Public Subnet 

VPC with Public and Private Subnets

VPC with Public and Private Subnets and Hardware VPN Access

VPC with a Private Subnet Only and Hardware VPN Access

<br><br><br><br>

### The Default VPC ### 

- created with an IPv4 CIDR block of 172.30.0.0/16, 
- which provides up to 65,531 private IP v4 addresses 
- an Internet gateway attached to default VPC with a route table  


<br><br>

**Notes On Creating Subnets On VPC**

Both IPv4 and IPv6 subnets are supported within a VPC; 

CIDR blocks should not overlap with any existing CIDR blocks associated within a VPC or with another VPC.

The size of an existing CIDR block is not always flexible ; cannot be increased or decreased; its static after creation.
<br><br><br><br>


### Once VPC Is Created ###
<hr>
<br>

1. Create a subnet

2. Create a IG for public subnet

3. Create a NAT Gateway for private subnet

4. Create a route table attach an IG or subnet route table 

5. Limit or allow traffic with NACL or thru security group 





