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

    
