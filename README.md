# Task 1: Infrastructure as Code (IaC)
• Create a Terraform configuration that provisions the following resources in AWS:  
o A VPC with public and private subnets   
o An EC2 instance in the public subnet   
o An RDS database in the private subnet   
• Ensure that the EC2 instance has the necessary security group rules to allow inbound traffic on ports 22 (SSH) and 80 (HTTP).   
• Provide the Terraform code and a brief explanation of your design choices.

![Brainboard - Ben](https://github.com/jaekimandy/terraform_aws_sample/assets/99704906/d6b9a9b4-ae8b-4ca7-9f9f-8629a38bc6fc)



1. Copy your RSA file (id_rsa.pub) in the working directory. (Overwrite the existing one in the directory)
2. Set the region to Seoul, which is ap-northeast-2
3. Create a VPC
4. Create an Internet Gateway
5. Create a public subnet
6. Create 2 private subnets
7. Create a route table
8. Link the routing table to the Internet Gateway
9. Route Table Association for Public Subnet
10. Create a security group for ec2 for ports 22 and 80
11. Create a security group for rds for port 5432
12. Import key-pair
13. Install Nginx through command
14. Create an ec2 instance linked with the public subnet and security group for ec2
15. Create a subnet group for RDS 
16. Create an RDS database

## Instructions
Copy your RSA file (id_rsa.pub & id_rsa) in the working directory. (Overwrite the existing ones in the working directory)  
Execute the following commands
1. AWS Configure
2. Terraform init
3. Terraform plan
4. Terraform apply
5. Terraform destroy

## Testing port 22 & 80 connection
1. Copy your RSA file (id_rsa & id_rsa.pub) in the working directory. (Overwrite the existing one in the directory)
2. Run your terraform
3. Find the IP address of the EC2 in the terraform output 'ec2_instance_public_ip'.
4. To test port 20: ssh ec2-user@<IP_Address_of_ec2>
5. Logged into the newly created EC2
6. To test port 80:  http://<IP_Address_of_ec2>

## Testing of connection between EC2 & DB
When EC2 gets created PostgreSQL gets installed on EC2 to run Psql

   
