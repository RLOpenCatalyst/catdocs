


.. _org-settings:


Organization
^^^^^^^^^^^^

An Organization can be an enterprise or a business that can have multiple sub groups and projects.

**Follow the steps below to create an organization**

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Organization Setup
 * Click Organizations
 * Click on New button provided 
 * In Create Organization page enter Name (Organization Name) and Domain Name (Website Address)

 .. image:: /images/updated_img/createOrg.png


 * Click on Save button
 * Now your Organization is setup and listed in the Organizations page

 .. image:: /images/updated_img/org.png



**Edit and Remove an Organization**
 You can edit and remove an Organization.

To Edit the Organization
 * Click on edit button to edit the organization details

To Remove the Organization
 * Click on delete button to remove the organization from the list


**Activate or Inactivate an Organization**

You can activate or inactivate an Organization by using the cursor button provided.  Remember, once you inactivate the organization all the entities relating to that organization will be disabled. You can enable the organization at any time. which will activate all the entities associated with that organization

 .. image:: /images/updated_img/editOrg.png

 
.. _bu-settings:

Business Groups
^^^^^^^^^^^^^^^
**Setup Business Groups for an Organization**

In an Organization you can create multiple Business Groups. A Business Groups can be a business division in your organization

**Follow the steps below to create a new Business Group in an Organization**

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Organization Setup
 * Click on Business Groups
 * Click on New button provided 
 * Enter the Business Group name in the Business Group name field
 * Select the Organization from the Organization drop down list
 * Click on Save button

 .. image:: /images/updated_img/editBG.png

 * Now the Business Group  is setup and listed in the Business Groups page


 .. image:: /images/updated_img/BG.png

**Edit and Remove a Business Group**
 You can edit and remove a Business Group.

To Edit the Business Group
 * Click on edit button to edit Business Group details

To Remove the Business Group
 * Click on delete button to remove Business Group from the list 

 


.. _projects-settings:

Projects
^^^^^^^^

**Setup Projects for a Business Group**

In a Business Group you can create multiple Projects. A Project in RLCatalyst can be a running project in your business group. Each project can run one or multiple applications

**Follow the steps below to create a new Project associating with Business Group and Organization**

 * From the main menu click on Settings
 * Once you click on Settings, from the side menu click on Organization Setup
 * Click on Projects
 * Click on New button provided 
 * Enter the Project name in the Name field
 * Provide a brief description about the project in the Description field
 * Select the Organization from the Organization drop down list
 * Select the Business Group from the Business Group drop down list
 * Environments and repository details are not mandatory while creating project and will be explained in later section

 .. image:: /images/updated_img/createProject.png

 * Click on Save button

 .. image:: /images/updated_img/project.png

**Edit and Remove a Project**
 You can edit and remove a Project.

To Edit the Project
 * Click on edit button to edit Project details

To Remove the Project
 * Click on delete button to remove Project from the list



**The following video will help you to setup an Organization, BusinessGroup, Project in RLCatalyst:**


.. raw:: html

	
	<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/khifxeCjPAw" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



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
