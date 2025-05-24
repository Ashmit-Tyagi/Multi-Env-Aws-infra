# Multi-Env-Aws-infra

# In this project, Terraform is used to provision and manage infrastructure across multiple environments — development (dev), testing (test), and production (prod). The setup follows a modular architecture, where each component of the infrastructure (such as EC2, VPC, Subnets, etc.) is defined in separate, reusable modules. This modular structure improves code organization, simplifies maintenance, and makes it easier to scale the infrastructure as new resources or environments are introduced.

### Each environment (dev, test, prod) is structured with the following essential Terraform configuration files, ensuring consistency, reusability, and clarity across deployments: ###

# a. main.tf
Defines the core infrastructure by referencing reusable modules (e.g., VPC, Subnet, EC2). It serves as the main blueprint outlining the resources and their interdependencies.

# b. variables.tf
Declares all input variables required by the configuration. This file enables flexibility and helps in parameterizing the infrastructure setup.

# c. terraform.tfvars
Provides specific values for the variables declared in variables.tf. Each environment has its own .tfvars file to reflect environment-specific configurations.

# d. backend.tf
Configures the remote backend (commonly S3) used for storing the Terraform state. This setup supports centralized, secure, and consistent state management across teams and environments.

# e. output.tf
Defines output values like VPC ID, Subnet ID, or EC2 instance IPs. These outputs are useful for logging, debugging, or integration with other Terraform stacks.

# f. local.tf
Contains locally scoped values such as environment name, project name. This helps reduce repetition and enables the construction of dynamic resource names and labels.
