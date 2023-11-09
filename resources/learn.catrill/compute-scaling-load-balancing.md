### EC2 Purchase options

    Launch Types: 

    - On - demand: Run on shared hardware. Per second billing.
    - Reserved: Up to 75% discount. 1-3 year terms.
        Types:
        - Standard: Up to 75% discount. 1-3 year terms.
        - Convertible: Up to 54% discount. 1-3 year terms.
        - Scheduled: Up to 75% discount. 1-3 year terms.
    



    Only zonal reserved instances can be used as a capacity reservation.
    Payments options: No upfront, all upfront or partial upfront.

    - Spot: Up to 90% discount. Bid on spare capacity.
    - Dedicated: Run on dedicated hardware. Per second billing.
    
    Dedicated Hosts vs Dedicated Instances:
    Dedicated Hosts: Physical server dedicated for your use.
    Dedicated Instances: You don't own,or sharethe host.Extra charges for instances, but
    dedicated hardware.
    
    Capacity reservations:
    - Can be usefull when you need computing options with no interruptions.
    
    EC2 Saving Plans:
    - 1-3 year commitment.
    Currently ec2,fargate and lambda.
    Products have an on-demand rate and a saving plan rate.
    Beyond your commitment, you pay on-demand rates.

    Advanced ec2 networking :
    Additional ENIS can be added in and remove from other subnet, but no in other AZ.
    Primary ENI created with the instance cannot be removed.
    Security group are attached to ENI.
    

### Load Balancer -  

    Minimum of /27 subnet size.
    Architectural points
        - ELB is a DNS A record pointing at a 1+ Nodes Per AZ.
        - Nodes (in one subnet per AZ) can scale
        - Internet-facing means whole nodes have public IPv4 IPS
        - Interanl is private only IPs
        - EC2 doesn't need to be public to work with a LB.

#### Application Load Balancer vs Network Load Balancer.

    Classic Load Balancer does not scale, every unique HTTPS name requires an individual CLB
    because SNI isn´t supported.


    Application Load Balancer:
    - Layer 7
    - HTTP, HTTPS, Websocket
    - Routing based on URL
    - Routing based on hostname
    - Routing based on path
    - Routing based on query string
    - Routing based on headers
    - Routing based on source IP
    - Routing based on HTTP method
    - Routing

    Network Load Balancer: Better perfomance than ALB.
    - Layer 4
    - TCP, TLS, UDP
    - Routing based on IP
    - Routing based on TCP port
    - Routing based on UDP port
    

    
