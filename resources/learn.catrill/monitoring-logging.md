#### Cloudwatch concepts

    Public Services - public services endpoints
    Agent Integration, on-premises

    Namespaces = container for metrics
    Datapoint = Timestamp, value, unit (of measure)
    Metric = time ordered set of data ppoints (CPUUtilization, NetworkIn, NetworkOut)
    Every metric has a MetricName.
    Dimensions = name/value pair, is very important to identify a metric for example for 
    many EC2 instances, you can use the instance ID as a dimension to identify the metric

    Resolution = Standard (60 seconds) or High Resolution (1 second)
    Determines the minimum period for a data granularity

    Retention 
        - sub 60 = retained for 3 hours
        - 60 seconds = 15 days
        - 5 minutes = 63 days
        - 1 hour = 455 days

    As data ages its aggregated and stored for longer with less resolution.
    
    Alarm = watches a metric over a time period.
    value of metric vs threshold over time.
    
    Alarm States
        - OK
        - INSUFFICIENT_DATA
        - ALARM    

    Data architecture - terms and concepts

    Namespaces: container for metrics
    Datapoint: timestamp, value, unit of measure
    Metric: time ordered set of data points (CPUUtilization, NetworkIn, NetworkOut)
    Every metric has a MetricName and Dimensions (name/value pair)

    Resolution: Standard (60 seconds) or High Resolution (1 second)

    Logs - Ingestion
    - Public Service - Store, Monitor, Access logging data
    - AWS on- premises IOT or any application.
    - CWAgent- system or custom application logging.
    - VPC Flow Logs - network traffic
    - CloudTrail - API calls

    Cloudwatch is a regional service.   
    Logs groups are a collection of logs streams.
    Every log stream has a log events.
    
    Logs Subscriptions - send logs to other services
    
    CloudTrail refresher
    90 days stored by default in Event History
    Management Events and Data Evens
    Only Management events are enabled by default.
    Is a regional service.
    Trail can be set for all regions.

    IAM,STS,CLOUDFRONT global service events.
    

    X-Ray - distributed tracing system

    Tracing Header: first service generates it's unique used to track a request through your distributed application
    
    Segments: data blocks, host/ip request, response work done, issues
    
    Subsegments: more granular version of the above, call to other service as a part of segment.
    Service graph: json document detailling services and resources which make up your application.
    Service Map: Visual version of the service graph showing traces.

    EC2- X-ray agent
    ECS- Agent in taks
    Lambda -enable option
    Elastic Beanstalk - enable option
    API Gateway - enable option
    Requires IAM permissions to work.

    Cost allocation tags: 
    Have to be enabled individually per account.
    AWS-Generated (aws:creeatedby) and User-Defined (user:environment)
    
    AWS Trust Advisor 
    Tied to the support plan you have.
    Free core 7 checks for free plan.
    - S3 bucket permissions
    - Security Groups - specific ports open
    - IAM use
    - MFA on root account
    - EBS public snapshots
    - RDS public snapshots
    - Service limits (50 services)

    With the business or entrprise support, you have 115 further checks     
    
    Access via the new Support API
    Integration with Cloudwatch Events


    
    
    

