# Task
# Terraform AWS Infrastructure Setup

## Overview
This Terraform project provisions a basic web application infrastructure on AWS, consisting of an EC2 instance running an Ubuntu web server and an RDS MySQL database.

## Repository Structure
- **main.tf:** The main Terraform configuration file that orchestrates the infrastructure setup using modules.
- **variables.tf:** Contains variable definitions for customizing the infrastructure.
- **outputs.tf:** Outputs useful information after deployment.
- **modules/**: Contains modularized code for EC2 and RDS resources.
  - **ec2/**: Terraform code specific to EC2 instance provisioning.
  - **rds/**: Terraform code specific to RDS instance provisioning.
- **screenshots/**: Contains a screenshot showing the successful deployment of the infrastructure.

## Prerequisites
- Terraform installed on your local machine.
- AWS CLI configured with your credentials.
- An AWS account with necessary permissions.

## Customization
You can customize the following variables in `variables.tf`:
- `aws_region`: The AWS region to deploy the infrastructure.
- `ami_id`: The AMI ID for the EC2 instance.
- `instance_type`: The EC2 instance type.
- `db_instance_class`: The RDS instance class.
- `db_engine`: The RDS database engine.
- `db_engine_version`: The version of the RDS database engine.
- `db_allocated_storage`: The allocated storage for the RDS instance.
- `db_name`: The database name.
- `db_username`: The database username.
- `db_password`: The database password.

## Deployment Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/terraform_challenge.git
   cd terraform_challenge
