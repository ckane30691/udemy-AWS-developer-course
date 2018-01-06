## Identitiy Access Management 101
- Allows you to manage users and their level of access to the AWS console

### What does IAM give you?
* Centralized control of your AWS Account
* Shared access to your AWS Account
* Granular Permissions
* Identity Federation (including ActiveDirectory, Facebook, LinkedIn, etc)
* Multifactor Authentication
* Provides temporary access for users/devices and services where necessary
* Allows you to set up your own password rotation policy
* Integrates with many other AWS services
* Support PCI DSS Compliance

### Critical Terms
* Users - end users
* Groups - A collection of users under one set of permissions
* Roles - You create roles and can then assign them to AWS
* Policies - Document that defines one or more permissions

# [STS](sts.md)

## ActiveDirectory Federation

SAML lets you authenticate to ActiveDirectory

Authenticate against AR first then get assigned the security credential

## Web Identity Federation

Just need to know that you can authenticate with mobile apps
