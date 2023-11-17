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
    
    
    
    
