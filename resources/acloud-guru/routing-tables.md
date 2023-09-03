### Route Table

- VPC does not support broadcast.


![img.png](img.png)




### Border Gateway Protocol (BGP)

- Popular routing protocol for the internet.
- Propagates information about the network to allow for dynamic routing.
- Required for Direct Connect and optional for VPN.
- Alternative of not using BGP with AWS VPC is static routes
- BGP is a path vector protocol, which means that the BGP router keeps a list of network prefixes that can be reached and the path to reach them.
