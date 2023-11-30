#### Service Catalog
    Document or Database created by an IT Team
    Organised collection of products

    Self service to deploy customer products or services

    Uses review portfolios and launch products into service enabled regions

### Some files for CI/CD

    buildspec.yml : CodeBuild
    
    appspec.yml : CodeDeploy
    
    pipeline.yml : CodePipeline

### AWS CodePipeline

    The orchestration of the CI/CD process
    Continous delivery tool
    Pipelines are built from STAGES.

### AWS CodeDeploy

    Files (ec2/on-premises)
    Resources(ecs/lambda)
    Permissions(ec2/on-premises)

    Lifecycle for ec2
    - ApplicationStop
    - DownloadBundle [non-script]
    - BeforeInstall
    - Install [non-script]
    - AfterInstall
    - ApplicationStart
    - ValidateService


#### Elastic BeanStalk (EB)

    An elastic beanstalk application is a collection of
    things relating to an application- a container/folder
    .ebextensions are a way to customise EB environments

    Inside application source bundle (ZIP/WAR)
    .ebexntesions folder
    Can be used to create resources with CFN format.

#### Elastic Beanstalck and HTTPS.

    You can attach the certificate directly to the ALB.
    Or you can configure that in the EB environment.

#### AWS OpsWorks

    Ideally for Dev/Ops teams should use chef or puppet
    3 Modes:
    - Puppet Enterprise: AWS Managed Puppet Master Server
    - Chef Automate: AWS Managed chef servers
    - OpsWorks: AWS Integrated Chef, no servers

    Remember cookbooks is something related to GIT.

#### AWS System Manager - Agent Architecture.

    Manage and control ec2 and on-premsises infrastructure.
    Manage Inventory and Patch Assets

    
#### AWS System Manager - Patch Manager

    Patch Baseline : Defines which patches should be applied
    Patch Group : Defines which instances should have which patches applied
    Maintenance Window : Defines when the patches should be applied
    Run Command : Defines the actual command to be run on the instances
    Concurrency & Error Threshold   
    Compliance

    AWS-AmazonLinux2DefaultPatchBaseline
    AWS-UbuntuDefaultPatchBaseline
    AWS-DefaultPatchBaseline : critial and security updates
    AWS-WindowsPredefinedPatchBaseline: same as above
    AWS-WindowsPredefinedPatchBaseline-OS-Applications: same as above + MS Applications

    1- Define base line
    2- Create Path group
    3- Maintance windows
    4- AWS-RunPatchbaseline
    5- Compliance, Systems Manager Inventory

    

    
    
    

    
    


    
