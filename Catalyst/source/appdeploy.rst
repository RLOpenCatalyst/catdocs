AppDeploy
=========

**App Deploy Flow**

* From the main menu click on Settings.

* Once click on Settings, from the side menu click on Devops Setup.

* Click Nexus Server.

* Click on +New button provided.

* On Create Nexus Configuration management page enter Nexus Server Name, Username, Password, Nexus Server URL and Select Organization.

* Click on + icon present next to Nexus Group ID Details and enter valid Nexus GroupID.

 .. image:: /images/nexusDetails.png


* Click on Save button present in Add Nexus Group Details window.

* Click on Save button  present in Nexus Configuration Management Page.

* Now your Nexus Configuration is setup and listed in the Nexus Server Management Page.

 .. image:: /images/nexusCreated.png




Once Nexus Server is configured you have to associate Repository details to your Project. For this

 * Go to Projects Page.

 * Edit your Project. 

 * Click + icon present next to Repository Details.

 * Select your Repository Server and Repository Name.

  .. image:: /images/repoDetails.png


 * Click on Save button on Add Repository Details page.
 
 * Click on Save button on Edit Project Page. 



Once you associated repository details to your project now start creating blueprint. Follow the below steps

* Go to Design.

* Select Software Stack Template Type and click Next.

* Select any Template and click Next.

* Configure Provider Parameters by selecting all provider parameters.

* Configure Organization Parameters by selecting.

* Configure Runlist Parameters by adding **deploy_upgrade_catalyst** cookbook.
 
 .. image:: /images/editRunlist.png


* Click on Update Runlist.

* Expand Configure Application.

* Select **Deploy app during Bootstrap** checkbox.

* On selecting checkbox all Repository details will autopopulate and the latest version will be always selected. [**Note:** If u select previous version also by default it will take latest version]

 .. image:: /images/deployApp.png

* Click on Next button.

* Click OK button in Confirm popup window.

* Blueprint Saved Successfully message is displayed.

 .. image:: /images/saveBlueprint.png



Launching Blueprint

* Go to Workzone.

* Click Infrastructure dropdown and Select Blueprints tab.

* Expand Software Stack.

* Select the Instance and Click on Launch button. 

* Go to Instances tab and you can see node will be launched and wait until bootstrap is successfull.

 .. image:: /images/launchedNode.png


* Go to Applications tab.

* You will see the Application details with Name, Version, IP Address of the node and Time.

 .. image:: /images/appDeployment.png


* Now copy the IP address where application is deployed and open new tab and paste IP address with port number. [Eg: 52.35.121.37:3001 ]

 .. image:: /images/runCatalyst.png

* Now Catalyst application is installed with the version 3.02.63 on the launched node. [See the version at bottom right corner of the window]


**Deploy New App:**

Now I will show you how to upgrade latest version of catalyst application on the same node.

* Go to Applications tab.

* Click on Deploy New App button.

* Enter the Repository details by selecting latest version [ Here latest is 3.02.64].

 .. image:: /images/newAppDeploy.png


* Click on Create New Job button.

* Enter the Job name

* Select the Node on which you are going to upgrade latest version.

* Add the cookbook **deploy_upgrade_catalyst** to the runlist.

 .. image:: /images/newJenkinsJob.png


* Click on Save button.

* Click OK button on Task Success popup window.

* Click on Jobs dropdown.

* Select the Job which is created in previous step. 

 .. image:: /images/selectJenkinsJob.png


* Click on Deploy button.

* Click OK button on Confirmation popup window.

* Execute Logs window will open and wait until Task execution is successful.

 .. image:: /images/executeLogs.png

* Close Execute Logs window.

* Now you can see Applcation card is displayed with Application details with Name, Version [3.02.64], IP address of the node and Time.

 .. image:: /images/applicationsTab.png


* Now copy the Ip Address where application is deployed and open new tab and paste Ip Address with port number. [Eg: 52.35.121.37:3001 ] and verify the latest version [3.02.64] of the application is deployed on the node in right bottom corner of the window.

 .. image:: /images/onNode.png







