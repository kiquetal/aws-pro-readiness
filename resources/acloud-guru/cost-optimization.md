### Cost Optimization

- Provision the resource you need and nothing more.
- Consolidate where possible for greater density and lower complexity..
- Right-Sizing : Using lowest cost resource that meets your needs.
- Loosely coupled architectures : Decoupling resources to reduce interdependencies.

### Purchase options

- Reserved Instances: Up to 75% off on-demand price.
types:
  - Standard : Use for steady state usage.
  - Convertible: Can change the attributes of the RI as long as the exchange results in the creation of Reserved Instances of equal or greater value.
  - Scheduled: Available to launch within the time windows you reserve.

- Spot Instances

### Order from least to most expensive

- Scheduled Reserved Instances: 1 year commitment, 30% off on-demand price.
- Convertible Partial Upfront Reserved Instances: 1 year commitment, 45% off on-demand price.
  (can change for other instance in the same Region, the same family,and operating system)
- Standard Reserved Instances: 1 year commitment, 50% off on-demand price. (can change 
 size within the same instance family, can change AZ, can change network platform)
- Convertible Standard Reserved Instances: 1 year commitment, 54% off on-demand price.
  (can change instance family, can change AZ, can change network platform)


### Differences between Dedicated Host and Dedicated Instance

- Dedicated Host: Physical server dedicated for your use.
- Dedicated Instance: Virtual machine running on a physical server dedicated for your use,can
share with other non-dedicated instances in the same account.
- Dedicated Host are available on-demand (hourly) or reservation (1 year or 3 years),for on-demand, reserved and spot instances.
- Dedicated Instance are available on-demand (hourly) or reservation (1 year or 3 years),for on-demand and reserved instances.


### Difference between Zonal RI and Regional RI

- Zonal RI: Reserved Instances that provide a capacity reservation in a specific Availability Zone.

- Regional RI: Reserved Instances that provide a capacity reservation in a region. If no AZ is specified, no reservation
is created but the disscount is applied to any instance in the family
in any AZ in the region.

