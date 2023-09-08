### Bussiness Continuity

- Design Solutions for Organizational Complexity

    RTO,RPO,
    Data backup and restoration

- Design for New Solutions

    RTO, RPO
    Disaster recovery for AWS


- Continuous Improvement for Existing Solutions

    Backup practices and methods
    HA an resiliency strategies

- Accelerate Workload Migration and Modernizations

    AWS Networking services and DNS


### Difference between High Availability and Fault Tolerance

- High Availability

    - Designed to have redundancy in the system to ensure that the system is available even when some of its components fail.
  
- Fault Tolerance

    - The ability of a system to react to a failure of a component in a graceful manner without affecting the overall system.


### Disaster recovery architectures

- Backup and Restore

    Pro:
        -  Very common
    Cons:
        Could take a long time to restore

- Pilot Light

    Minimal system to get up and running
    Requires intervention to initiate the recovery process
 
- Warm Standby

    Shadow environment, ready to go live at any time
    Needs to scale up to handle the load

- Multi-Site

    Ready all the time to take full production load.
    Seconds or less
    Little or no intervention

    Expensive



