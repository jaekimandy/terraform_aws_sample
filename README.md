# Task 1: Infrastructure as Code (IaC)
• Create a Terraform configuration that provisions the following resources in AWS:  
o A VPC with public and private subnets   
o An EC2 instance in the public subnet   
o An RDS database in the private subnet   
• Ensure that the EC2 instance has the necessary security group rules to allow inbound traffic on ports 22 (SSH) and 80 (HTTP).   
• Provide the Terraform code and a brief explanation of your design choices.

![Brainboard - Ben](https://github.com/jaekimandy/terraform_aws_sample/assets/99704906/d6b9a9b4-ae8b-4ca7-9f9f-8629a38bc6fc)



1. Set the region to Seoul, which is ap-northeast-2
2. Create a VPC
3. Create an Internet Gateway
4. Create a public subnet
5. Create 2 private subnets
6. Create a route table
7. Link the routing table to the Internet Gateway
8. Route Table Association for Public Subnet
9. Create a security group for ec2 for ports 22 and 80
11. Create a security group for rds for port 5432
12. Import key-pair ( Terraform destroy doesn't remove key-pair, so it needs to be manually deleted through AWS console)
13. Create an ec2 instance linked with the public subnet and security group for ec2
14. Create a subnet group for RDS 
15. Create an RDS database

## Instructions
1. Copy your RSA file (id_rsa.pub) in the working directory. (Overwrite the existing one in the directory)
2. AWS Configure
3. Terraform init
4. Terraform plan
5. Terraform apply
6. Terraform destroy

## Testing port22 connection
1. Copy your RSA file (id_rsa.pub) in the working directory. (Overwrite the existing one in the directory)
2. Run your terraform
3. Find the IP address of the EC2 in the terraform output 'ec2_instance_public_ip'.
4. ssh ec2@<IP_Address_of_ec2)
5. Logged into the newly created EC2
   
   
