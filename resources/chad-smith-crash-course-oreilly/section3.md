#### Disaster Recovery

    AWS VM Migration Optiosn

| _                         | Create AMI | Requires Agent | Schedule replication | Failover |
|---------------------------| --- | --- | --- |----------|
| VM import/export tool     | Yes | No | NO | NO       |
| Server migration Service  | Yes | Sort of | Yes | No       |
| AWS Migration Service     | Yes | Yes | Yes | Sort of  |
| Elastic Disaster Recovery | Yes | Yes | Yes | Yes       |

#### MultiAccount setup

    Requirements for StandAlone Account 
    Payment method
    Support plan
    Verified contact info
    Root acct passwd?

    Leave Organizatoin as MemberAccount
    Cannot be delegate admin acount for any organization
    Appropiate permissions
    Enable IAM user access to billing.

    Resource manager report consideration
    The report is generated every 36 hours
    The report supports 1000 objects in output.

    Reservation and Saving plan only can be activated in payer account.
