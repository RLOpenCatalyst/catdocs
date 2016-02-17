Workzone 
========

RL Catalyst Workzone is an option all the settings take action. Workzone has below options:


**Infrastructure**:
 a. Instances : It displays the numbers of instances that currently launched and running.
 b. Blueprints : This options allows you to launch instances.
 c. Cloud Formation : It displays the list of stacks launched from cloud formation blueprints.
 d. AzureARM: It displays the list of Deployments launched from Azure ARM Blueprints.
 e. Containers : Container details launched from docker blueprints.

**Orchestration**: This options allows you to execute one or more tasks/actions on multiple nodes.

**Applications**: Here user can deploy new applications and deployed applications will be shown in card or table view will all details.


Here user can deploy new applications and deployed applications will be shown in pipeline view and table view with all details.


Launch New Instances
^^^^^^^^^^^^^^^^^^^^
  Instances are launched from Blueprints. Follow below steps to launch Instances from blueprints.

  * Go to Workzone → Click on Infrastructure drop down → Choose Blueprints

  .. image:: /images/softBlueprint.JPG


  * Select the Blueprint and click on Launch button. Once the ‘Launch’ button is clicked, the instance will be launched in 5-8 minutes


  * Go to Instances tab to view the launched instance

  .. image:: /images/instances.JPG




View Instances in Table View
  RL Catalyst on the Instances page provides you two kinds of views.

  * Grid View


  * Table View


You can click on the respective button to view the instances.

 .. image:: /images/tableView.JPG




Instance Actions:
  On the launched instance user can perform below actions.
  
  * Chef Client Run
  * SSH 
  * Stop / Start
  * MoreInfo


 * **Chef Client Run** option allows you to update the Chef Client Runlist. You can add new software to the Runlist and click on **Update**

 * **SSH**, this option allows you to open the command prompt Terminal. You can execute your commands directly using this option

 * **Stop**, This option allows you to start and stop an Instance

 * **More Info**, This option displays the information about the Instance. You can view the logs of the Instance




Update Configuration
^^^^^^^^^^^^^^^^^^^^
  Any extra action on the running instance can be performed via the Chef client Run icon, which is displayed at the bottom left corner. Installing new software, upgrading a software etc can be performed using this icon. 

Follow below steps to run chef client run:

 * Click on Chef client run icon

 From here you can add Roles, Cookbooks [Present in your chef server] and Templates [Created in Settings] to the Runlist.


 .. image:: /images/chefClientRun.JPG


 * Select any cookbook and move to Runlist by clicking > icon

 * Click on Update button.
 
 * Click OK on confirmation popup to update runlist

 .. image:: /images/confirmChefClient.JPG


 * Instance Logs window will be displayed to see the logs

 .. image:: /images/instanceLogs.JPG


 * Click on Close button to close the Instance logs window



Connect to the Instance
^^^^^^^^^^^^^^^^^^^^^^^
Follow below steps to connect to Instance:

  * Click on the SSH icon present on the instance

  * Enter the Username of the Instance

  * Select the authentication type by selecting password / pem file

  * Enter the Password or Browse the Pem file

  .. image:: /images/sshTerminal.JPG

  
  * Click on Submit button

  .. image:: /images/sshShell.JPG
 


Start Instance
^^^^^^^^^^^^^^
Follow below steps to start the Instance:

Catalyst allows you to start the instatnce which is already stopped. 

 * Click on the **Start** icon of the stopped instance

 * Instance will be started and turn to Green color. Chef Client , SSH button will be enabled

 .. image:: /images/startedInstance.JPG



Stop Instance
^^^^^^^^^^^^^
Follow below steps to stop the Instance:

Catalyst allows you to stop the instatnce which is already Running.

  * Click on the Stop icon present on the instance

  * Click OK on confirmation popup

  .. image:: /images/stopConfirm.JPG


  * Instance status is showing as stopped and red icon will be shown

   **Note:** User can perform stop / start action only for the launched node from catalyst.

   **Note:** For the imported node from IP address Stop button will be grayed out will be shown later.

   **Note:** For the Stopped Instance, Chef client SSH buttons will be disabled.

    .. image:: /images/stoppedInstance.JPG






