
### Architecting to scale

- Design for New Solutions
    
        Autoscaling policies and events
        Application integration ( SNS,SQS,Step Functions)
        Service quotas and limits
        Performance monitoring technologies

- Continuous Improvement for Existing Solutions.

        Monitoring and logging solutions
        High-performing system architectures
        Identifying and examining perfomance bottlenecks
        Scaling methodologies.


- Accelerate Workload Migration and Modernization

        Containers (ECS,EKS,Fargate,ECR)
        Serverless compute offerings (AWS Lambda)
        Integration Service(SQS,SNS,EventBridge,Step Functions)




![img_19.png](img_19.png)

![img_18.png](img_18.png)


### EC2 AutoScaling Policies


![img_13.png](img_13.png)

Default cooldown period is 300 seconds
not supported for scheduled scaling.



### Scaling containers

- Control and Complexity

      High Control/ High complexity (overhead)
      non-managed services ( eks )

      ECS (mid control/mid complexity)

      Fargate (low control/low complexity)

      App Runner (low control/low complexity)

![img_14.png](img_14.png)

![img_15.png](img_15.png


### MapReduce

![img_16.png](img_16.png)

Supports Apache Spark, HBase, Presto and Flink

Managed Hadoop framework for processing large amounts of data across EC2 instances.

A Step is a programmatic task for performing some process on the data.

A cluster is a collection of EC2 instances that host the steps.


### Monitoring and Visualizing Data

- Amazon QuickSight

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
      - Third-party data sources (Salesforce, Twitter, etc)

