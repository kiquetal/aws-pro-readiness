#### Reliability and Availability

    EBS
    AZ Score
    Synchronus writes
    Requires EC2


    EFS
    Regional
    Mount targets are AZ scoped
    3X
    Requires compute

    FsX
    AZ scope    
    Requires ec2

    S3
    Regional
    3x
    Direct Access


    A company's web application is deployed in AWS. The application uses Cloudfront,
    an Application Load Balancer and Auto-scaling group of EC2.

    Network security and permissions.

    An application runs on EC2 instances in a VPC and accesses a dynamodb table that
    contains sesitive data. The EC2 instance use an IAM role granting access to the
    table.



