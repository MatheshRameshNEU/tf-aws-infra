# AWS VPC and Subnet Setup with Terraform

This project provides a Terraform configuration to create an AWS Virtual Private Cloud (VPC) along with public and private subnets, route tables, and an internet gateway.

## Prerequisites

Before you begin, ensure that you have:

- An AWS Cloud Platform account.
- AWS CLI installed and configured.
- Terraform CLI installed.

## Configuration Steps

1. Install and set up the AWS CLI and Terraform on your local machine.

2. Clone the repository containing the Terraform configuration files using the following command: `git clone git@github.com:CSYE6225-12922-Mathesh/tf-aws-infra.git`.

3. Navigate to the cloned repository directory.

4. Review and update Terraform configuration: Create a new Terraform configuration file (e.g., `main.tf`) or modify the existing ones to define the required resources such as networks and subnets. Ensure that the values are not hard-coded in your Terraform configuration files. You can use variables to make the configuration dynamic.

5. Variables are defined in a separate file (e.g., `variables.tf`) to hold values like VPC name, region, VPC CIDR range, etc. This allows you to reuse the same Terraform configuration for multiple VPCs by changing the variable values.

6. Initialize the Terraform configuration by running `terraform init`.

7. Validate the configuration using `terraform validate`.

8. Plan the infrastructure changes with `terraform plan`.

9. Apply the changes to create the VPC and subnets using `terraform apply`.

## Continuous Integration (CI) Workflow

The Continuous Integration (CI) workflow for this project is implemented using GitHub Actions. It includes the following steps:

1. When a new pull request or push event occurs, GitHub Actions triggers the workflow.

2. The workflow checks out the repository's code.

3. It installs Terraform and initializes the working directory.

4. The `terraform fmt` command is executed to format the Terraform configuration files.

5. The `terraform validate` command is executed to validate the Terraform configuration syntax.

6. If the validation is successful, the workflow proceeds to the next steps; otherwise, it fails and notifies the user.

7. After successful validation, the workflow continues with additional steps.

## Conclusion

With this setup, you can easily manage and provision AWS infrastructure using Terraform, ensuring a dynamic and reusable configuration. The CI integration helps maintain quality and consistency throughout your project.
