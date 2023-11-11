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
