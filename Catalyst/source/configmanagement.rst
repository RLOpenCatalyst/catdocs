


Puppet Server
^^^^^^^^^^^^^

Puppet Server is an application that runs on the Java Virtual Machine (JVM) and provides the same services as the classic Puppet master application. It mostly does this by running the existing Puppet master code in several JRuby interpreters, but it replaces some parts of the classic application with new services written in Clojure.

If you are using Puppet for your configuration management requirements, configure it in RLCatalyst. You can configure only one puppet server for one organization. Same puppet server cannot be associated with multiple organizations. 

To configure a new puppet server follow the steps below:

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Devops Setup
 * Click on Puppet Server
 * Click on New button provided 
 * Enter the puppet server name in the Name box
 * Enter the user name in User Nane field
 * Enter the Hostname in Host Name field
 * Choose the organization from the Organization drop down list
 * Choose the Authentication by selecting Password / Pem file
 * Enter Password / Upload the pem file

 .. image:: /images/createPuppet.JPG


 * Click on Save button
 * Now your Puppet server is configured and listed in the Puppet Server Management page

 .. image:: /images/puppetList.JPG

*****

**Import nodes from Puppet Server**

You can import existing nodes from the configured puppet server into RLCatalyst by selecting the required Business Group and Project. These imported nodes can be operated from the Workzone.

 * To import the existing nodes click on Import button
 * Select the node and the respective Environment for the dropdown 
 * Select the environment from Environment drop down list for the node to be imported
 * Select the respective checkbox in the Action column
 * Click on the Import Nodes button 
 * Select the business group from Business Group drop down list
 * Select the project from the Project drop down list
 * Enter the user name to access server for import in the User Name box 
 * Choose authentication type from the Choose Authentication Type drop down list. RLCatalyst provide two types of authentication, you can either choose Password or by uploading the PEM file
 * Type Password or upload PEM file 
 * Click on Import button
 * Close the popup containing the success message 'Node imported'
 * The imported node will be available in the respective Environment of the Workzone


 **Note**: For the imported node using puppet server , Puppet client run icon will be shown.

**Hereby attaching a video which will demonstrate as in how to Create Puppet in RLCatalyst:**


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/5YtNPCHEgg4" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

*****

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

 .. image:: /images/nexusDetails.png



 * Click on Save button
 * Now the Nexus server setup is ready and listed in the Nexus Server page

 .. image:: /images/nexusList.JPG

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


Configure Docker
^^^^^^^^^^^^^^^^

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

 .. image:: /images/createDocker.JPG

 * Click Save button
 * Now Docker is successfully configured to RL Catalyst

**Hereby attaching a video which will demonstrate as in how to Create Docker in RLCatalyst:**


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/MYjKmgLpO7c" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****


.. _Configure-Jenkins:

Configure Jenkins
^^^^^^^^^^^^^^^^^

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

 .. image:: /images/createJenkins.JPG

 * Click Save button
 * Now Jenkins is successfully configured to RLCatalyst


**Hereby attaching a video which will demonstrate as in how to Create Jenkins in RLCatalyst:**


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/99m0sGvnIiw" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****

.. _provider-settings:


Providers in RLCatalyst
^^^^^^^^^^^^^^^^^^^^^^^^

Provider is used to interact with the many resources supported by AWS,AZURE,OPEN STACK,VMWARE. The provider needs to be configured with the proper credentials amd other required details before it can be used.

You can configure multiple cloud provider accounts  of type **AWS**, **AZURE**, **OPEN STACK** and **VMWARE** within RLCatalyst.

To configure the Providers setup follow the steps below:

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Devops Setup
 * Click on Providers
 * Click on New button provided 
 * Select the provider from the Provider Type drop down list (e.g. AWS)
 * Enter the name of the provider in the name field

 * To add **AWS** Provider Account

 	* Provide the access key  in the Access Key field 	
 	* Provide the secret key in the Secret Key field
 	* Select the organization from the Organization drop down list
 	* Select the region from the Region drop down list where your provider is located
 	* Select the key pair for the provider from the Key Pair drop down list
 	* Upload the .pem file for Provider
    
 
     .. image:: /images/createProvider.PNG

    
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

.. _provider-sync:

Provider Sync for AWS
^^^^^^^^^^^^^^^^^^^^^

Provider sync allows you to import unmanaged instances to Catalyst. Once you import your node to catalyst appliaction it will bootstrap and will be displayed in Managed instances tab.

**Managed Instance** means Node which has been bootstrapped by Catalyst and **Unmanaged instances** means Node which has not been bootstrapped by catalyst.

Follow the below steps for AWS provider sync:


* Create an **AWS** provider as shown above. The Created provider will be available in Providers page

 .. image:: /images/createAWS.jpg


* Click on the Sync Instance button of the provider.


* Click on UnManaged instances tab
 
 .. image:: /images/unManagedIns.PNG

* Select the Instance with the Action to be imported

 .. image:: /images/selectInstance.PNG


* Click on Import Instances button 

 .. image:: /images/importIns.PNG


* A pop up is displayed with the message "Instance Imported"

 .. image:: /images/instanceImported.PNG


* Verify the Node is imported in the Environment

 .. image:: /images/verfiyNode.PNG


* Click on Control panel -> Action History and Wait until the Bootstrap succeeds

 .. image:: /images/bootstrapSuccess.PNG


Now click on Back to Instances Tab

* Go to Settings -> Devops Setup -> Providers and click on Sync Instances button
The Bootstrapped node will be displayed under Managed Instances tab

 .. image:: /images/managedInstances.PNG




**Following video demonstrates how to do provider sync in RLCatalyst**:


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/rhYHxpH0vPM" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

*****








