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

### S3 - CRR( Cross-Region Replication)

    Replicate data across regions for compliance, lower latency, etc.
    Versioning must be enabled on both source and destination buckets.
    Regions must be unique.
    Files in an existing bucket are not replicated automatically.
    All subsequent updated files will be replicated automatically.
    Delete markers are not replicated.
    Deleting individual versions or delete

### S3 Replication Options

    All objects or a subset
    Storage-Class default is to maintain.
    Ownership- default is the source account. (CAREFULL ABOUT THIS! THE DESTINATION ACCOUNT COULD NOT ACCESS THE OBJECTS!)
    No system events, Glacier or Glacier Deep Archive.

    SRR - Log aggregation
    CRR - Global Resilience Improvements
    CRR - Latency Reduction

### S3 Bucket Keys

    CloudTrail KMS events now show the bucket.
    Not the object
    Works with replication, the object encryption is maintained.
    
### S3 Presigned URLS

    Uses the identity which created it.
    You can create a URL for an object you have no access to
    When using the URL, the permissions match the identity which generated it.
    Access denied could mean the generating ID never had access or doesn´t now.
    Don't generate with a role. URL stops working when temporary credentials expire.

### S3 Select and Glacier Select

    A way to retrieve objects, using SQL queries.
    Works with CSV, JSON, Parquet files, BZIP2 

### S3 Access Points

    Simplify managing access to S3 Bucketrs/Objects
    Many access point per bucket
    
### S3 Object Lock
    
    Can only be enabled for new buckets. 
    Write Once Read Many (WORM),NO DELETE, NO OVERWRITE
    Requires versioning enabled on the bucket.
    1- Retention Period
        - Compliance : Can't be overwritten or deleted for a specified period of time.
        - Governance: Special permissions can be granted allowing lock settings to be adjusted.

    2- Legal Hold
        No retention, No deletes or changes until removed.
        s3:PutObjectLegalHold is required to add or remove.

### Amazon Macie

    Uses ML to discover, classify and protect sensitive data.
    Uses CloudTrail, CloudWatch Events, CloudWatch Logs, VPC Flow Logs, S3 Logs, AWS Config, and more.
    Uses mutli-account structures.
    Reacting with S3.


### EBS Volume Types

    GP2 = SSD 
    Up to 16,000 IOPS per volume.
    Up to 250 MB/s per volume.
    GP3 = 
    Up to 16,000 IOPS per volume.
    Up to 1,000 MB/s per volume.

    Provisioned IOPS= can be adjusted independently from volume size.
    Up to 64,000 IOPS per volume.
    Up to 1,000 MB/s per volume.
    Block Express: Up to 256,000 IOPS per volume.
    Up to 4,000 MB/s per volume.

### Instance Store Volume

    Attached at launch time.
    Local on EC2 Host
    Lost on instance, move, resize, or hadrware failure 
    High Performance
    
### Choosing between Instance Store and EBS.

    Persistance = EBS (avoid instance store)
    Resilience = EBS (avoid instance store)
    
### Transfer Family

    Supports transferring TO or FROM S3 and EFS
    FTP, FTPS, SFTP, AS2, MFTW
    Multi AZ


### Placement groups

    Cluster: Pack instances close together  : low latency
    Spread keep instances separated : critical instances
    Partition: groups of instances spread apart : large distributed and replicated workloads


    Partiion placement groups
    Instances can be placed in a specific partition.
    7 partitions per AZ
    HDFS,HBASE and Cassandra
    Own racks and network switches.
    You can launch many instances in a partition.


    
### RDS Custom

    Fills the gap between between RDS and EC2 running a DB Engine.
    DB on EC2 is self managed but has overhead.
    MS SQL and Oracle
    Running within the account.

#### Dynamodb Operations, Consistency and Performance.

    Read and Write: On- demand unkown unpredictable ,low admin
    Read and Write: Provisioned predictable, high admin
    
    Every item up to 400kb
    3 read consistency models
        - Eventual Consistent Reads (Default)
        - Strongly Consistent Reads
        - Transactional Consistent Reads
    1 WCU = 1 write per second for an item up to 1kb
    1 RCU = 1 strongly consistent read per second for an item up to 4kb


    
#### DynamoDB consistency model

    Eventually consistency = Default
    Strongly consistency = 2x cost
    
#### Local Secondary INdexes (LSI)

    LSI is an alternative view for a table.
    MUST be created with a table.
    5 LSI per base table.
    Alternative SK on the table
    Shares the RCU and WCU with a table.

#### DAX

    DynamoDB Accelerator
    In memory cache for DynamoDB
    10x performance improvement
    Microsecond latency
    Eventually consistent reads only
    
#### DynamoDB Global Tables

    Global Tables provides multi-master cross-region replication.
    Last writer wins 
    Tables are created in multiple regions and added to the same global table.
    Read and Write can occur to any region
    Strongly consistent only in the same region as writes.

#### ELK Stack

    Elasticsearch - search and indexing
    in a VPC, uses compute
    Kibana visualization/ dashboard
    Logstash similar to CWLogs, needs a Logstash agent
    
#### Athena

    Serverless interactive querying service
    Ad-hoc queries on data pay only data consumed.
    Schema-on-read table like translation
    Original data never changed - remains on s3
    Schema translates data => relational like when read.
    - XML, JSON ,CSV PARQUET,AVRO ORC, APACHE Cloudtrail,VPC FLowlogs
    Support  structured, semi-structured and unustructured.

    Queries where loading/transformation isn't desired.
    AWS Glue Data Catalog & Web server Logs
    w/ Athena Federated Query ... other data sources.

#### Amazon Neptune

    Graph database
    Highly available, durable, fully managed
    Supports Apache TinkerPop and SPARQL
    Use cases: Fraud detection, Social networking,
    Recommendation engines, Life sciences,
    Knowledge graphs, Network/IT operations, and more.
    
    MultiAZ & Scales via read replicas.
    Where relationships are important.
    
 #### Quantum Ledger Databases(QLDB) 
 
    Uses S3, and near real time with Kinesis.

 





