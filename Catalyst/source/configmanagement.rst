


Puppet Server
^^^^^^^^^^^^^


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

**Hereby attaching a video which will demonstrate as in how to Create Puppet**:


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/sqQ8dRWnWKI" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

*****

.. _configure-nexus:

Nexus Server
^^^^^^^^^^^^
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

**Hereby attaching a video which will demonstrate as in how to Create Nexus**:


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/OWjg9h4vdKA" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****



Configure Docker
^^^^^^^^^^^^^^^^

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

**Hereby attaching a video which will demonstrate as in how to Create Docker**:


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/PTKKXE4dAxk" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****

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


**Hereby attaching a video which will demonstrate as in how to Create Jenkins**:


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/uoMmBnUhYjE" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****

Providers in RLCatalyst
^^^^^^^^^^^^^^^^^^^^^^^^

You can configure multiple cloud provider accounts  of type AWS, AZURE, OPEN STACK and VMWARE within RLCatalyst.To configure the Providers setup follow the steps below:

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Devops Setup
 * Click on Providers
 * Click on New button provided 
 * Select the provider from the Provider Type drop down list (e.g. AWS)
 * Enter the name of the provider in the name field
 * To add AWS Provider Account

 	* Provide the access key  in the Access Key field 	
 	* Provide the secret key in the Secret Key field
 * To add Azure Provider Account
 * To add OpenStack Provider Account
 * To add VMWare Provider Account
 * Select the organization from the Organization drop down list 
 * Select the region from the Region drop down list where your provider is located
 * Select the key pair for the provider from the Key Pair drop down list
 * Upload the .pem file for Provider

 .. image:: /images/createProvider.JPG

 * Click on Save button
 * Now Provider is successfully configured to RLCatalyst


**Hereby attaching a video which will demonstrate as in how to Create Providers**:


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/Z1I3PEn9QVs" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>
