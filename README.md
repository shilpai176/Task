# Terraform AWS Infrastructure Setup

## Overview
This Terraform project provisions a basic web application infrastructure on AWS, consisting of an EC2 instance running an Ubuntu web server and an RDS MySQL database.

## Repository Structure
- **main.tf:** The main Terraform configuration file that orchestrates the infrastructure setup using modules.
- **variables.tf:** Contains variable definitions for customizing the infrastructure.
- **outputs.tf:** Outputs useful information after deployment.
  
## Prerequisites
- Terraform installed on your local machine.
- AWS CLI configured with proper credentials.
- An AWS account with necessary permissions
- We have configured aws account by using free trial account. as per the task requirement db-instance class is to db.t2.micro but it was 
  not supported for free trial so we have changed the db.t3.micro
- The Ubuntu 20.04 is not supported in free trial so I have configured the ubuntu-noble-24.04-amd64-server-20240801 version

## Customization
You can customize the following variables in `variables.tf`:
- `aws_region`: The AWS region where resources will be created (default: us-west-2).
- `ami_id`: The ID of the AMI used for the EC2 instance (default: ami-05134c8ef96964280).
- `instance_type`:The instance type for the EC2 instance (default: t2.micro).
- `db_instance_class`: The instance class for the RDS MySQL instance (default: db.t3.micro)..
- `db_engine`: The RDS database engine.
- `db_engine_version`: The database engine to use (default: mysql).
- `db_allocated_storage`: The allocated storage for the RDS instance in GB (default: 20).
- `db_name`: The name of the MySQL database (default: mydb).
- `db_username`: The username for the MySQL database (default: admin).
- `db_password`: The password for the MySQL database (sensitive, default: XXXXX(add the password).

## Deployment Instructions
1. crete the main.tf,output.tf and variable.tf files in terraform add the given code in there respective tf files.
2. Initialize Terraform
   Run the following command to initialize Terraform, which will download the necessary providers:
   /* Terraform init */
3. Review the Plan
   It's a good practice to review what Terraform will do before applying the changes. Use the following command to see the execution plan:
   /* Terraform Plan */
4. Apply the Configuration
    Apply the configuration to create the resources on AWS:
     /* Terraform Apply */
