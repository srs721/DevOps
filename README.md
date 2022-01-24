# DevOps
Waterfall Model : gather requirements -> Design -> Implement -> test -> Deploy -> Maintaince
Disadvantages cannot be used for porjects which are agile and can change, Once application is in testing stage it is very difficult to go back and change that was not thought at the design stage., Not good for complex, OO project.

We Use agile methodology - Where each project is broken into smaller iterations and each iteration cycle consists of Discover <-> Design <-> Develop. Each iteration should be between a 2-8 weeks gap and each should have working product delivered. 
Disadvantages is he development team and operations team dont work togther, because developer will only dveleop and depolyment is done manually. Ops team comes back and says there are bugs and dev team should go back and repair it.

DevOps makes the entire process from commiting a change to pushing into prod using some standard process which reduces the time and also easier to roll back/identify probelms.
Solution for the above is DevOps. It bridges the gap between the Dev and Operations. It is a methodology that both the developer and operations take part during the entire lifecycle of the product from analysiing to maintaince. This happens using various stages and tools used in DevOps. Continuous process of plan,code, bulid, test, deploy, operate and monitor.

Various Stages Involved in DevOps - 
1. Version Control - Maintaining different versions of code
2. Continous Integration - Complie, validate, code review, unit tests
3. Continous Delivery - Deploying applications to UAT, test servers
4. Continous Deployment - Deploying tested products on prod env.

Azure DevOps is a centralised tool which is used to keep track of your repos, your tests, deployments.

At first stage,
Once multiple developers push changes to a shared repo in azure devOps, the devOps server automatically pulls the changes and starts a build pipeline. Build pipeline not only involves code complilation, but also code review, unit testing, integration testing, packaging the entire code into a jar/tar file (these steps can be performed by using plugins and trigger the tasks squentiallly). This happens continously.  This complete process is called Continous Intergration.

At the second stage,
Once the build is completed, azure DevOps will take that build and deploy it on test servers. In the release phase. This process is called Continous Delivery.

At third stage,
When the code is being tested successfully on the dev env, the code is automatically/manually pushed to the production environment. This step is called Continous Deployment.

This whole process is simple to identify the errors that can take place. If a build fails we know which commit caused the failure and only look at that part of the code, instead of going through the entire code. Similarly for the other stages as well.


 CONFIGURATION MANAGEMENT - 
 Example: We have performed testing in our UAT env and everything works fine, but at prod it doesnt work beacuse of the software not being upgraded. Configuration management is important for installing/upgrading the configurations. We write one script which can be used to configure it on dev and prod env.
 
Puppet is a tool which can be used for configuration management. It follows master slave approch to manage configurations across the servers. Uses pull approach
Ansible, Chef, Salt Stack are the other tools used for this purpose. Uses push approach.

CONTAINERIZATION - Nothing but light weight VM's
- We can use docker which sits on top of our OS and creates insulated environments for each of our applications to run.
- A container contains our application.
- Example: A developer writes complex requirement for a microservice service application in a docker file. The docker image is created which acts as a template and using this image multiple docker containers can be created. The docker image is then it is uplaoded to docker hub(contains repositories of the docker images) from there we can pull the image and create as many conatiners as we want in test/prod environment. Can be used to run images on different servers.


KUBERNETES - It is open source container management tool which automates container deployment , container scaling,descaling and container load balancing.

AZURE

1. Cloud computing platfrom by Microsoft - It is used to builld, deploy and manage applications through the global network of datacentres.
2. Azure service is nothing but the services provided by azure that we consume. VM, storage account etc.
3. Three types of cloud computing are -

   - IaaS(Infrastructure as a service) - IaaS is an alternative to on-premises infrastructure that encompasses storage, networking, servers, and virtualization services. 
									   - IaaS facilitates businesses’ day-to-day operations with cloud-hosted services that are easily accessible over the internet.(pay-as-you-go options). we have to worry about OS, middle ware, data, applications.(eg VM,storage accounts)
									   
   - PaaS(Platform as a service) -   Is a tool that helps developers build hardware, software, and applications. Over the internet. Configuration is already done(OS, middleware). need to take care of only my data and applications.
                                     applications on it.(eg Facebook)
   - SaaS(Software as a service) -	 tool that offers users a variety of applications without having to install software on their devices. like 0365. directly consuming the service. Provides business value.

IaaS - like purchasing a car
PaaS - renting a car
SaaS - booking ola/uber

CLOUD SERVICES 
1. Private Cloud - within organisations own infrastructure
AZURE SERVICES-
1. Compute services - VM, App services, data factory.
2. Migration services - to migrate data, apps, storage into cloud. 
3. Security and Complaince - 
4. Storage - SQL, My SQL, blob, data lakes
5. Databse
6. Networking
7. Management tools


App registration - As a developer I register my app with the my AAD. The AAD stores the apps identity using client id, secret key. Now if I have some data to be accessed using an API.
We can use the generated client id and secret and a redirect URI to generate access token, which can be used as an outh 2 authorization to our API. 
If multiple tenants wants to use this App, replication(local instances) of the app are created in respective AAD called service principle.
Client ID, secret - application object, app registration
scope,consent,token - service principle

Azure Active Directory - It is cloud based identity provider and access management service. If my company is using any of the microsoft features like O365, sharepoint, teams. We login to these services using AAD. Also AAD is used to connect to resources on azure.

Data bricks
Service bus
ARM Templates

