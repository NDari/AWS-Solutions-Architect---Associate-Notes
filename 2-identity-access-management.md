### Identity Access Management (IAM)

* A centralized location to manage users and their access to the various AWS
  services in the organization.
* Allows you to used FaceBook, Active Directory, LinkedIn, etc accounts for
  logging into your services.
* You can setup password policies for the users in the organization here, such
  as requirements on length, complexity, and periodic resets.
* **Payment Card Industry Data Security Standard (PCI DSS)**: applies to
    companies of any size that accept credit card payments. If your company
    intends to accept card payment, and store, process and transmit cardholder
    data, you need to host your data securely with a PCI compliant hosting provider
* IAM Supports PCI/DSS compliance.
* **Secret Access Key and Access Key ID**: are a unique identifier so that your
* **Role**: is similar to a user, in that it is an AWS identity with permission
    policies that determine what the identity can and cannot do in AWS. However,
    instead of being uniquely associated with one person, a role is intended
    to be assumable by anyone who needs it. Also, a role does not have any
    credentials (password or access keys) associated with it. Instead, if a
    user is assigned to a role, access keys are created dynamically and provided
    to the user.
* IAM is global, so that the users groups, roles, etc. are across all regions.
    users and applications can programmatically authenticate with AWS resources.
* **Policy**: A .json file which is used to assign permissions to a user, group,
    role, or resource. A policy allows you to specify the *actions* (what can
    be done using this policy, such as creating or deleting), *resources* (what
    resource can you take the actions on), and *effects* (what will happen when
    the user requests access). Everything is set to denied unless explicitly
    allowed here.
* **Managed Policies**: Standalone policies that you can attach to multiple
    users, groups, and roles in your AWS account. Managed policies apply only
    to identities (users, groups, and roles) - not resources. You can use two
    types of managed policies: *AWS managed policies* – created and managed
    by AWS, *Customer managed policies* ones you create and manage in your
    AWS account. Using customer managed policies, you have more precise control
    over your policies than when using AWS managed policies.
* **Inline Policies**: Policies that you create and manage, and that are
    embedded directly into a single user, group, or role. Resource-based
    policies are another form of inline policy.
* **Root Account**: The account of the owner of the AWS account. These credentials
    allow full access to all resources in the account. Because you can't restrict
    permissions for root account credentials, you should delete your
    root access keys and then create AWS Identity and Access Management (IAM)
    user credentials for everyday interaction with AWS
* When you create a new user in your account, they have no permissions by default.
* When you create a new user, that is the only time that their Secret Access Key
    and Access Key ID is visible to you. So you should download the .csv file
    containing this information and save it somewhere safe. This file is shown
    when users are created.
* **Power User Account**: Allows full access to all AWS services except for IAM
    user and group management.
