Terraform is **no longer** open source from 2023

- **Original Terraform:** Was fully open-source (MPL 2.0) but changed to BSL in 2023, restricting large-scale commercial use that competes with HashiCorp.
- **OpenTofu:** A community-driven, fully open-source fork of the last MPL-licensed Terraform version (v1.5), aiming for complete compatibility and governed by the Linux Foundation under the CNCF.
- **Current Status:** You can still use the core Terraform CLI, but for a truly open-source, community-governed alternative, OpenTofu is the path.

Example: 
imagine you are working with multiple cloud provider (CP) or moving to another ,the infrastructure that you created in previous need to be moved and set in accordance to new CP.

Instead of doing everything manually , TERRAFORM comes into picture ,where it manages and changes the services in accordance to new platform

It solves the problem of learning too many tools.

Developed by HASHICORP

### Work Flow:
- Define infrastructure
- Init
- Validate
- Plan
- Apply
- Destroy


## Key points

- Terraform helps avoid manual infrastructure setup
- It can work across multiple cloud providers
- It reduces complexity in managing infrastructure

## Key misconceptions to address:

**1. Terraform isn't primarily a migration tool** While Terraform _can_ help with migrations, it doesn't automatically "move" or convert infrastructure between cloud providers. **Each cloud provider has different services and APIs**. You'd need to:

- Rewrite your Terraform configuration for the new provider
- Manually map services (AWS EC2 → Azure VMs, for example)
- Recreate resources in the new environment

**2. You still need to learn provider-specific knowledge** Terraform doesn't eliminate the need to understand different cloud platforms. You still need to know:

- How each cloud provider's services work
- Their specific configuration options
- Best practices for each platform

## What Terraform actually solves:

**Infrastructure as Code (IaC)**: Write your infrastructure in declarative configuration files instead of clicking through consoles

**Consistency**: Deploy the same infrastructure reliably across environments (dev, staging, production)

**Version control**: Track infrastructure changes over time using Git

**Multi-cloud orchestration**: Manage resources across AWS, Azure, GCP, etc. from a single tool and workflow

**State management**: Terraform tracks what infrastructure exists and what needs to change

Think of Terraform as a **unified interface** for managing infrastructure, not a magic translator between cloud providers. It makes multi-cloud _management_ easier, but migrations still require significant planning and reconfiguration.

	the request from you is converted into API call for CP through Terraform

As a user we won't  directly talk to the API of Cloud provider (CP) but through Terraform.

www.geeksforgeeks.org/devops/what-is-terraform/
follow the link to know about difference between Ansible and Terraform

https://www.geeksforgeeks.org/devops/terraform-work-flow/
To know about terraform work flow


![[WhatsApp Image 2026-01-13 at 15.30.02.jpeg]]

Here user are the developer , write the code and it moves through Jenkins. While doing infrastructure configuration , the terraform state file contains the detailed output of the  resources and it should not be stored in GitHub or in any remote as well as one single machine as it contains the sensitive data regarding the resources. So to solve this issue we you aws S3 that is called remote backend with proper authentication and locking , it can be done by aws Dynamo DB , for updating the state file , which track the terraform work. 

If someone is configuring infrastructure then ,the s3 is locked . After the execution of the input ,then s3 is unlocked.


Disadvantages:
- State file is single source of truth , if it is misconfigured or corrupted then terraform is compromised and Infrastructure is messed up
- Manual changes to the Cloud Provider cannot be identified and auto-corrected
- Not a GitOps friendly tool. 
- can become very complex and difficult to manage
- Trying to position as a configuration management tool as well