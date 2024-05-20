## Dynamic Website Hosting on AWS - DevOps Project
Overview
This project involves hosting a dynamic website on AWS using a variety of AWS services to ensure scalability, security, and fault tolerance. The project utilizes a Virtual Private Cloud (VPC) setup with public and private subnets, EC2 instances, an Application Load Balancer, and Auto Scaling Groups. The repository contains a reference diagram and deployment scripts to replicate the ##setup.

## Architecture

The architecture consist of: 

Virtual Private Cloud (VPC): Configured with both public and private subnets across two availability zones to enhance fault tolerance and availability.
Internet Gateway: Enables internet connectivity for VPC instances.
Security Groups: Network firewalls to control traffic to and from the instances.
Availability Zones: Utilized for higher availability and redundancy.
Public Subnets: Host infrastructure components like NAT Gateway and Application Load Balancer.
Private Subnets: Securely host web servers (EC2 instances).
NAT Gateway: Allows instances in private subnets to access the internet.
EC2 Instances: Host the dynamic website.
Application Load Balancer: Distributes traffic evenly to EC2 instances in the Auto Scaling Group.
Auto Scaling Group: Manages EC2 instances to maintain website availability and performance.
Certificate Manager: Secures application communications.
Simple Notification Service (SNS): Alerts about activities within the Auto Scaling Group.
Route 53: Domain registration and DNS setup.
S3: Stores application code.
## AWS Resources

## Networking 
VPC: Configured with public and private subnets in two availability zones.
Internet Gateway: Provides internet access to VPC instances.
Security Groups: Manage inbound and outbound traffic.
Public Subnets: For NAT Gateway and Application Load Balancer.
Private Subnets: For EC2 instances hosting the website.
NAT Gateway: Allows internet access for instances in private subnets.
EC2 Instance Connect Endpoint: For secure connections to instances.
## Compute and Load Balancing
EC2 Instances: Host the website within private subnets.
Application Load Balancer: Balances traffic across EC2 instances.
Auto Scaling Group: Ensures scalability and high availability.
## Security and Monitoring
Certificate Manager: Secures website communications.
Simple Notification Service (SNS): Sends alerts for Auto Scaling Group activities.
## Domain and Storage
Route 53: Manages domain registration and DNS records.
S3: Stores application code.
## Deployment Instructions
Clone the Repository:
sh
Copy code
git clone https://github.com/your-repository.git
Navigate to the Project Directory:
sh
Copy code
cd your-repository
Review the Reference Diagram:
Refer to reference-diagram.png for an overview of the architecture.
Deploy the VPC and Subnets:
Use the provided CloudFormation or Terraform scripts in the vpc directory.
Configure Security Groups:
Set up security groups as defined in the security-groups directory.
Launch EC2 Instances:
Use the EC2 launch scripts in the ec2 directory to set up instances in private subnets.
Set Up Load Balancer and Auto Scaling:
Follow instructions in the load-balancer and auto-scaling directories.
Configure Route 53:
Update DNS records using the scripts in the route-53 directory.
Deploy Application Code:
Upload your application code to S3 and deploy to EC2 instances.
