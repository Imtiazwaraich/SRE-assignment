# SRE-assignment
How to execute the CloudFormation YAML code in AWS CloudFormation:

# Infrastructure Deployment using AWS CloudFormation

This repository contains the AWS CloudFormation template to deploy the infrastructure with the specified architecture.

## Prerequisites

Before you begin, make sure you have the following prerequisites:

- An AWS account
- AWS Command Line Interface (CLI) installed and configured with appropriate credentials

## Deployment Instructions

To deploy the infrastructure using AWS CloudFormation, follow these steps:

1. Clone this repository to your local machine or download the CloudFormation YAML template (`template.yml`).

2. Open a terminal or command prompt and navigate to the directory containing the CloudFormation template.

3. Run the following AWS CLI command to create the CloudFormation stack:

   ```shell
   aws cloudformation create-stack --stack-name my-infrastructure-stack --template-body file://template.yml

Replace my-infrastructure-stack with your desired stack name.

Wait for the stack creation to complete. You can monitor the progress either through the AWS Management Console or by running the following AWS CLI command:

aws cloudformation describe-stacks --stack-name my-infrastructure-stack

Replace my-infrastructure-stack with your stack name.

Once the stack creation is complete, you can retrieve the outputs of the stack using the following AWS CLI command:

aws cloudformation describe-stacks --stack-name my-infrastructure-stack --query 'Stacks[0].Outputs'

The outputs will contain the information about the created resources, such as VPC ID, subnets, and more.

**Cleanup**

To delete the infrastructure and clean up resources, you can run the following AWS CLI command:

aws cloudformation delete-stack --stack-name my-infrastructure-stack

Replace my-infrastructure-stack with your stack name. Wait for the deletion to complete.
