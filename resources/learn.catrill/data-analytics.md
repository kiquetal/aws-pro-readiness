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

