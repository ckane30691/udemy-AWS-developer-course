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

## Securtity Token Service (STS)

### Key Terms
* Federation: Combining or joining a list of users in one domain (such as IAM) with a list of users in another domain (such as ActiveDirectory, Facebook, etc)
* Identity Broker: A service that allows you take an identity from point A or and join it to Point B
* Identity Store: Services like AR & Facebook
* Identities: A user of a service like Facebook

### Scenario
You are hosting a company website on some EC2 web servers in your vpc.  Users can login and the site should authenticate against the company's ActiveDirectory.  Your VPC is connected to the company HQ via a secure IPSEC VPN.  Users should only have access to their S3 bucket once logged in.  How do you set this up?

1. Employee enters their username and password
2. The application calls an identity broker.  The broker captures the username and password
3. The identity broker captures the username & password with LDAP
4. The identity broker calls the new GetFederationToken() function using IAM credentials.  The call must include an IAM policy and a duration (1 to 36hr)
5. Security Token Confirms Policy of IAM user making the call to GetFederationToken gives permission to create new tokens and then returns 4 values to the application: An access key, a secret access key, a token, and a duration (the token's lifetime)
6. The identity broker returns the temp security credentials to the reporting application.
7. The data storage application uses the temporary security credentials (including the token)
to make requests to Amazon S3.
8.  Amazon S2 uses IAM to verify that the credentials allow the requested operation on the given S3 bucket and key
9. IAM provides S3 with the go-ahead to perform the requested operation

#### Key Take Aways
1. Develop an Identity Broker to communicate with LDAP and AWS STS
2. Identity Broker always authenticates with LDAP first, THEN with AWS STS
3. Application then get temp access to AWS resources
