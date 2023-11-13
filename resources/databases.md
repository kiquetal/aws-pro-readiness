### RDS Architecture

    Database Server as a Service.
    multiple databases on one DB Server.
    Choices are: MySQL, MariaDB, PostgreSQL, Oracle, Microsoft SQL Server.

    Read Replica uses asynchronous replication to scale read operations.
    Synchronous replication is used when Multi-AZ is enabled.The S3 backup is done using the data from
    the standby instance.

    
#### MultiAZ - Instances

    The renamed as Multi-AZ instances the replication is at the storage level.
    The primary and standby instances are in different AZs.
    The standby instance is not available for read operations.

    Backup can ocurrs from the standby instance.
    In the event of a failure the DNS record is updated to point to the standby instance.

    Not with the free tier.
    One StandBy replica ONLY, can´t be used for read and write operations.
    Failover between 60-120 seconds.
    Same region only.
    
#### MultiAZ-Cluster

    One writer can have mutiple reader instances. (sync replication)
    Is using the synchronous replication.
    Data is commited when 1+ reader finishes writing.
    1 Writer and 2 Reader.(different azs)
    Much faster hardware, Graviton + local NVME
    Fast writes to local storage => flush to EBS
    Reader can be used for reads, allowing some read scaling.
    

### AWS Backup and Restore

    Automated backup and snapshot = Both uses S3.
    Snapshot are not automatically. 
    First SNAP is full size of consumed data then onward is incremental.
    Snapshot does not expire.

    Automated backup is incremental up to retention period.(0 to 35 days)

    Cross- Region

    RDS can replicate backups to anothe region.
    both snapshot and transaction logs
    
    Restore; New RDS Instances - new addreses.
    Snapshot = single point in time, creation time.
    Restore aren´t fast - Think about RTO.

    
#### Read Replica

    Without application changes , read replica are usefuless.
    Read Replica means async replication.Could be used for another AZ.

    Up to 5 read replicas.
    Each providing an additional instance of read replica.
    Read Replica can have read replica.


#### RDS Security

    Authentication, Authorization, Encryption in transit, Encryption at rest.
    SSL/TLS is available for RDS, can be mandatory.
    RDS supports EBS volume encryption.
    Handled by host/ebs
    RDS MSSQL and RDS ORacle support TDE (Transparent Data Encryption)

### Amazon Aurora key difference

    A single primary instance + 0 more replicas.
    No local storage, uses cluster volume
    Uses a "clusters"

    Up to 15 replicas.

    All SSD based, high IOS, low latency
    Storage is billed based on what'used.
    High water mark billed for the most used.

    Restores create a new cluster
    Backtrack can be used wich allow in-place rewinds to a previous point in time.

### Aurora serverless

    You provion ACU (Aurora Capacity Units)
    ACU is a combination of CPU and Memory.

    Uses cases: infrequently used applications.
    for new applicatons.
    unpredictable workloads.


    
    
    
    
