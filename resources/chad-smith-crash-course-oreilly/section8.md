##### Question

    An on-premise operations teams has been tasked
    with migrating 900Tb data into a single AWS S3 bucket.
    The data is currently stored on a NAS and accessed using
    NFS mounts. The company has a 100Mbps internet connection


    Snowball considerations
    - Appliance-based
    - Cannot perfom direct copy
    - Cannot store entire data set
    - Requires time to ship.

    Direct Connection considerations
    - Direct copy only
    - No storage hardware
    - Copy could use all bandwidth

    S3- DataSync considerations
    - Agent-based
    - Can perform direct copy
    - Can store entire data set
    - Can use all bandwidth

