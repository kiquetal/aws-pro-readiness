#### Disaster Recovery / Business Continuity

    - RTO (Recovery Time Objective)
    - RPO (Recovery Point Objective)
    
    - Backup and Restore:
        Can last for hours or days.
    - Pilot Light
        Can last for minutes or hours.
    - Warm Standby
        Can last for seconds or minutes.
    - Multi-Site
        Can be almost instantaneous.

### DR- COMPUTE

    EBS resides in a single AZ.
    EC2 host have ec2 instances and is restricted to a single AZ.
    You can protect using ASG and Multi-AZ.
    
    AZ failure means ECS container host failure
    In fargate mode containers use ENIś in a VPC.
    Service can be used to achieve a similar
    architecture to auto scaling groups.


