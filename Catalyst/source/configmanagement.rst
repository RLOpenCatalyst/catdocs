


.. _configure-nexus:

Nexus Server
^^^^^^^^^^^^

Nexus is a repository manager. It allows you to proxy, collect, and manage your dependencies so that you are not constantly juggling a collection of JARs. It makes it easy to distribute your software. Internally, you configure your build to publish artifacts to Nexus and they then become available to other developers. You get the benefits of having your own ‘central’, and there is no easier way to collaborate.

RLCatalyst works with different repositories where you have kept your artifacts . If you have a nexus repository, add it here

To configure a new Nexus server follow the steps below:

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Devops Setup
 * Click on Nexus Server
 * Click on New button provided
 * Enter the Nexus server name in the Nexus Server Name field
 * Enter nexus server username in the User Name field
 * Enter nexus server password in the Password field
 * Enter nexus server URL in the Nexus Server URL field
 * Choose the organization from the Organization drop down list
 * Click on + icon present next to Nexus Group ID Details and enter valid Nexus GroupID and save

 .. image:: /images/updated_img/nexusDetails.png



 * Click on Save button
 * Now the Nexus server setup is ready and listed in the Nexus Server page

 .. image:: /images/updated_img/nexusList.png

**Hereby attaching a video which will demonstrate as in how to Create Nexus in RLCatalyst:**


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/RDiPzUPOCR8" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****

.. _associate-nexus:

Once Nexus Server is configured you have to associate Repository details to your Project. Follow the below steps:

 * Go to Projects Page

 * Edit your Project

 * Click on + icon present next to Repository Details

 * Select your Repository Server and Repository Name

  .. image:: /images/repoDetails.png


 * Click on Save button on Add Repository Details page
 
 * Click on Save button on Edit Project Page


Docker
^^^^^^

Docker is all about making it easier to create, deploy, and run applications by using containers. Containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package.

You can configure the Docker setup with RLCatalyst. To configure the Docker setup follow the steps below:

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Devops Setup
 * Click on Docker
 * Click on New button provided 
 * Select the Organization from the Organization drop down list
 * Provide a reference name in the Reference Name field
 * Provide the registry in the Docker Hub Registry field provided 
 * Provide the Docker user ID in the User ID field
 * Provide the email address to connect to the Docker in the Email Id field
 * Enter the Docker password in the Password field

 .. image:: /images/updated_img/createDocker.png

 * Click Save button
 * Now Docker is successfully configured to RL Catalyst

**Hereby attaching a video which will demonstrate as in how to Create Docker in RLCatalyst:**


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/MYjKmgLpO7c" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****


.. _Configure-Jenkins:

Jenkins
^^^^^^^

Jenkins is CI/CD tool which can be used for build and deployment automation. You can configure the Jenkins setup with RLCatalyst.To configure the Jenkins setup follow the steps below:

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on DevOps Setup
 * Click on Jenkins
 * Click on New button provided 
 * Select the Organization to which the Jenkins server will be attached to
 * Enter the name in the Name field
 * Enter the Jenkins Server URL
 * Enter the user ID in the User ID field
 * Enter the Jenkins password in the Password field

 .. image:: /images/updated_img/createJenkins.png

 * Click Save button
 * Now Jenkins is successfully configured to RLCatalyst


**Hereby attaching a video which will demonstrate as in how to Create Jenkins in RLCatalyst:**


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/99m0sGvnIiw" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****

.. _provider-settings:


Providers
^^^^^^^^^

RLCatalyst supports infra automation across providers like AWS, Azure, VMware, Openstack. Each provider needs to be configured with the proper credentials amd other required details before it can be used. 

You can configure multiple cloud provider accounts  of type **AWS**, **AZURE**, **OPEN STACK** and **VMWARE** within RLCatalyst.

To configure the Providers setup follow the steps below:

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Devops Setup
 * Click on Providers
 * Click on New button provided 
 * Select the provider from the Provider Type drop down list (e.g. AWS)
 * Enter the name of the provider in the name field

 * To add **AWS** Provider Account

RLCatalyst supports 2 types of authentication into the AWS account. 

**IAM Role** - RLCatalyst supports authentication using IAM roles, in cases when user doesnt want to enter secret keys and access keys. This requires the RLCatalyst instances to be on AWS and is launched with an IAM role. The credentials will be acquired by rlcatalyst from its instance metadata . Only such provider account can be added per orgnaization in the current version of RLcatalyst . All AWS API requests made from catalyst by the default provider will be signed with security credentials fetched from instance metadata.

**Prerequisites** - 
RLCatalyst should be deployed on an AWS instance. This AWS instance should be launched with an IAM role with permissions to launch EC2 instances and CFTs. Also, new instances from rlcatalyst can only be launched in the same AWS account in which catalyst is running. 

Refer to http://docs.aws.amazon.com/AWSSdkDocsJava/latest/DeveloperGuide/java-dg-roles.html for more details

To choose this mode, unselect the checkbox **Requires Access Credentials**

**Secret key and Access key** - This method requires the access key and secret key to authenticate access to the AWS provider account. 

