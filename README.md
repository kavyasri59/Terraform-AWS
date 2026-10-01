# Terraform AWS EC2

This project demonstrates how to create and manage an AWS EC2 instance using Terraform.

# Project Overview

Terraform is used to provision an EC2 instance in AWS.

AWS Configuration

| Configuration | Value |
|---|---|
| Cloud Provider | AWS |
| Region | `us-east-1` |
| Resource | EC2 Instance |
| Instance Type | `t3.micro` |
| AMI ID | `ami-0b6d9d3d33ba97d99` |
| EC2 Name | `Kavya` |
| Terraform Resource Name | `kavya` |

# Terraform Configuration

The `main.tf` file contains the following configuration:

```hcl
provider "aws" {
  region = "us-east-1"
}

resource "aws_instance" "kavya" {
  ami           = "ami-0b6d9d3d33ba97d99"
  instance_type = "t3.micro"

  tags = {
    Name = "Kavya"
  }
}
