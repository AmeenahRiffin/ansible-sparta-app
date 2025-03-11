

# Infrastructure as Code (IaC) and Ansible Research

- [Infrastructure as Code (IaC) and Ansible Research](#infrastructure-as-code-iac-and-ansible-research)
  - [What is Infrastructure as Code?](#what-is-infrastructure-as-code)
    - [Key Benefits of IaC](#key-benefits-of-iac)
    - [When to Use IaC](#when-to-use-iac)
    - [Popular IaC Tools](#popular-iac-tools)
  - [Configuration Management vs. Provisioning](#configuration-management-vs-provisioning)
    - [Configuration Management (CM)](#configuration-management-cm)
    - [Infrastructure Provisioning](#infrastructure-provisioning)
    - [Ansible Deep Dive](#ansible-deep-dive)
    - [Industry Adoption](#industry-adoption)
  - [What is Ansible?](#what-is-ansible)
    - [Why Use Ansible?](#why-use-ansible)
    - [Basic Ansible Components](#basic-ansible-components)
  - [Printing Facts in Ansible](#printing-facts-in-ansible)
    - [What is it?](#what-is-it)
    - [When should you gather facts?](#when-should-you-gather-facts)
    - [When should you skip fact gathering?](#when-should-you-skip-fact-gathering)


## What is Infrastructure as Code?
Infrastructure as Code is the practice of managing and provisioning computing infrastructure through machine-readable definition files rather than manual processes. It treats infrastructure configuration like software code.

### Key Benefits of IaC
- Consistency in infrastructure deployment
- Version control for infrastructure changes
- Automated scaling and management
- Reduced human error
- Faster deployment cycles
  

### When to Use IaC
- During cloud infrastructure deployment
- For maintaining consistent development environments
- When implementing continuous integration/deployment
- For disaster recovery planning
- Managing multiple environments (dev, staging, prod)

### Popular IaC Tools
- Terraform (Multi-cloud provisioning)
- AWS CloudFormation (AWS-specific)
- Azure Resource Manager (Azure-specific)
- Google Cloud Deployment Manager
- Pulumi (Multi-language support)

## Configuration Management vs. Provisioning

### Configuration Management (CM)
- Maintains systems in a desired state
- Manages software and settings
- Handles updates and patches
- Examples: Ansible, Chef, Puppet, Salt

### Infrastructure Provisioning
- Creates/destroys infrastructure resources
- Manages cloud resources (VMs, networks, storage)
- Handles resource lifecycle
- Tools like Terraform specialize in this

### Ansible Deep Dive
- Push-based configuration management
- Uses SSH for communication
- Declarative approach using YAML
- Can handle both CM and limited provisioning
- Ideal for application deployment

### Industry Adoption
- Netflix: Uses Spinnaker with Terraform
- Google: Relies on Kubernetes and Terraform
- Amazon: Employs CloudFormation
- Microsoft: Utilizes ARM templates
- Reddit: Implements Ansible for configuration
- Twitter: Uses Puppet for configuration management


## What is Ansible?
Ansible is an open-source automation tool that automates software provisioning, configuration management, and application deployment.

### Why Use Ansible?
- Agentless architecture (only requires SSH)
- Simple YAML syntax
- Large community and module support
- Easy to learn and implement
- Works with multiple platforms

### Basic Ansible Components
- Playbooks: Contains the tasks to be executed
- Inventory: Lists the target hosts
- Modules: Pre-built functions for specific tasks
- Roles: Reusable configurations




## Printing Facts in Ansible

### What is it?
A demonstration of how to gather system information (facts) in Ansible

### When should you gather facts?
- You need to know system details (OS, IP addresses, hardware info)
- You want to run tasks based on system properties
- You're creating config files that need host-specific information

### When should you skip fact gathering?
- Your tasks don't need system information
- You're doing basic things like managing files or services
- Your target devices don't support fact gathering
- You need the playbook to run as fast as possible

