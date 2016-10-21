


.. _conf-settings:


Chef Server
^^^^^^^^^^^
The Chef server acts as a hub for configuration data. The Chef server stores cookbooks, the policies that are applied to nodes, and metadata that describes each registered node that is being managed by the chef-client.

A node is any machine—physical, virtual, cloud, network device, etc.—that is under management by Chef.

A cookbook is the fundamental unit of configuration and policy distribution.

A policy file allows you to specify in a single document the cookbook revisions and recipes that should be applied by the chef-client.


RLCatalyst allows you to configure your own chef server. You can add either a hosted chef server or an on-premise installation of chefserver. If you dont have either of these, please create an account at https://getchef.opscode.com/signup . For more details on chef, please go to :doc:`Chef Setup <chefsetup>` . 

In RLCatalyst only one chef server can be configured for one organization. The same chef server cannot be associated to multiple organizations. Each chef server account will have a URL(Hosted/On-Premise), a User pem file, a Validator pem file and a knife file . You will get all these files when you create accounts in Chef.

Data/File needed for adding a Chef Server account in RLCatalyst

 * Name : Alias or name of the chef server , to be identified in RLCatalyst
 * User Name : User name of your chef server account
 * URL : URL of the hosted or on-premise chef server
 * User Pem File : User file to access your Chef Server account
 * Knife.rb : Configuration file that you get while setting up the Chef server
 * Validator Pem File : During the first chef-client run, this private key does not exist. Instead, the chef-client will attempt to use the private key assigned to the chef-validator, located in /etc/chef/validation.pem.
 * Key File : It is used to encrypt the contents of the data bag item.
 * Template File :  The default bootstrap operation relies on an Internet connection to get the distribution to the target node. If a target node cannot access the Internet, then a custom template i.e, template file can be used to define a specific location for the distribution so that the target node may access it during the bootstrap operation.

To configure a new chef server follow the steps below:

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Config Setup
 * Click on Chef Server
 * Click on New button provided 
 * Enter the configuration name in the Name field
 * Enter the Chef user name in User Name field
 * Provide or specify the Chef URL for the server to be configured
 * Choose the organization from the Organization drop down list
 * Upload the user PEM file provided by the Chef Server in the User PEM File field
 * Upload the validator PEM file provided by the Chef Server in the Validator PEM File field
 * Upload the Knife.rb file provided by the Chef Server in the Knife.rb File field
 * Upload the key file which is used for Databag
 * Upload the Template file which is used to Bootstrap node


 .. image:: /images/updated_img/createChefServer.png



 Through Setup & Configuration Wizard:


 .. image:: /images/updated_img/createChefServer01.png


 * Click on Save button 
 * Now your chef server is configured successfully and listed in the Chef server management page.

 .. image:: /images/updated_img/chefServer.png

*****

**Edit and Remove Chef Server configuration**
 You can edit and remove a chef server configuration.


To Edit the Chefserver
 * Click on edit button to edit chef server configuration details

To Remove the Chefserver
 * Click on delete button to remove chef server configuration from the list

**Following video demonstrates how to configure a chef server in RLCatalyst:**


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/qwCu-xx-wcA" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

*****

**Import nodes from Chef Server**

You can import existing nodes from the configured chef server into RLCatalyst by selecting the required Business Group and Project. These imported nodes can be operated from the Workzone.

 * To import the existing nodes click on import button  
 * Select the environment from Environment drop down list for the node to be imported . These are the environments available in your Chef account
 * Select the respective checkbox in the Action column

 .. image:: /images/updated_img/chefImport.png

*****

 * Click on the Import Nodes button 
 * Select the business group from Business Group drop down list
 * Select the project from the Project drop down list
 * Enter the user name to access the chef server for import in the User Name field 
 * Choose authentication type from the Choose Authentication Type drop down list. RLCatalyst provides two types of authentication, you can either choose Password or by uploading the PEM file
 * Type Password or upload PEM file
 * Click on Import button
 * Close the popup containing the success message 'Node imported'
 * Click on Workzone
 * The imported node will be available in the respective Environment of the Workzone

