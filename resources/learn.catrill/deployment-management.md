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


    
