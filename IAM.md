
# Identity and Access Management, Global service

```
• Users : are people within your organization, and can be grouped
• Groups : only contain users, not other groups
• Roles : Some AWS service will need to perform actions on your behalf , we will assignpermissions to AWS services with IAM Roles
```

# IAM – Password Policy

```
• Strong passwords = higher security for your account
• Allow all IAM users to change their own passwords
• Require users to change their password after some time (password expiration)
• Prevent password re-use

Multi Factor Authentication - MFA
• Users have access to your account and can possibly change configurations or delete resources in your AWS account
• You want to protect your Root Accounts and IAM users
• MFA = password you know + security device you own

```

# How can users access AWS ?

```
• Three options:
  • AWS Management Console (protected by password + MFA)
  • AWS Command Line Interface (CLI): protected by access keys
  • AWS Software Developer Kit (SDK) - for code: protected by access keys
  • Access Keys are generated through the AWS Console

• Users manage their own access keys
• Access Keys are secret, just like a password. Don’t share them
• Access Key ID ~= username
• Secret Access Key ~= password

```

# IAM Security Tools

```
• IAM Credentials Report (account-level)
   • a report that lists all your account's users and the status of their variouscredentials
• IAM Access Advisor (user-level)
   • Access advisor shows the service permissions granted to a user and when those services were last accessed.
   • You can use this information to revise your policies.
```

# IAM Guidelines & Best Practices

```
• Don’t use the root account except for AWS account setup
• One physical user = One AWS user
• Assign users to groups and assign permissions to groups
• Create a strong password policy
• Use and enforce the use of Multi Factor Authentication (MFA)
• Create and use Roles for giving permissions to AWS services
• Use Access Keys for Programmatic Access (CLI / SDK)
• Audit permissions of your account using IAM Credentials Report & IAM
Access Advisor
• Never share IAM users & Access Keys
```

# IAM Section – Summary

```
• Users: mapped to a physical user, has a password for AWS Console
• Groups: contains users only
• Policies: JSON document that outlines permissions for users or groups
• Roles: for EC2 instances or AWS services
• Security: MFA + Password Policy
• AWS CLI: manage your AWS services using the command-line
• AWS SDK: manage your AWS services using a programming language
• Access Keys: access AWS using the CLI or SDK
• Audit: IAM Credential Reports & IAM Access Advisor
```
