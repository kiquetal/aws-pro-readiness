## Domain 2: Design for New Solutions

### Task Statement 2.1: Design a deployment strategy to meet business requirements.

Knowledge of:

- Infraestructure as Code (for example, AWS Cloudformation)
- Continous integration and continous delivery (CI/CD)
- Change management processes
- Configuration management tools( for example AWS System Manager)

Skills in:

- Determining an application or upgrade path for new services and features
- Selecting services to develop deployment strategies and implement appropiate rollback mechaninsm
- Adopting managed services as needed to redure infraestructure provisioning and patching overhead
- Making advanced technologies accesible by deleting complex development and deployment taks to AWS

- Task Statement 2.2 : Design a solution to ensure business continuity

Knowledge of:

- AWS Global Infraetructure
- AWS networking concepts( for example route53, routing methods)
- RTOs and RPOs
- Disaster recovery scenarios( backup and restore, pilot light, warm standby, multi-site)
- Disaster recovery solutions on AWS

Skills in:

- Configuring disaster recovery solutions
- Configuring data and database replication
- Performing disaster recovery testing
- Architecting a backup solution that is automated, is cost-effective and supports business continuity across multiple Availability Zones or Regions,
- Designing an architectrur that provides applicataion and infraestructure availability in the event of a disruption.
- Using processes and components for centralized monitoring to proactively recover from system failures

### Task Statement 2.3: Determine security controls based on requirements.

Knowledge of:
- IAM
- Route tables, security groups and network ACLs
- Encryption  options for data at rest and data in transit
- AWS Service endpoints
- Credential management services
- AWS Managed security services ( AWS Shield, AWS WAF, Amazon GuardDuty, AWS Security hub)

Skill in:

- Specifying IAM users and IAM roles that adhere to the principle of least privileges access
- Specifying inbound and outbound network flows by using security group rules and network ACL rules
- Developing attack mitigation strategies for large-scale web applications
- Developing encryption strategies for data at rest and data in transit
- Specifying service endpoints for service integrations
- Developing strategies for patch management to remain compliant with organizational standards

### Task Statement 2.4: Design a stategy to meet reliability requirements.

Knowledge of

- AWS Global Infraestruture
- AWS Storage services and replication stratgies ( amazon S3, amazon RDS, elasticache)
- Multi AZ and multi region architectures
- Auto scaling policies and events
- Application integration (SNS, SQS, Step Functions)
- Servcice quotas and limits

Skills in

- Designing highly avaiable application environments based on business requiremetns
- Using advanced techniques to design for failure and ensure seamless system recoverability
- Implementing loosely coupled dependencies
- Operating and maintaining high-availability architectures ( application failovers, database failovers)
- Using AWS managed services for high availability
- Implementing DNS routing policies ( route 53 latency-based routing, geolocatin routing, simple routing)

### Design a solution to meet perfomance objectives

Knowledgeof:
- Perfomance monitoring technologies
- Storage options for AWS
- Instance families and use cases
- Purpose-built databases

Skils in:

- Designing large-scale application architectures for a variety of access patterns
- Designing an elastic architecture based on business objectives
- Applying desing patterns to meet perfomance objectives with caching, buffering and replica
- Developing a process methodology for selecting purpose-built services for required tasks
- Designing a rightsizing strategy

### Task Statement 2.6: Determine a cost optimization strategy to meet solution goals and objectives
Knowledge of;

- AWS cost and usage monitoring tools (for example Cost Explorer, Trusted Advisor, AWS Prinicing Calculator)
- Pricing models(for example Reserved Instances, Saving Plans)
- Storage tiering
- Data transfer costs
- AWS managed service offerings

Skills in:

- Identitying opportunities to select and rightsize infraestructure for cost-effective resources
- Identifying appropiate pricing models.
- Perfoming data transfer modeling and selecting services to reduce data transfer costs
- Developing a strategy and implementing controls for expenditure and usage awareness.


---
    
---

### Systems Manager

- Hybrid
- Cross-platform
- Scalable
- AWS Optimized
- No complex licensing models
- Partner benefits

Capabilities:

- Run Command

      Remotely and securely run configuration actions at scale
        - Hybrid
        - Cross-platform
        - Scalable
      How does run command work? In a managed instance, requires document and some kind of invocation.
      Uses cases:
        - Monitoring your systems
        - On-demand patching
        - Deploying software
        - Run bootstrapping scripts on applictions

- State Manager
- Inventory
- Patch Manager
- Maintenance Window
- Automation
- Parameter Store
- Session Manager
- OpsCenter
- Explorer
- Change Calendar
- Distributor




---
## The Well-Architected Framework- six pillars

### Notes about Operational Excellence (excelencia operativa)

The operational excellence pillar includes
the ability to support development and run
workloads effectively, gain insight into their
operations, and to continuously improve
supporting processes and procedures to
deliver business value.

Design principles for operational excellence include

- Perform operations as code
- Annotate documentation
- Make frequent, small, reversible changes
- Refine operations procedures frequently
- Anticipate failure
- Learn from all operational failures

---
- Organization
- Prepare
- Operate
- Evolve

### Notes about Security (seguridad)

The security pillar encompasses the ability
to protect data, systems, and assets to take
advantage of cloud technologies to improve
your security.

Design principles for security include

- Implement a strong identity foundation
- Enable traceability
- Apply security at all layers
- Automate security best practices
- Protect data in transit and at rest
- Keep people away from data
- Prepare for security events

---

- Security Foundations
- Identity and Access Management
- Detective Controls
- Infrastructure Protection
- Data Protection
- Incident Response
- Application Security

### Notes about Reliability (fiabilidad)

The reliability pillar encompasses the ability
of a workload to perform its intended function
correctly and consistently when it's expected to.
This includes the ability to operate and test
the workload through its total lifecycle.

Design principles for reliability include

- Automatically recover from failure
- Test recovery procedures
- Scale horizontally to increase aggregate workload availability
- Stop guessing capacity
- Manage change in automation

---

- Foundations: Change Management
- Foundations: Failure Management
- Foundations: Workload architecture
- Foundations: Recovery Planning

### Notes about Performance Efficiency (eficiencia de rendimiento)

The performance efficiency pillar includes the
ability to use computing resources efficiently
to meet system requirements and to maintain
that efficiency as demand changes and
technologies evolve.

Design principles for performance efficiency include

- Democratize advanced technologies
- Go global in minutes
- Use serverless architectures
- Experiment more often
- Consider mechanical sympathy

---

- Selection
- Review
- Monitoring
- Tradeoffs


### Notes about Cost Optimization (optimización de costos)

The cost optimization pillar includes the
ability to run systems to deliver business
value at the lowest price point.

Design principles for cost optimization include


- Implement cloud financial management
- Adopt a consumption model
- Measure overall efficiency
- Stop spending money on data center operations
- Analyze and attribute expenditure

---
- Practice Cloud Financial Management
- Expenditure Awareness
- Cost-Effective Resources
- Matching supply and demand
- Optimizing over time

### Notes about sustainability (sostenibilidad)

The sustainability pillar focuses on 
environmental impacts, especially energy
consumption and efficiency, since the are 
important levers for architect to inform direct
action to reduce resource usage.

Design principles for sustainability include

- Understand your impact
- Establish sustainability goals
- Maxime utilization of resources
- Anticipate and adopt new, more efficient hardware
- Use managed services
- Reduce the downstream impact of your cloud workloads

