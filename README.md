# Task 1: Infrastructure as Code (IaC)
• Create a Terraform configuration that provisions the following resources in AWS:  
o A VPC with public and private subnets   
o An EC2 instance in the public subnet   
o An RDS database in the private subnet   
• Ensure that the EC2 instance has the necessary security group rules to allow inbound traffic on ports 22 (SSH) and 80 (HTTP).
• Provide the Terraform code and a brief explanation of your design choices.

1. Set the region to Seoul, which is ap-northeast-2
2. Create a VPC
3. Create an Internet Gateway
4. Create a public subnet
5. create 2 private subnets
6. create a route table
7. link the routing table to the Internet Gateway
8. Route Table Association for Public Subnet
9. create a security group for ec2 for ports 22 and 80
11. create a security group for rds for port 5432
12. Import key-pair ( Terraform destroy doesn't remove key-pair, so it needs to be manually deleted through console)
13. Create an ec2 instance linked with the public subnet and security group for ec2
14. Create a subnet group for RDS 
15. create a RDS database
