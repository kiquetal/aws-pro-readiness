#### Networking and Hybrid 

#### DHCP in a VPC

    Dynamic Host Configuration Protocol, auto configuration for network resources.
    DHCP Options are inmutable, you can't change them after creation.
    The default DNS for AWS is route53 resolver.

    Example of public DNS: ec2-3-238-142-248.us-east-2.compute.amazonaws.com
    Example of private DNS: ip-10-0-0-10.us-east-2.compute.internal
#### VPC Router Deep Dive

    HA and Redundancy.
    Route traffic between subnets.
    Controlled using Route Tables.

    Every VPC is created with a Main route table.

#### Stateful vs Stateless firewalls

    TCP run L4
    
    Security Groups are stateful.
    Network ACLs are stateless.
    The main difference is that Network ACLs have separate inbound and outbound rules, 
    while Security Groups use a single set of rules for both inbound and outbound traffic.
    
    Statefull firewall is intelligent enough to idenfity the REQUEST and RESPONSE components
    of a connection as being related.

    Allowing the REQUEST(inbound or outbound) means the respnse(inobound or outbound) is automatically allowed.


