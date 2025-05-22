# Multi-Env-Aws-infra

### Each environment (dev, test, prod) is structured with the following essential Terraform configuration files, ensuring consistency, reusability, and clarity across deployments: ###

# a. main.tf
Defines the core infrastructure by referencing reusable modules (e.g., VPC, Subnet, EC2). It serves as the main blueprint outlining the resources and their interdependencies.

# b. variables.tf
Declares all input variables required by the configuration. This file enables flexibility and helps in parameterizing the infrastructure setup.

# c. terraform.tfvars
Provides specific values for the variables declared in variables.tf. Each environment has its own .tfvars file to reflect environment-specific configurations.

# d. backend.tf
Configures the remote backend (commonly S3) used for storing the Terraform state. This setup supports centralized, secure, and consistent state management across teams and environments.

# e. provider.tf
Specifies the cloud provider settings, such as AWS region, credentials, and provider version. This ensures consistent deployments across all environments.

# f. output.tf
Defines output values like VPC ID, Subnet ID, or EC2 instance IPs. These outputs are useful for logging, debugging, or integration with other Terraform stacks.

# g. local.tf
Contains locally scoped values such as environment name, project name, or tags. This helps reduce repetition and enables the construction of dynamic resource names and labels.
