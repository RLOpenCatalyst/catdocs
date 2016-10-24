
.. _provider-settings:


Providers
^^^^^^^^^

RLCatalyst supports infra automation across providers like AWS, Azure, VMware, Openstack. Each provider needs to be configured with the proper credentials amd other required details before it can be used. 

You can configure multiple cloud provider accounts  of type **AWS**, **AZURE**, **OPEN STACK** and **VMWARE** within RLCatalyst.

To configure the Providers setup follow the steps below:

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Provider Configuration
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

    1. Tags: you have two sections, left side you will get the tags which are present in ur AWS acccount will shown here and you can add description for your refrence only. And right side you can map the tags with Business Group, Project and Environment, Specify which tags represent Business Group, project name and the environment name. Once you will save it, you can see the refelection in Mapping tab.

    .. image:: /images/updated_img/providers.png

    

    2. Mappings: In Mapping, all the mapped Tag Values would be visible with respect to Business Group, Projects and Environment. Select one tag name for Business Group, project from drop down as well as Environment tag name for Environment And save the changes. Now go to Instances tab.

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

        **Assigned S3**:
 
        .. image:: /images/updated_img/S3.png


**Following video demonstrates how to do provider sync in RLCatalyst**:


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/rhYHxpH0vPM" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

*****

.. _configure-vm:

VM Images
^^^^^^^^^

An image of a virtual machine is a copy of the VM, which may contain an OS, data files, data to be installed on multiple VMs and applications.It is usually tested for security, reliability and has the best tested conflagrations.

**Adding a New VMImage**

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Provider Configuration
 * Click on VMImages
 * Click on New button provided  
 * Enter the image name in the Name field
 * Select the organization from the Organization drop down list
 * Choose the provider from the Choose Provider drop down list
 * Select the operating system type from the Operating System drop down list
 * Provide the image identifier name in the Image ID field
 * Provide the admin user name in the Admin User Name field
 * Provide the admin password in the Admin Password field
 * Click on Save button

 .. image:: /images/createVM.JPG


 * Now new VM Image is added and available in the VM Image list

**Hereby attaching a video which will demonstrate as in how to Create VM Images in RLCatalyst:**


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/0ciDKco_WF8" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

*****


**How to add Windows VMImage?**
 Before onboading Windows nodes into RLCatalyst, we need to ensure that WinRM is configured on the windows guest node, the two ports 5985 & 5986 are opened for communication between RLCatalyst and node.

 The settings below must be added to your base server image or passed in using some sort of user-data mechanism provided by your cloud provider. 

**Steps (To be performed from a windows host):**

1. Use remote desktop to connect to the node (Start->Run->MSTC).

2. Provide the IP Address / Host name of the node along with the username and password.

3. Once connected to the node,

 a. Open / Run powershell as an administrator

 b. Execute the below commands (you could copy and paste all the commands together)

    winrm quickconfig -q

    winrm set winrm/config/winrs '@{MaxMemoryPerShellMB="300"}'

    winrm set winrm/config '@{MaxTimeoutms="1800000"}'

    winrm set winrm/config/service '@{AllowUnencrypted="true"}'

    winrm set winrm/config/service/auth '@{Basic="true"}'

    winrm set winrm/config/client/auth '@{Basic="true"}'

    netsh advfirewall firewall add rule name="WinRM 5985" protocol=TCP dir=in 

    localport=5985 action=allow

    netsh advfirewall firewall add rule name="WinRM 5986" protocol=TCP dir=in 

    localport=5986 action=allow

    net stop winrm

    Set-Service WinRm -StartupType Automatic

    net start winrm

 **Note:** Press enter to execute the last command, if you have copy - pasted the above commands.

4. To create an image from this node, follow the instructions given by the cloud service provider for image creation.

 a. Remember to create a local admin user before generating an image, as image generation wipes out existing administrator account, which will be manageable only from the server's console and not remotely.

 b. Install all necessary updates before creating the image.

 c. Use the Windows sysprep utility to create the image. 

 d. Details about using the sysprep utility can be found here (https://technet.microsoft.com/en-in/library/hh824938.aspx)




*****