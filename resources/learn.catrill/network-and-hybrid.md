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
    
    Security Groups are stateful. (detects response traffic automatically(
    Network ACLs are stateless.
    The main difference is that Network ACLs have separate inbound and outbound rules, 
    while Security Groups use a single set of rules for both inbound and outbound traffic.
    
    Statefull firewall is intelligent enough to idenfity the REQUEST and RESPONSE components
    of a connection as being related.

    Allowing the REQUEST(inbound or outbound) means the respnse(inobound or outbound) is automatically allowed.


    Network Access Control List (NACL) is a stateless firewall.
    
    Custom NACL
    They have only one rule, for inbound and outbound, they deny all traffic by default.
    Only impacts data crossing subnet boundary
    Ips/CIDR,Port & Protocols, no logical resources
    NACL cannot be assigned to AWS resources, they are associated with subnets.

    
    SG are attached to ENIS.

![img_sg_inbound.png](./images/img_sg_inbound.png)

    Capacity: 200 rules per NACL
    60 rules per SG

    NACLs are evaluated before SGs when traffic enters or leaves a subnet.


#### AWS Local Zone

    Think as single AZ, locates near your parent region

### Border Gateway Protocol (BGP)

    Autonomous System (AS) Routers controlled by one entity a network in BGP.
    
### Global Accelerator

    Global Accelerator is a networking service that sends your user’s traffic through Amazon Web Services’ global network infrastructure, improving your
    internet user performance by up to 60%.

    Moves the AWS network closer to customers.
    Connections enter at edge using anycast IP addresses.
    Transit over AWS backbone to 1+ locations.
    Can be used for NON HTTPS( TCP or UDP) traffic.

### IPSEC VPN Fundamentals

    Has two main phases: IKE phase 1 (slow) and IKE phase 2 (fast)
    IKE phase 1: Authentication and key exchange
    Using Asymmetric encryption to agree on, andcrate a shared symmetric key.

    IKE phase 2: Fast & Agile
    Uses the keys agreed in phase 1 to create a secure tunnel.
    Create IPSEC CA and IPSEC tunnel.

  Policy-based VPN
  rule sets match traffic => a pair of SAs
  different tules/security settings

  Route-based VPN
  target matching (prefix)
  matches a single pair of Sas





