### 7 rs

    - Retire: Get rid of it
    - Retain: Do nothing
    - Relocate: VMWare on windows
    - Rehost: Lift and shift
    - Replatform: Lift and reshape: AMIS, Managed Services
    - Refactor: Rearchitect: Serverless
    - Repurchase: Abandon existing and purchase new

### Database Migration Service

    SCT= Schema Conversion Tool.
    Including DB-> S3 (migration using DMS)
    SCT can't be used to migrate DB of the same type.

    Can be used for larger migrations multi-TB in size.

### Snowball & Snowmobile
    Snowball, Snowball Edge and Snowmobile are all part of the AWS Snow Family.
    Snowball: 80TB
    Snowmobile: 100PB

    Snowball edge
    Both Storage and compute
    42TB to 168TB
    Storage optimized, compute optimized and GPU optimized

    Snowcone: 8TB

### AWS DataSync

    Data Transfer service TO and FROM AWS.
    Migrations, Data processing transfers, archival, cost effective storage or DR/BC.
    Designed to work at huge scale.    
