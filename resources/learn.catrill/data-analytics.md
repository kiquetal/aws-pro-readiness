#### Kinesis Concepts

    Kinesis is a scalable streaming service
    Producers send data into a kinesis streams.
    Streams can scale from low to near infinite data rates.
    Public service and highly available.
    Streams store a 24 hour rolling window of data.

#### Difference between SQS and Kinesis

    SQS is a message queue, Kinesis is a streaming service.
    SQS is pull based, Kinesis is push based.
    SQS is not real time, Kinesis is real time.

    Ingestion should be used with Kinesis.
    SQS decoupling and asynchronous communications.
    No persistance of message, no window

##### Kinesis Data Firehose

    Fully managed service to load data for data lakes, data stores and analytics services.
    Automatically scaling fully serverless, resilient. 
    Near Real Time delivery (~60 seconds)
    Supports transformation of data on the fly.
    Billing-volume through firehose.
    
    Destinations:
    - S3
    - Redshift
    - HTTP endpoints
    - Splunk
    - ElasticSearch
    
    Can not be considered real time, just near real time.
    
    
#### Amazon Kinesis Data Analytics

    Kinesis data streams are used to allow multiple applications to ingest data.
    Kinesis DataFIrehose is used to load data into data stores(supports lambda for transformation)
    Real time processing of data, uses SQL.
    can be used to use destination using Kinesis Data Firehose.(near real time)
    can be used to send data to lambda (real time)
    can be used to send kinesis data streams (real time)
    
    Streaming data needing real-time SQL processing
    Time-series analytics elections/e-sports
    Real-time dashboards 
    Real-time metrics

#### MapReduce

    Is framework for data analysis architecture - huge scale, parallelal processing.
    EMR Architecture has at least 1 node, the master node. 
    Manly core nodes work as data nodes for HDFS.
    EMRFS is a resilient, HDFS is not.
    
#### Redshift

    Is a data warehouse, not a database.Petabyte scale.
    OLAP(columnar) - Online Analytical Processing, rather than OLTP. 
    Direct Query S3 using Redshift Spectrum.
    Direct Query other DBs using federated query
    Served based (not serverless)
    Uses cluster architecture., not multi AZ.
    Leader Node and Compute Nodes.

#### AWS Batch

    Is a managed batch processing product
    Batch processing is the execution of a series of programs or jobs on a computer without manual intervention.
    An alternative for aws lambda, when you reach the 15 minute limit.

    Job Script, Executable or Docker container submitted to batch. 
    Job Definition -iam, resources config points
    Job queue job are submitted to a queue
    Compute Environmnet

    Managed vs Unmanaged
    
#### Amazon QuickSight

    Business Intelligence (BI) service
    Create and publish interactive dashboards
    Pay-per-session pricing model
    Data Sources:
    - Amazon Athena
    - Amazon Aurora
    - Amazon OpenSearch
    - Amazon Redshift
    - Amazon S3
    - Amazon RDS
    - AWS Iot Analytics
    - Amazon Timestream
    - MySQL,Spark,PostgreSQL,SQL Server,Oracle,Presto,MariaDB,Exasol
    
#### ECS - Concepts

    Is a service for running docker containers. It's managed.Could be considered serverless
    usees EC2 instances or Fargate.

    EC2 VS ECS VS Fargate

    If you use containers use ECS
    Large workload - price consicous - ec2 mode.
    

#### SQS

    High Availability, Highly Scalable, Fully Managed Message Queuing Service.
    Standard Queue - best effort ordering, at least once delivery.
    FIFO Queue - First in First out, exactly once delivery.
    3000 messages per second with batching, 300 without.

    Max message size is 256kb
    Messages are stored in SQS until a consumer deletes them.

    Visibility Timeout - time a message is invisible to other consumers after a consumer starts processing it.
    Default is 30 seconds, max is 12 hours.

    Long Polling - Wait for a message to arrive in the queue, before returning a response.
    Short Polling - Return immediately, even if no messages are in the queue.

    Dead Letter Queue - Messages that can not be processed are sent to a dead letter queue.

#### SQS Extended Client Library

    SQS Extended Client Library for Java
    Amazon SQS Extended Client Library for Java is a Java library for Amazon SQS that extends the functionality of the Amazon SQS Java Messaging Library to support Amazon SQS message payloads of up to 2 GB.

    Stored in S3, message contains a pointer to the object in S3.

    SQS Delay Queue: has a `DelaySeconds` attribute that allows you to postpone the delivery of new messages to a queue for a number of seconds.
    Min is 0, max is 900 seconds.
    Not supported for FIFO queues.

    SNS provides topics
    SQS provides queue
    Public services, H/A
    
#### Amazozn MQ

    Based on Managed Apache ActiveMQ
    Jms api protocols such as AMQP, MQTT, OpenWire, STOMP.
    Based on Virtual Private Cloud(VPC)

#### AWS lambda
    
    Two key permission model
    - Execution Role
    - Resource Based Policy

    Lambda version: 
    Unpublished function can be changed & deployed.
    This is what you've used so far.
    Function can be published... creates an inmutable version.
    locked,no editing of that published version.

    Lambda Alias:
    Point to a specific version of a function.
    Can be used to point to a published version.
    You can´t use $LATEST with aliases.

    
    