Import By IP
^^^^^^^^^^^^
In the Instances page, you can import any running instances to the catalyst application using Import By IP option, follow the below steps to import:

 * Click on Import by IP icon

 * In the **Import Instance By IP** window

 * Provide the IP address which needs to be Imported

 * Choose the operating system from **Choose Operating System** drop down list

 * Provide the user name in the **Username** box

 * Choose authentication type from the **Choose Authentication Type** drop down list. RL Catalyst provide two types of authentication, you can choose Password or by uploading PEM file

 * Type **Password or upload PEM file**

 * Provide the application name in the **Name** box and the host **URL** in the URL box

 * You can also Add new application by clicking on the Add Application URL option

 * Click **Import** to start importing the Instance

 .. image:: /images/ImportbyIP.jpg




 * Node will be imported and displayed in the instances tab. For the imported node Stop button will be disabled

 .. image:: /images/importNode.JPG







Cloud Formation Templates
^^^^^^^^^^^^^^^^^^^^^^^^^
 Follow below steps to launch Cloud formation blueprints:

 * Go to Workzone → Click on Infrastructure dropdown → Select Blueprints option → Click on **'Cloud Formation'** template type

 .. image:: /images/cftBlueprint.JPG


 * Select the cloud formation blueprint and click on Launch button

 * Enter the Unique Stack Name in the popup window

 .. image:: /images/cftPopup.JPG



 * Click on Submit button

 * Confirmation pop will be displayed with Stack ID

 .. image:: /images/cftStackid.JPG


 * Close the popup

 * Go to Infrastructure - > Cloud Formation , the CFT stack will be listed

 .. image:: /images/cftStacks.JPG


 * Go to Instances tab to see the launched Instance





Docker Blueprints
^^^^^^^^^^^^^^^^^
 Follow below steps to launch docker blueprints:

 * Go to Workzone → Click on Infrastructure dropdown → Select Blueprints option → Click on **'Docker'** template type

 .. image:: /images/dockerBlueprint.JPG


 * Select the docker template which is listed and click on Launch button

 * Click OK on the Confirmation popup

 * Click Next button in the Launch docker blueprint window


 .. image:: /images/launchDocker.JPG


 * Select the node on which you are going to launch docker blueprint and click on **Start** button


 .. image:: /images/selectNode.JPG



 * Logs window will be displayed and wait until the installation successfull

 * Go to Infrastructure - > Containers tab, the container details will be listed

 
 .. image:: /images/docker.JPG





Control Panel
^^^^^^^^^^^^^
 The **Control Panel** option displays the detailed information on the selected **Instance**	.  It displays information such as Blueprint Information , Hardware information, Software Information, Configuration Management, Additional Parameters, Services, Actions and Logs.

 .. image:: /images/controlPanel.JPG



Inspect Software 
^^^^^^^^^^^^^^^^
 Inspect functionality allows user to know the installed software on the Instance.

 * Go to Instance Control panel

 * Click on Inspect Software button

 * Popup is displayed to know the installed software on the instance

 .. image:: /images/inspect.JPG




Convert to Workstation
^^^^^^^^^^^^^^^^^^^^^^
 * Go to Instance Control panel → Services tab

 * Click on 'Convert To Workstation' button
 
 * Click on 'OK' button

 * Confirmation pop up is displayed saying **'Your workstation has been setup successfully. The .chef folder is available in Home'.**


 .. image:: /images/workStation.JPG



 * Click on **OK**  button to close the popup




View Action History
^^^^^^^^^^^^^^^^^^^
 Action history feature allows user to view the history of the actions performed on the Instances with complete details.

 * Go to Instance Control panel

 * Click on Action History tab


 .. image:: /images/actionHistory.JPG







Orchestration
^^^^^^^^^^^^^
 Orchestration option allows you to execute one or more tasks/actions on multiple nodes. 


**Chef Task**

 * To add a new task click on the **New** button

 * Select the task type from the **Select Task Type** drop down list (Chef)
 
 * Enter a task name in the **Task Name** box
 
 * Select the nodes from the **Select Nodes** list for which you want to assign task
 
 * Click on **Edit Runlist** icon and add cookbooks to the runlist

 * Click on **Update runlist** button

 * You can also select the **Cookbook Attributes**


 .. image:: /images/orchestration.JPG



 * Click Save button to save the task

 * The task is added to the **Orchestration** list

 .. image:: /images/orcList.jpg



**Jenkins Task**

 * To add a new task click on the **New** button

 * Select the task type from the **Select Task Type** drop down list (Jenkins)

 * Enter a task name in the **Task Name** box

 * Select the server from the **Select Jenkins Server** drop down list

 * Select the job from the **Select Job** drop down list

 * Select the Auto synch button to **'Yes'** [ This will shows the task execution history]

 * Add Job links for the Jenkins task


 .. image:: /images/jenkinsTask.JPG



 * Click Save button to save the task

 * The task is added to the Orchestration list


 .. image:: /images/tasklis.JPG



