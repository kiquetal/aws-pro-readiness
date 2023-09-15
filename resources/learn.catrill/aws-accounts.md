### Course AWS Accounts


- An AWS Account is a container for identities and resources.

-> unique email, and a credit card. 

![img.png](./images/img.png)


Identity Center Center (Formerly AWS SSO), requires a permission set and group/user to
allow access to AWS accounts.

Management account is the account that you use to create and manage AWS Organizations.
Member accounts are the accounts that you invite to join your organization.

Payer account: Management account that pays for all the charges accrued by the member accounts.

#### Service Control Policies

Inherits permissions from the parent account.
Can be applied to OUs or accounts.

![img-scp.png](./images/img-scp.png

### Security Token Service (STS)

The trust policy controls who can assume the role. Conceptually this is a wall around the role.
They're valid until they expire.

Trust policy has no impact on existing credentials.

The correct way to revoke access is to apply an inline policy AWSRevokeOlderSessions to the role.

### Policy Interpretation Deep Dive.

Structure:

- Version
- Statement
    - Sid
    - Effect
    - Principal
    - Action
    - Resource
    - Condition


