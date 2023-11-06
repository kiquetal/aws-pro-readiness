### FSx for Windows File Server

	Fully managed native windows file servers/shares
	Designed for integration with windows environments
	Integrates with Directory Services or self-managed AD
    Single or Multi-AZ within AZ
    Back-up compatible
    Can kms at reast
    Highly perfomance.
    
    
#### Fsx Key Features
   
    VSS - User driven restores
    SMB native integration.
    DFS
    Windows permissions models


### FSx for Lustre: High Performance Computing

    Machine Learning, Big Data, Financial Modelling
    100's GB/s throughput.
    Deployment types:
        - Scratch: short term storage / No HA, NO replication.
        - PERSISTENT: Long term storage (HA in one AZ)

    Accesible over VPN or Direct Connect.
    

### Efs Architecture

    Linux Only
    General Purpose or Max I/O performance modes
    Uses NFSv4.1 protocol
    Bursting and Provisioned Throughput modes
    Supports encryption at rest 
    Every mount point has a security group

### S3 Storage classes

    S3 Standard: 99.99% availability, 11 9's durability

    S3 Intelligent Tiering: 99.9% availability, 11 9's durability
    min size is 128kb

    S3 Standard-IA: 99.9% availability, 11 9's durability
    min size is 128kb
    It is important and long-lived data that is accessed less frequently, but requires rapid access when needed.

    S3 One Zone-IA: 99.5% availability, 11 9's durability
    min size is 128kb
    Is cheaper than IA, but only stores data in one AZ.

    S3 Glacier: 99.99% availability, 11 9's durability, 

    S3 Glacier Instance = for long-lived accesed once per qtr with
    millisecond latency. 128kb for min size. 90 day minimum storage duration.

    S3 Glacier Instant : 99.99% availability, 11 9's durability
    min size is 128kb

    S3 Glacier Flexible: min 90 day storage duration,
    min size is 40kb
    Expedited: 1-5 minutes
    Standard: 3-5 
    Bulk: 5-12 hours

    S3 Glacier Deep Archive: 99.99% availability, 11 9's durability
    min is 40kb

    S3 Outposts: 99.99% availability, 11 9's durability
    

![s3-lifecycle-transitions.png](./images/s3-lifecycle-transitions.png)

