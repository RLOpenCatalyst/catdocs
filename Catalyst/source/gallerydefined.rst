



.. _configure-softwarestack:

Templates
^^^^^^^^^

Templates are user defined skeleton structure which helps the user to add Cookbooks,Roles which in turn leads to create Blueprints.

**Adding a New Template For Software Stack Template Type**

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Gallery Setup
 * Click on Templates
 * Click on New button provided 
 * Enter the template name in the Template Name field
 * Upload an Icon by clicking on the Browse button.
 * Choose the template type 'Software Stack' from the Template Type drop down list
 * Choose the Organization from the Organizationdrop down list
 * Select the Cookbooks from left frame and Click the arrow button to add to the Order Runlist. You can deselect the selected Cookbooks from the Order Runlist by clicking the arrow button to the Select Runlist box again
 * You can customize the order of Order Runlist. First select the item and then use the up and down arrows provided to change the order of the Order Runlist.

 .. image:: /images/createTemplate.JPG

 * Now new template is added and available in the Templates list

*****


.. _configure-docker:

**Adding a New Template For Docker Template Type**

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Gallery Setup
 * Click on Templates
 * Click on New button provided 
 * Provide a template name in the Template Name field
 * Upload an Icon by clicking on the Browse button.
 * Choose the template type 'Docker' from the Template Type drop down list
 * Choose the Organization from the Organizationdrop down list
 * Choose the Docker repo
 * Enter the Title
 * Add Docker Repo Path
 * Click on Add button

 .. image:: /images/dockerTemplate.JPG

 * Click on Save button

 * Now new template is added and available in the Templates list


**Hereby attaching a video which will demonstrate as in how to Create Templates**:


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/rMBCRLRkeHs" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****

**Adding a New Template For Cloud Formation Template Type**

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Gallery Setup
 * Click on Templates
 * Click on New button provided 
 * Enter the template name in the Template Name field
 * Upload an Icon by clicking on the Browse button
 * Choose the template type 'CloudFormation from the Template Type drop down list
 * Choose the Organization from the Organizationdrop down list
 * Browse the Template File
 * Click on Save button

 .. image:: /images/cftTemplate.JPG

 * Now new template is added and available in the Templates list
*****


VM Images
^^^^^^^^^

An image of a virtual machine is a copy of the VM, which may contain an OS, data files, data to be installed on multiple VMs and applications.It is usually tested for security, reliability and has the best tested conflagrations.

**Adding a New VMImage**

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Gallery Setup
 * Click on VMImage
 * Click on New button provided  
 * Enter the image name in the Name field
 * Select the organization from the Organization drop down list
 * Choose the provider from the Choose Provider drop down list
 * Select the operating system type from the Operating System drop down list
 * Provide the image identifier name in the Image ID field
 * Provide the admin user name in the Admin User Name field
 * Click on Save button

 .. image:: /images/createVM.JPG


 * Now new VM Image is added and available in the VM Image list

**Hereby attaching a video which will demonstrate as in how to Create VM Images**:


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/dC3Ve-Ihz2I" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****


Service Command
^^^^^^^^^^^^^^^

Service Commands helps user to create a service associated with cookbooks which can run on the instance with the following actions **Start**, **Stop** and **Restart**.

**Adding a new Service Command**

 * From the main menu click on Settings

 * Once click on Settings, from the side menu click on Gallery Setup

 * Click on Service Command

 * Click on New button provided 

 * On Create Services page Select Organization, Enter Name, Choose Service Command Type as Chef Cookbook/Recipe , Select Chef Server, Service cookbooks as 'service_apache'.

 * Select the Actions.

 .. image:: /images/createService.png


 * Click on Save button

 * Now your Service Command is setup and listed in the Services Page
 
 .. image:: /images/services.png



**Go to Workzone and Launch or Import a Node**

 .. image:: /images/nodeApache.png


 * Click on Chef Client run icon , add Apache2 cookbook to the runlist and click Update button. Wait until chefclient is success.

 .. image:: /images/updateRunlist.png 

 * When apache2 cookbook run successfully by default service will be running.Click on SSH icon and execute **sudo service apache2 status** command and verify apache2 is running.

 .. image:: /images/sshTerminal.png 


 * Close the SSH window
  
 * Go to Instance control panel

 * Go to Services tab and add the apache service and click on Save button

 .. image:: /images/addService.png


 * Service is added to the Instance and Start,Stop and Restart buttons will be shown

 .. image:: /images/controPanel.png

 * Click on Stop button (Red color) and wait until it succeeds

 * Click on SSH icon

 * Execute command **sudo service apache2** status and verify apache2 is not running

 .. image:: /images/serviceStatus.png






 





 




