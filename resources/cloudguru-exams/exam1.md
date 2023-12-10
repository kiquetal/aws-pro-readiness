### Domain1: Design for Organizational Complexity
    Your company is preparing for a large sales promotion coming up in 
    a few weeks. In the past you've run into scaling issues because
    the Region and AZ of your web landscape is very heavily used.
    
    For this particular promotion, we should reserve on-demand capacity
    in advance to ensure that we have the capacity we need.

    Purchasing a regional instance, will be unnecessary for this promotion.

    Your company has been running its core application on a fleet of r4.xlarg 
    You are confident that the application has a steady-state perfomance, and now
    you have been asked to purchase RI, with the option of moving
    to ohter memory of compute optimized instances.
    
    Purchase a one-year Convertible RI for two-consecutive years.


    


#### Domain 3

    The security monitor teams informs you that two EC2 instances
    are not compliant, as reported AWS Config. The lambda checks
    if EBS are encrypted using a key imported key material.
    

    - Solution create a Customer Manged Key (CMK). Create a snapshot
    copyt the snapshot and encrypt the snapshot with the CMK.
    Create a new volume from the snapshot and attach it to the EC2.


    Per the requirements of a government you must encrypt all data at rest.
    Additionally you must retain control over the key.

    - Solution: Create a Customer Managed Key (CMK), creates a random 256 bit key
    and encrypt it with wrapping key. Import the encrypted key with import token.
    
    A client calls you in a panic. They notice on their RDS conole that one
    of their mission-critical production databases has an "Available" listed under
    the Maintanenance column. They are extremely concerned that any sort of
    update to the database will negatively impact their business..

    - Defer the updates indefinetly until they are compfortable.

    If you disable the maintenace window for a DB instance, will still apply 
    the updates but aims to apply them in a period that minimizes disruptions
    to your database availability.

    Cross-zone load balancing ensures that requests are equally spread across
    all available instances, regardless of AZ. When cross-zone load balancing
    is enabled, each load balancer node distributes traffic accross the registered  
    target in all enabled AZ.

    We can increase the size of an EBS from the console or the CLI, but then
    we also need to expand the file system to use the new space.

    If a ec2 have a ssh key and this key was public, then the ec2 is compromised,
    you should stop and terminate the instance, Launch new instance
    with another ssh key pair. SSH to the new ecs instance using the new private key.

    You need to encrypt data at rest.
    You ue AWS S3, ALB with SSL termination and EBS encrypted.

    LUKS-OS is a block device encryption you alread have this capability using EBS. 
    S3 is already encrypted at rest. ALB with SSL termination is already encrypted.
