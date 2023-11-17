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
    


    
    
    