Edit or Remove a Task
  You can edit or remove a task. Follow the steps below.

  * Click on Edit button to edit a task from the Orchestration list


 
  * Click on Delete button to remove a task from the Orchestration list





**Execute Task**

 You can execute a task (Chef and Jenkins) by clicking Execute button in the list of tasks page.

 Once you execute the task, Execute logs window will pop-up shows the status of the execution.




**Task History**

 You can view the task history by clicking the History button in the list of tasks page. Once you click on the history button, Task History window will pop-up and shows the history of the task.

 The following information is shown in the history of task:


 * Job number

 * Job output links including logs info

 * Status

 * Start time
 
 * Endtime

 * Logs


 .. image:: /images/history.JPG










Application Deployment
^^^^^^^^^^^^^^^^^^^^^^

* From the main menu click on Settings

* Once click on Settings, from the side menu click on Devops Setup

* Click Nexus Server

* Click on +New button provided

* On Create Nexus Configuration management page enter Nexus Server Name, Username, Password, Nexus Server URL and Select Organization

* Click on + icon present next to Nexus Group ID Details and enter valid Nexus GroupID

 .. image:: /images/nexusDetails.png


* Click on Save button present in Add Nexus Group Details window

* Click on Save button  present in Nexus Configuration Management Page.

* Now your Nexus Configuration is setup and listed in the Nexus Server Management Page

 .. image:: /images/nexusCreated.png




Once Nexus Server is configured you have to associate Repository details to your Project. Follow the below steps:

 * Go to Projects Page

 * Edit your Project

 * Click + icon present next to Repository Details

 * Select your Repository Server and Repository Name

  .. image:: /images/repoDetails.png


 * Click on Save button on Add Repository Details page
 
 * Click on Save button on Edit Project Page



Once you associate repository details to your project now start creating blueprint. Follow the below steps:

* Go to Design

* Select Software Stack Template Type and click Next

* Select any Template and click Next

* Configure Provider Parameters by selecting all provider parameters

* Configure Organization Parameters by selecting

* Configure Runlist Parameters by adding **deploy_upgrade_catalyst** cookbook
 
 .. image:: /images/editRunlist.png


* Click on Update Runlist

* Expand Configure Application

* Select **Deploy app during Bootstrap** checkbox

* On selecting checkbox all Repository details will autopopulate and the latest version will be always selected. [**Note:** If u select previous version also by default it will take latest version]

 .. image:: /images/deployApp.png

* Click on Next button

* Click OK button in Confirm popup window

* Blueprint Saved Successfully message is displayed

 .. image:: /images/saveBlueprint.png



**Launching Blueprint**

* Go to Workzone

* Click Infrastructure dropdown and Select Blueprints tab

* Expand Software Stack

* Select the Instance and Click on Launch button

* Go to Instances tab and you can see node will be launched and wait until bootstrap is successfull

 .. image:: /images/launchedNode.png


* Go to Applications tab

* You will see the Application details with Name, Version, IP Address of the node and Time

 .. image:: /images/appDeployment.png


* Now copy the IP address where application is deployed and open new tab and paste IP address with port number. [Eg: 52.35.121.37:3001 ]

 .. image:: /images/runCatalyst.png

* Now Catalyst application is installed with the version 3.02.63 on the launched node. [See the version at bottom right corner of the window]


Deploy New App
  Now I will show you how to upgrade latest version of catalyst application on the same node.

* Go to Applications tab

* Click on Deploy New App button

* Enter the Repository details by selecting latest version [ Here latest is 3.02.64]

 .. image:: /images/newAppDeploy.png


* Click on Create New Job button

* Enter the Job name

* Select the Node on which you are going to upgrade latest version

* Add the cookbook **deploy_upgrade_catalyst** to the runlist

 .. image:: /images/newJenkinsJob.png


* Click on Save button

* Click OK button on Task Success popup window

* Click on Jobs dropdown

* Select the Job which is created in previous step

 .. image:: /images/selectJenkinsJob.png


* Click on Deploy button

* Click OK button on Confirmation popup window

* Execute Logs window will open and wait until Task execution is successful

 .. image:: /images/executeLogs.png

* Close Execute Logs window

* Now you can see Applcation card is displayed with Application details with Name, Version [3.02.64], IP address of the node and Time

 .. image:: /images/applicationsTab.png


* Now copy the Ip Address where application is deployed and open new tab and paste Ip Address with port number. [Eg: 52.35.121.37:3001 ] and verify the latest version [3.02.64] of the application is deployed on the node in right bottom corner of the window

 .. image:: /images/onNode.png
