To choose this mode select the  checkbox **Requires Access Credentials**

    * Provide the access key  in the Access Key field     
    * Provide the secret key in the Secret Key field
    * Provide the bucket name in the S3 Bucket Name field
    * Select the organization from the Organization drop down list
    * Select the region from the Region drop down list where your provider is located
    * Select the key pair for the provider from the Key Pair drop down list
    * Upload the .pem file for Provider
    
 
     .. image:: /images/updated_img/createProvider.png

    
    * Click on Save button

    * Now Provider is successfully configured to RLCatalyst


* To add **Azure** Provider Account

    * Provide the Subscription ID
    * Provide the Client ID
    * Provide the Client Secret Key
    * Provide the Tenant ID
    * Upload the Pem file
    * Upload the private Key file
    * Select the organization from the Organization drop down list
    * Click on Save button
    * Now Provider is successfully configured to RLCatalyst

  


* To add **OpenStack** Provider Account
 
    * Provide the Username
    * Provide the password
    * Provide the Host
    * Provide the Project name
    * Provide the Tenant ID
    * Provide the Tenant Name
    * Provide the Compute Service Endpoint
    * Provide the Identity Service Endpoint
    * Provide the Network Service Endpoint
    * Provide the Image Service Endpoint
    * Provide the Instance key Name
    * Upload the pem file for Instance
    * Select the organization from the Organization drop down list
    * Click on Save button
    * Now Provider is successfully configured to RLCatalyst



* To add **VMWare** Provider Account
 
    * Provide the Username
    * Provide the password
    * Provide the Host
    * Enter the DC
    * Select the organization from the Organization drop down list
    * Click on Save button
    * Now Provider is successfully configured to RLCatalyst
 

 

**Hereby attaching a video which will demonstrate as in how to Create Providers in RLCatalyst:**


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/FnpU1fFCe-Y" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****



**Provider Sync for AWS**

Provider sync allows you to import unmanaged instances to Catalyst. 

Follow the below steps for AWS provider sync:


* Create an **AWS** provider as shown above. The Created provider will be available in Providers page

 .. image:: /images/updated_img/createAWS.png


* Click on the Sync Instance button of the provider.

    1. Tags: you have two sections, left side you will get the tags which are present in ur AWS acccount will shown here and you can add description for your refrence only. And right side you can map the tags with PROJECT ans ENVIRONMENT, Specify which tags represent project name and the environment name. Once you will save it, you can see the refelection in Mapping tab.

    .. image:: /images/updated_img/providers.png


    2. Mappings: In Mapping, all the mapped Tag Values would be visible with respect to Projects and Environment. Select one tag name for project from drop down as well as Environment tag name for Environment And save the changes. Now go to Instances tab.

    .. image:: /images/updated_img/mapping.png



    3. Instances: You have 3 catalyst status:

        * Managed: If catalyst status is ‘Managed’, you will get all “Bootstraped successfull Instances”. You can delete the instances from here.
        * Assigned: If you want to assign some unassigned Instance then you have to update tags corresponding to the mapping.
        * Unassigned: Here you will get all other Instances available in your AWS account. Here you can update the tags value by selecting the node.

        **Unassigned Instances**:

        .. image:: /images/updated_img/unassignedInstances.png

        **Assigned Instances**:

        .. image:: /images/updated_img/assignedInstance.png

        **Managed Instances**:

        .. image:: /images/updated_img/managedInstances.png


    4. RDS: Amazon Relational Database Service (Amazon RDS) is a web service that makes it easier to set up, operate, and scale a relational database in the cloud. It provides cost-efficient, resizeable capacity for an industry-standard relational database and manages common database administration tasks.

        **Unassigned RDS**:

        .. image:: /images/updated_img/unassignedRDS.png

        **Assigned RDS**:

        .. image:: /images/updated_img/assignedRDS.png

    5. S3: A bucket is a logical unit of storage in Amazon Web Services (AWS) object storage service, Simple Storage Solution S3. Buckets are used to store objects, which consist of data and metadata that describes the data.
    It is the account bucket name, where we store all the information regarding AWS Provider like instances cost and usage.


        .. image:: /images/updated_img/unassignedS3.png

 
        .. image:: /images/updated_img/S3.png


**Following video demonstrates how to do provider sync in RLCatalyst**:


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/rhYHxpH0vPM" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

*****

CMDB
^^^^

A configuration management database (CMDB) is a repository that acts as a data warehouse for information technology (IT) installations. It holds data relating to a collection of IT assets (commonly referred to as configuration items (CI)), as well as to descriptive relationships between such assets.To configure the CMDB setup follow the steps below:

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on DevOps Setup
 * Click on CMDB
 * Click on New button provided 
 * Select the Organization to which the Jenkins server will be attached to
 * Enter the name in the Name field
 * Enter the Jenkins Server URL
 * Enter the user ID in the User ID field
 * Enter the Jenkins password in the Password field

 .. image:: /images/updated_img/createJenkins.png

 * Click Save button
 * Now Jenkins is successfully configured to RLCatalyst