🚀 Terraform Project: AWS VPC Setup with ALB & S3 Integration
Project Overview
This project demonstrates the deployment of a highly available web infrastructure on AWS using Terraform. The infrastructure includes a Virtual Private Cloud (VPC) with public subnets, EC2 instances running Apache web servers, an Application Load Balancer (ALB), and an S3 bucket for static content. The entire setup is automated using Terraform, ensuring consistent and repeatable deployments.

Table of Contents
Architecture Diagram
Features
Prerequisites
Getting Started
Clone the Repository
Configure AWS CLI
Terraform Initialization
Deploy the Infrastructure
File Structure
Outputs
Clean Up
Contributing
License
Architecture Diagram
 
![Terraform with aws](https://github.com/user-attachments/assets/59da2f50-1729-4d8d-b07c-f1e48f12c76d)

Features
VPC Setup: Custom VPC with public subnets in multiple availability zones.
Security Configuration: Security groups to control inbound and outbound traffic.
Web Server Deployment: Two EC2 instances with Apache, each serving a custom HTML page.
Load Balancer: ALB distributes traffic between the EC2 instances for high availability.
S3 Bucket: Integration with an S3 bucket for managing static assets.
Automation: Full automation of infrastructure setup using Terraform.
Prerequisites
Terraform: Install Terraform
AWS Account: An active AWS account with appropriate IAM permissions.
AWS CLI: Install AWS CLI and configure it with your credentials.
Getting Started
Clone the Repository

git clone https://github.com/yourusername/terraform-aws-vpc-alb-s3.git
cd terraform-aws-vpc-alb-s3
Configure AWS CLI
Ensure your AWS CLI is configured with the appropriate credentials:



aws configure
Terraform Initialization
Initialize Terraform to download necessary providers and modules:



terraform init
Deploy the Infrastructure
To deploy the infrastructure, simply run:


terraform apply
Terraform will prompt you to confirm. Type yes to proceed.

File Structure

├── main.tf                    # Main Terraform configuration file
├── variables.tf               # Input variables definition
├── outputs.tf                 # Output variables definition
├── userdata.sh                # User data script for EC2 instance 1
├── userdata1.sh               # User data script for EC2 instance 2
├── README.md                  # Project README file
└── terraform.tfstate          # Terraform state file (auto-generated)
Outputs
After successful deployment, Terraform will provide the DNS name of the load balancer:


Outputs:

loadbalancerdns = "myalb-xxxxxxxxxx.ap-south-1.elb.amazonaws.com"
You can visit this URL in your browser to see the web servers in action.

Clean Up
To clean up and remove the infrastructure, run:


terraform destroy
This will delete all the resources created by Terraform.

