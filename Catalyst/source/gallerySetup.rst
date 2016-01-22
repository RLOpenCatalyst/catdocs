Gallery Setup
^^^^^^^^^^^^^

**The Gallery Setup option in RL Catalyst provides you two options**:

 * Templates:  You can create different templates in RL Catalyst for all supported Cookbooks. You can also add new templates for newly added Cookbooks. To know more on what is a Cookbook please click: http://docs.chef.io/cookbooks.html

 * Service Command: Service command allows you to setup the service running options. You can choose between Chef Cookbooks based services and System service based commands. 

 * VM Image:  You can create multiple VM Images in RL Catalyst. RL Catalyst allows you create multiple VM images which is independent of Operating System.

*****

**Adding a New Template For Software Stack Template Type**

 * From the main menu click on Settings
 * Once click on Settings, from the side menu click on Gallery Setup
 * Click Templates
 * Click on +New button provided 
 * Provide a template name in the Template Name box
 * Upload an Icon by clicking the Browse button.
 * Choose a template type 'Software Stack' from the Template Type drop down list
 * Choose the Organization from the Organizationdrop down list
 * Select the Cookbooks from left frame and Click the arrow button to add to the Order Runlist. You can deselect the selected Cookbooks from the Order Runlist by clicking the arrow button to the Select Runlist box again
 * You can customize the order of Order Runlist. First select the item and then use the up arrow and down arrow provided to change the order of the Order Runlist.

 .. image:: /images/createTemplate.JPG

 * Now new template is added and available in the Templates list

*****

**Adding a New Template For Docker Template Type**

 * From the main menu click on Settings
 * Once click on Settings, from the side menu click on Gallery Setup
 * Click Templates
 * Click on +New button provided 
 * Provide a template name in the Template Name box
 * Upload an Icon by clicking the Browse button.
 * Choose a template type 'Docker' from the Template Type drop down list
 * Choose the Organization from the Organizationdrop down list
 * Choose the Docker repo
 * Enter the Title
 * Add Docker Repo Path
 * Click on Add button

 .. image:: /images/dockerTemplate.JPG

 * Click on Save button


**Hereby attaching a video which will demonstrate as in how to Create Templates**:


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/rMBCRLRkeHs" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****

**Adding a New Template For Cloud Formation Template Type**

 * From the main menu click on Settings
 * Once click on Settings, from the side menu click on Gallery Setup
 * Click Templates
 * Click on +New button provided 
 * Provide a template name in the Template Name box
 * Upload an Icon by clicking the Browse button
 * Choose a template type 'CloudFormation from the Template Type drop down list
 * Choose the Organization from the Organizationdrop down list
 * Browse the Template File
 * Click on Save button

 .. image:: /images/cftTemplate.JPG

*****

**Adding a New VMImage**

 * From the main menu click on Settings
 * Once click on Settings, from the side menu click on Gallery Setup
 * Click VMImage
 * Click on +New button provided  
 * Provide an image name in the Name box
 * Choose the provider from the Choose Provider drop down list
 * Select the operating system type from the Operating System drop down list
 * Provide the image identifier name in the Image ID box
 * Provide the admin user name in the Admin User Name box
 * Select the organization from the Organization drop down list
 * Click Save button
 * The new VM Image is added to the list

 .. image:: /images/createVM.JPG

**Hereby attaching a video which will demonstrate as in how to Create VM Images**:


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/dC3Ve-Ihz2I" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****

**How to add a new Service Command**

 * From the main menu click on Settings
 * Once click on Settings, from the side menu click on Gallery Setup
 * Click Service Command
 * Click on +New button provided 
 * Enter a name for the service in the Name box
 * Choose the Service Command Type from the drop down list. You can service between a Chef Cookbook /Recepie or system Service Command
 * If you choose Chef Cookbook /Recepie command
    a. Select the server from the Chef Server drop down list
    b. Select the Cookbooks from the Service Cookbooks drop down list
    c. Select the action that’s needs to be run on the service. You can use the default or packages option to run the service. (Start, Stop, Restart and Status are the options provided for running the service)

    a. Select the operating system from the Choose Operating System drop down list
    b. Enter the command in the Command box, for e.g. Apache
    c. Select the action that’s needs to be run on the service. (Start, Stop, Restart and Status are the options provided for running the service).
 
 * Click Save button
 * Now the Service Command is added to the Services list.

*****

**How to Edit or Remove a Service**

You can edit or remove a Service. Follow the steps below.
 
 * Click on edit button to edit a service from the Services list
 * Click on delete button to remove a service from the Services list