*****

**Chef Factory**
 It consists of common and re-usable recipes and cookbooks.

 * Click on Chef factory icon present in the Action column , Chef factory page will open.

 .. image:: /images/updated_img/chefFactory.png

 * Go to Sync tab, here all the cookbooks and roles which are present in the chef server will be listed.

 .. image:: /images/updated_img/chefCookbooks.png

 * Select the Cookbook and click on Sync
 * Close the popup window
 * Go to Cookbooks tab, here you can find the downloaded (Synched) cookbook

 .. image:: /images/updated_img/chefFactoryActions.png

*****


**Databags and Items for Chef server**

A data bag is a global variable that is stored as JSON data and is accessible from a Chef server.A data bag is indexed for searching and can be loaded by a recipe or accessed during a search.

A data bag item may be encrypted using shared secret encryption. This allows each data bag item to store confidential information (such as a database password) or to be managed in a source control system (without plain-text data appearing in revision history). Each data bag item may be encrypted individually; if a data bag contains multiple encrypted data bag items, these data bag items are not required to share the same encryption keys.


How to create Databag and Items for Chef Server?

 * In the Chef Server Page, Click on Databag icon in the Action column of your chef server
 * Click on + icon above the List of Data Bags column header

 .. image:: /images/updated_img/databag.png

*****

 * Enter the name of the Databag in the Name field


 .. image:: /images/updated_img/createDatabag.png

*****

 * Click on Save button
 * Select the Created Databag and create an item by clicking + icon above the 'Items for -Databagname' column header
 * Enter the ID and Item body

 .. image:: /images/updated_img/createDatabagItem.png

*****

 * Select the checkbox Do you want to Encrypt
 * Click on Save button
 * Now Databag and its item is created. Item body is shown in last column
 * Click on Close button to navigate back to Chef server management page

*****


Puppet Server
^^^^^^^^^^^^^

Puppet Server is an application that runs on the Java Virtual Machine (JVM) and provides the same services as the classic Puppet master application. It mostly does this by running the existing Puppet master code in several JRuby interpreters, but it replaces some parts of the classic application with new services written in Clojure.

If you are using Puppet for your configuration management requirements, configure it in RLCatalyst. You can configure only one puppet server for one organization. Same puppet server cannot be associated with multiple organizations. 

To configure a new puppet server follow the steps below:

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Config Setup
 * Click on Puppet Server
 * Click on New button provided 
 * Enter the puppet server name in the Name box
 * Enter the user name in User Nane field
 * Enter the Hostname in Host Name field
 * Choose the organization from the Organization drop down list
 * Choose the Authentication by selecting Password / Pem file
 * Enter Password / Upload the pem file

 .. image:: /images/updated_img/createPuppet.png


 * Click on Save button
 * Now your Puppet server is configured and listed in the Puppet Server Management page

 .. image:: /images/updated_img/puppetList.png

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


.. _env-settings:

Environments
^^^^^^^^^^^^

In an Organization you can create multiple Environments. These environments need to be linked to Projects back. For example: Production, Development, Testing and so on. 

Follow the steps to setup a new Environment in an Organization:

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Organization Setup
 * Click on Environments
 * Click on New button provided
 * Select the Organization from the Organization drop down list
 * Select the server from the Chef Server drop down list
 * You can see a list of environments in the drop down. These are the environments defined in your chef server account. You can select one from this  drop down list **OR** you can Add new Environments to chef server by clicking on **Add** link provided right above the select an Chef Environment drop down
 * Now Enter the Environment name to be created

 .. image:: /images/updated_img/addNewEnv.png

*****

 * Click on Add button
 * Now select the environment you added to the chef server from the Chef Environment drop down list

 .. image:: /images/updated_img/createEnv.png

*****

 * Assign the project by toggling to 'Yes'
 * Click on Save button.
 * Now the environment is setup and listed in the Environments page

 .. image:: /images/updated_img/env.png
 
*****


**Hereby attaching a video which will demonstrate as in how to Create Environment in RLCatalyst:**


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/LBPj6psKfsw" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****