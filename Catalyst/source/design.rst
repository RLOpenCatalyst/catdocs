Design
======

User defined Blueprints can be created in the Design section associated with the respective **providers** and **Template Types**.

**Blueprints** are predefined templates which can be used by service consumers to Launch the instances. Blueprints are designed by Service Designers. Each blueprint stores the metadata of the instance, variables, actions and activity.

RL Catalyst Design options allows you to create Blueprints by using predefine templates.

**Creating BluePrints for Sofware Stack Template Type** using AWS provider

Blueprints are predefined templates which can be used by service consumers to launch the instances. Blueprints are designed by service designers. 
Each blueprint stores the metadata of the instance, variables, actions and activity. Follow the steps for creating BluePrints.

 * From the Design page choose a Software Stack Template Type and click Next

 .. image:: /images/templateTypeList.JPG

 * From the Template cards choose template and click Next

 **NOTE -** If you have not created a template of Software Stack template type in Settings, follow the instructions at :ref:`configure-softwarestack`.

 .. image:: /images/templateList.JPG

 * Once you choose the Template, Enter the details for creating the BluePrint

 a. In the Configure Providers Parameters option,  choose the operating system from Choose Operating System drop down list
 b. Choose the provider from the Choose Provider drop down list
 c. Choose the image that you want to use from the Choose Available Images drop down list
 d. Choose the region from the Choose Region drop down list
 e. Choose the VPC from the Select VPC drop down list
 f. Choose the subnet from the Select Subnet drop down list
 g. Choose the key pair from the Select Key Pair drop down list
 h. Choose the instance size from the Select Instant Size drop down list
 i. Choose the security group from the Choose Security Group drop down list

 .. image:: /images/bpCreation.png

 j. In the Configure Organization Paramteres option, Choose the Organization, Enter blueprint name, Choose Business group and Project names
 k. In the Configure Runlist Parameter  option, Click on +  icon (Edit Runlist), select the Cookbooks from the left frame and Click the arrow button to add to the Runlist. You can deselect the selected Cookbooks from the Order Runlist by clicking the arrow button to the Select Runlist box again
 l. You can customize the order of Order Runlist. First select the item and then use the up arrow and down arrow provided to change the order of the Order Runlist
 m. Click on Update runlist button

 .. image:: /images/runlistUpdate.JPG

 n. In the Configure Application URL option, you can view the application URL available for the BluePrint
 o. If you want to add a new URL, click on the New button
 p. Add Application window will pop up

 

 q. Provide the application name in the Name box and the host URL  in the URL box
 r. Click Add button, to the add the Application URL

 .. image:: /images/appUrl.JPG

 s. Click on Next button 
 t. Now blueprint is created for Software Stack Template type

 .. image:: /images/creationSuccess.JPG	

*****


**Creating BluePrints for Docker Template Type**

 * From the Design page choose a Docker Template Type and click Next

 .. image:: /images/dockerTT.JPG

 * Choose the available Template and click Next


 **NOTE -** If you have not created a template of Docker template type in Settings, follow the instructions at :ref:`configure-softwarestack`.

 .. image:: /images/dockerTempleteList.JPG

 * Choose your Organization name form Choose Organization dropdown
 * Provide name in Enter Blueprint Name textfield
 * Choose your business group from Choose Business Group dropdown
 * Choose your project from Choose Project dropdown

 .. image:: /images/createBpDocker.JPG

 * Click on Launch Parameters icon

  a. Enter Container Name
  b. Enter Port mappings
  c. Enter Volumes
  d. Enter Volumes-from
  e. Enter Linked Container name
  f. Enter Environment variables
  g. Enter Start up Command
  h. Enter Additional StartUp command
  i. Click on Add button
    
   .. image:: /images/dockerPopup.JPG


 * Click Next button 
 * Click OK in confirmation popup
 * Now Docker blueprint saved successfully

 .. image:: /images/dockerConfirm.JPG

*****

**Creating BluePrints for Cloud Formation Template Type**

 * From the Design page choose a Cloud Formation Template Type and click Next

 .. image:: /images/cftTemplateType.JPG

 * Choose the available Template and click Next

 **NOTE -** If you have not created a template of Cloud formation template type in Settings, follow the instructions at :ref:`configure-softwarestack`.

 .. image:: /images/cftTemplateList.JPG

 * Click on Configure Organization Parameters
 * Choose your Organization name form Choose Organization dropdown
 * Provide name in Enter Blueprint Name textfield
 * Choose your business group from Choose Business Group dropdown
 * Choose your project from Choose Project dropdown

 .. image:: /images/cftCreate.JPG

 * Click on Configure Stack Parameters
 * Choose the region from the Choose Region drop down list
 * Choose the provider from the Choose Provider drop down list
 * Choose the Keyname from the Choose Keyname drop down list
 * Choose the Subnet from the Choose Subnet down list.
 * Choose the Security Group from the Choose Security Group list
 * Choose the AMImageID from the Choose AMImageID  list
 * Choose the Instance Type from the Choose Instance Type  list
 * Click on Next button
 * Now blueprint is created for Cloud Formation Template

 .. image:: /images/cftCreateLast.JPG


