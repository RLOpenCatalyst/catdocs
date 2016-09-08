
.. _Features-RL:Catalyst

Working with RL Catalyst
========================


.. _Import Linux Node and Install latest version of-Tomcat:

Scenario 1 : Import Linux Node and Install latest version of Tomcat
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Import RLCatalyst instance/VM 

 * Go to Workzone and expand the Organization tree on the left side to get the environments . Click on Import by IP icon 
 * Enter 127.0.0.1 in the IP Address field . User/Password is vagrant/vagrant .Enter all the details and click on import button and wait until **Instance Bootstrap Successfully**

Please refer to :ref:`import-byip`  for more details

2. Install latest version of Tomcat
 * Click on Chef-Client Run icon on the imported node in Infrastructure -> Instances tab
 * Search for **tomcat-all-rl** cookbook and add to runlist and click on update runlist button and wait until instance runlist updates . This cookbook will install the latest version of Tomcat

3. Access Tomcat
 * Once the runlist updates go to Controlpanel -> Additional Parameters -> New Application URL and add **Name** and **URL - http://localhost:8080** and save. Now click on your Applink in Infrastructure -> Instances and verify Tomcat running.

Note: If you want to **Import Linux Node and Install latest version of JBoss**, you can follow the same steps 1 and 2, But to access JBoss you need to follow

3. Access Jboss
 * Once the runlist updates go to new Tab enter **Ip address:8080** and then you will get **Welcome page of JBoss**.



**Following video demonstrates how to import Linux node and install latest version of Tomcat in RLCatalyst:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/rc_QHKGBWeo" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****




.. _Install Apache on imported node and use service to stop, start and restart-Apache:

Scenario 2 : Install Apache on imported node and use service to stop, start and restart Apache
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Create a Service command
 * In Settings, Under Gallery setup -> Service command, create a new service by selecting service command type as **chef cookbook/recipe**. Search for the **service_apache** in service cookbooks dropdown. Select actions **Start,Stop,Restart** and save.
   
 Please refer :ref:`Service-Command` for more details.


2. Import RLCatalyst instance/VM . Ignore this step if you have already executed **Scenario 1**
 * Go to Workzone and expand the Organization tree on the left side to get the environments . Click on Import by IP icon 
 * Enter 127.0.0.1 in the IP Address field . User/Password is vagrant/vagrant .Enter all the details and click on import button and wait until **Instance Bootstrap Successfully**

 Please refer to :ref:`import-byip`  for more details.


3. Install Apache using chef client run
 * Click on Chef-Client run button on the imported node and add **apache2** cookbook and click on Update runlist button and wait until instance runlist gets updated


4. SSH in to the Node from RLCatalyst and check the apache status
 * SSH in to the box from rlcatalyst and run **sudo service apache2 status** to check the Apache status
   Apache is running

5. Add the service apache to the node
 * Go to Controlpanel -> Service Tab -> Click on Add New Service. Choose the apache service and save.
 

6. Stop the service and check the status
 * Click on Stop icon
 * SSH in to the box from catalyst and run **sudo service Apache status** and check the Apache status.
   You can see that Apache is stopped


7. Start the service and check the status
 * Go to Controlpanel -> Services and Click on Start icon
 * SSH in to the box from catalyst and run **sudo service Apache status**
   Apache is up and running now

8. Restart the service and check the status
 * Click on Restart icon
 * SSH in to the box from catalyst and run **sudo service Apache status**
   Apache is up and running now  

**Following video demonstrates how to Install Apache on imported node and use service to stop Apache in RLCatalyst:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/pt2Pg3rzFuc" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****


.. _Deploy Pet-clinic application in the imported node:

Scenario 3: Deploy Petclinic application in the imported node
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Import RLCatalyst instance/VM . Ignore this step if you have already executed **Scenario 1**
 * Go to Workzone and expand the Organization tree on the left side to get the environments . Click on Import by IP icon 
 * Enter 127.0.0.1 in the IP Address field . User/Password is vagrant/vagrant .Enter all the details and click on import button and wait until **Instance Bootstrap Successfully**

   Please refer to :ref:`import-byip`  for more details.


2. Install Tomcat Cookbook(tomcat-all-rl) . Ignore this step if you have already executed **Scenario 1**
 * Click on Chef-Client Run icon on the imported node in Workzone -> Infrastructure -> Instances tab
 * Search for **tomcat-all-rl** cookbook and add to runlist and click on update runlist button and Wait until instance runlist updates


3. Create a Chef orchestration task, Choose the node and add the cookbook deploy_war & Edit cookbook attributes and save
  * In Workzone, Under Orchestration ,create a new Chef task and add **deploy_war** cookbook and edit the following attributes
  * Source code url - **https://s3-us-west-2.amazonaws.com/catalystcode/petclinic-2.02.71.war**
  * Application version – 2.02.71
  * Node publice IP – enter the public IP where tomcat is running and present as node in catalyst.

4. Execute the task 
 * After execution of task, go to Controlpanel -> Additional Parameters -> New and add **Name** and **URL - http://$host:8080/petclinic** and save. Now click on your Applink in Infrastructure -> Instances and verify petclinic installtion.



**Following video demonstrates how to Import Ubuntu Node and Deploy petclinic in RLCatalyst:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/iabnWpgMOhE" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****


.. _Update Petclinic application-version:

Scenario 4 : Update Petclinic application version
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Import RLCatalyst instance/VM . Ignore this step if you have already executed **Scenario 1**
 * Go to Workzone and expand the Organization tree on the left side to get the environments . Click on Import by IP icon 
 * Enter 127.0.0.1 in the IP Address field . User/Password is vagrant/vagrant .Enter all the details and click on import button and wait until **Instance Bootstrap Successfully**

   Please refer to :ref:`import-byip`  for more details.

2. Install Tomcat Cookbook(tomcat-all-rl) . Ignore this step if you have already executed **Scenario 1**
 * Click on Chef-Client Run icon on the imported node in Workzone -> Infrastructure -> Instances tab
 * Search for **tomcat-all-rl** cookbook and add to runlist and click on update runlist button and Wait until instance runlist updates

3. Create a Chef orchestration task. Ignore this step if you have already executed **Scenario 3**. 
 * In Workzone, Under Orchestration Create a New Chef Task and add deploy_war cookbook and edit the following attributes
 * Source code url - https://s3-us-west-2.amazonaws.com/catalystcode/petclinic-2.02.71.war
 * Application version – 2.02.71
 * Node publice IP – enter the public IP where tomcat is running and present as node in catalyst 


4. Execute the task.  Ignore this step if you have already executed **Scenario 3**. 
 * After execution of task, go to Controlpanel -> Additional Parameters -> New and add Name and URL - http://$host:8080/petclinic and save. Now click on your Applink in Infrastructure -> Instances and verify petclinic installtion.


5. Upgrade Petclinic Version
 * Edit Chef Orchestration task
 * Click on Edit attribute link
 * Enter the Source code URL with the latest version **https://s3-us-west-2.amazonaws.com/catalystcode/petclinic-2.02.72.war**
 * Application version – 2.02.72
 * Node publice IP – enter the public IP where tomcat is running and present as node in catalyst and save

6. Now Execute the task and verify the latest version
 * After execution of task, go to Controlpanel -> Additional Parameters -> New and add Name and URL - http://$host:8080/petclinic and save. Now click on your Applink in Infrastructure -> Instances and verify petclinic installtion with the latest version.



*****


.. _View History of App deployments &-upgrades:

Scenario 5 :View History of App deployments & upgrades
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Execute **Scenario 3** to deploy Petclinic application in the imported node
2. Once application is installed on on the node navigate to applications tab and click on **H** icon[History], you will find history of the application deployed


*****



.. _Deploy a multi-tier application using docker-container:


Scenario 6 : Deploy a multi-tier application using docker container
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Introduction:** Here, we are deploying a petclinic application with 2 docker container, one for Mysql and one for petclinic. 

1. Create docker template for Mysql and petclinic

 * Go to GallerySetup -> Templates
 * Create template for mysql by adding docker repo path ``relevancelab/mysqlpet`` and save
 * Create template for petclinic by adding docker repo path ``relevancelab/tomcatpet`` and save

2. Create a docker blueprint using Mysql and petclinic template
 
 * Go to Design -> Select mysql template -> Click Launch parametrs icon -> Enter container name and add Additional startup as ``init.sh`` -> Click on Add button

 * Click on Add button to add tomcat template -> select tomcat template and the tag -> Click on Add button
 * Click Launch parametrs icon -> Enter container name and Port mapping as ``8080:8080`` and Nlnked container as mysqlpet:mysql -> Click on Add button 
 * Click Next button to create blueprint

3. Import Ubuntu Node
 
 * Go to Workzone and expand the Organization tree on the left side to get the environments . Click on Import by IP icon, Enter all the details and click on import button and wait until **Instance Bootstrap Successfully**

   Please refer to :ref:`import-byip`  for more details

4. Run Docker cookbook on the instance
 
 * Click Chef client run and Run docker by adding ``docker_rl`` cookbook and wait until **Instance Runlist Updates** & docker icon is displayed on card


5. Launch Docker blueprint on Ubuntu node

 * Go to **Infrastructure** -> **Blueprints** -> **Docker** -> **Next** and select the instance and **Start**. Wait until **Done image pull and run** message is displayed


6. Verify the 2 Contianers

 * Once image pull is successfull go to **Infrastructure** -> **Containers** tab to see the container details


7. Access the Petclinic application

 * Access the Petclinic application by accessing **$host:8080/petclinic**


8. SSH in to the ubuntu node form RLCatalyst and verify the containers

 * Click on SSH icon, enter the valid details and submit 

 * Enter the following command ``docker ps`` and check the container details




Following video demonstrates how to Deploy a composite docker container(petclinic app with 2 container) in RLCatalyst:


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/ClkYW13vLvU" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>




*****



.. _Launch New Ubuntu Instance and Install-Jboss:

Scenario 7 : Create a new Ubuntu Instance  and Install Jboss
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Create a blueprint to launch a new Ubuntu instance and install JBoss server on it  . 

1. Add Provider
 * In Settings, under DevopsSetup -> Providers, add a New AWS provider by entering the valid details
   
   Please refer to :ref:`provider-settings` for more details.

2. Add VMImage for Ubuntu
 * In Settings, under Gallery setup -> VMImage, add a New VMImage for Ubuntu .  The image should be accessible from your AWS account
   
   Please refer to :ref:`configure-vm` for more details.

3. Create Blueprint using Ubuntu as base Image by adding Jboss Cookbook to runlist
 * In Design, under OSImage template type select ubuntu template and create blueprint by entering the other details and by adding **jboss7_rl** cookbook in configure runlist parameters and save

4. To verify Jboss installation
 * Launch the Blueprint from Workzone -> Infrastructure -> Blueprints. After launch of Blueprint go to Infrastructure -> Instances, once the node bootstraps go to Controlpanel -> Additional Parameters -> New Application URL and add **Name** and **URL - http://$host:8080** and save. Now click on your Applink in Infrastructure -> Instances and verify Jboss installtion.


**Following video demonstrates how to Launch New Ubuntu Instance and Install Jboss in RLCatalyst:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/Ifsh6gjeeeo" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****




.. _Deploy Windows App on-IIS:

Scenario 8 : Deploy Windows App on IIS
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We are deplying MyShopper application with deploy_iis cookbook.

1. Add Provider . Skip this step if Scenario6 is already executed
 * In Settings, under DevopsSetup -> Providers, add a New provider by entering the valid details

   Please refer to :ref:`provider-settings` for more details.

2. Add VMImage for Windows(Public AMI to be added for Windows2012).
 * In Settings, under Gallery setup -> VMImage, add a New VMImage for Windows

   Please refer to :ref:`configure-vm` for more details.

3. Create Blueprint using Windows base image by adding IIS cookbook to runlist
 * In Design, under OSImage template type select windows template and create blueprint by entering the other details and by adding **deploy_iis** cookbook in configure runlist parameters and save

4. Launch Blueprint and Verify IIS Installation
 * Launch the Blueprint from Workzone -> Infrastructure -> Blueprints. After launch of Blueprint go to Infrastructure -> Instances, once the node bootstraps enter <ipAddress> of the instance in new tab it will take you to the MyShopper application home page.


**Following video demonstrates how to Launch Windows Instance and Install IIS in RLCatalyst:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/m0yFKmCM4ak" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****



.. _Launch New ubuntu Instance, Install Tomcat, upgrade to-v8.0[attribute]:

Scenario 9 : Create a new Ubuntu Instance, Install Tomcat and upgrade to latest version
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Add Provider . Skip this step if Scenario6 is already executed
 * In Settings, under DevopsSetup -> Providers, add a New provider by entering the valid details

   Please refer to :ref:`provider-settings` for more details.

2. Add VMImage for Ubuntu . Skip this step if Scenario6 is already executed
 * In Settings, under Gallery setup -> VMImage, add a New VMImage for Ubuntu

   Please refer to :ref:`configure-vm` for more details.

3. Create Blueprint using Ubuntu as base Image and Tomcat Cookbook
 * In Design, under OSImage template type select ubuntu template and create blueprint by entering the other details and by adding **tomcat-all-rl** cookbook in configure runlist parameters and save

4. Launch Blueprint and Access Tomcat
 * Launch the Blueprint from Workzone -> Infrastructure -> Blueprints. After launch of Blueprint go to Infrastructure -> Instances, once the node bootstraps go to Controlpanel -> Additional Parameters -> New Application URL and add **Name** and **URL - http://$host:8080** and save. Now click on your Applink in Infrastructure -> Instances and verify Tomcat installtion.

5. Chef Client Run to upgrade Tomcat version to 8.0
 * Click on Chef-Client run button and Edit the cookbook attributes and select the latest **Tomcat Version**, save and update runlist
   Wait until the Instance runlist updates and Now click on your Applink in Infrastructure -> Instances and verify Latest Tomcat installtion.



**Following video demonstrates how to Launch New ubuntu Instance,Install Tomcat,upgrade to v8.0[attribute] in RLCatalyst:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/4sd-PK3_sLI" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****



.. _Provider Sync and-Import Instances:

Scenario 10 : Provider Sync and Import Instances
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Once the basic data is loaded, you can start exploring RLCatalyst from the Provider-Sync Feature. You can sync nodes from your AWS provider account and convert the nodes to 'Managed' . This will give a control on your AWS infra by letting you track the capacity, cost and usage . Once sync-ed, you can see the summary dashboard from 'Track'

1. Add your AWS Provider. Skip this step if Scenario6 is already executed
 * In Settings, under DevopsSetup -> Providers, add a New provider by entering the valid details
   Please refer to :ref:`provider-settings` for more details.

2. Provider Sync. Once the provider account is added, you can start importing the nodes into RLCatalyst . Importing will bootstrap the nodes with the configured chef server . The imported instances can be managed from the workzone, under the project and environment to which the nodes are imported.

 * Click on Sync instances button of your provider -> **UnManaged Instances** of the created provider

3. Import the instances into Catalyst **[Unmanaged to managed]**
 * Select the Instances and click on Import Instances and enter the valid details and Sync
 * You can see the nodes imported in the respective environments and verify the imported instances is present under **managed instances** tab.


Please refer to :ref:`providersync and-import` for more details.

*****


.. _AWS Cost, Usage-Dashboards:

Scenario 11 : AWS Cost, Usage Dashboards
^^^^^^^^^^^^^^^^^^^^^^^^^
RLCatalyst provides you a consolidated dashboard for tracking your AWS infrastructure cost and usage . This helps you to identify un-used capacity and do better utilization. RLCatalyst summarizes this data for all the AWS provider accounts configured.

Follow the instructions to configure your dashboards:

1. Add Provider . Skip this step if Scenario6 is already executed
 * In Settings, under DevopsSetup -> Providers, add a New **AWS** provider by entering the valid details

   Please refer to :ref:`provider-settings` for more details.

2. Track -> usage and cost dashboards
 * Click on **Tracks** under provider you will be able to see **Provider Dashboard** and **AWS Summary Dashboard**


**Provider Dashboard**
 This will give you the snapshot of instances - Total Number vs Number of Managed vs Number of Un-Managed.

 .. image:: /images/summary.png


**AWS Summary Dashboard**
 This will give you the snapshot of Total cost, Daily cost etc.

 .. image:: /images/summaryDash.png


**Following video demonstrates how to view AWS Cost,Usage dashboards in RLCatalyst:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/N4TiDHC7vzE" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****


.. _Deploy Wordpress on multiple docker-container:

Scenario 12: Deploy Wordpress on multiple docker container 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
1. Create a docker template for MYSQL
 * Go to Settings -> Gallery Setup -> Templates, Enter the Template name -> Choose Template type as **Docker** -> Choose the **Organization**
 * Donot select the **Docker Repo** -> **Add Docker Repo Path** as **relevancelab/wpmysql** and save


2. Create a docker template for Wordpress
 * Go to Settings -> Gallery Setup -> Templates, Enter the Template name -> Choose Template type as **Docker** -> Choose the **Organization**
 * Donot select the ``Docker Repo`` , **Add Docker Repo Path** as **relevancelab/wordpress** and save


3. Create Docker bluperint for MYSQL
 * In Design -> select **AWS** provider -> select **Docker** Template Type -> select your template, add the details and save


4. Create Docker blueprint for wordpress
 * In Design -> select **AWS** provider -> select **Docker** Template Type -> select your template, add the below details and save
 * **Portmapping: 8080:80**
 * **Linked Container: mysql:mysql**
 
5. Launch Ubuntu Node or Import a Ubuntu node
 * Click on **Chef Client run** -> Run **docker** cookbook on that node

6. Launch Mysql Docker Blueprints.
 * Go to Infrastructure -> Blueprints -> Expand Docker -> Select Mysql blueprint and Click on Launch button -> Select the node -> Click on Start button

7. Launch Wordpress Docker Blueprints.
 * Go to Infrastructure -> Blueprints -> Expand Docker -> Select Wordpress blueprint and Click Launch button -> Select the node -> Click on Start button

8. Go to Containers tab to view the container and thier details.
 * Go to Infrastructure -> Containers . You can find 2 containers wordpress and mysql with the details being displayed


9. Add Application URL in instance control panel
 * Go to Instance -> Control Panel and add application in this format (http://$host:8080)


10. Access wordpress Application by clicking the Appname.
 * Click on More icon on instance control panel -> Click on the Wordpress application name. User should be able to see wordpress installation page

11. Connect to the instance and verify container details are listed
 * Click on SSH icon -> Enter the Details and submit , Execute ``sudo docker ps`` command, Container details should be displayed


**Following video demonstrates the Composite Docker for Wordpress:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/_17iCshUxUE" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****


.. _Create CentOS instance and launch-Liferay:

Scenario 13 : Create CentOS instance and launch Liferay
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Create template for liferay app

 * Go to GallerySetup -> Templates

 * Create template by adding deploy_liferay_app cookbbok and save


2. Under Desgin create blueprint using the liferayapp template

 * Go to Design -> Select liferay template and create blueprint. (Make sure the instance size is atleast 2GB)
  
 * Add application URL **http://$host:8001**


3. Launching blueprint

 * Go to Workzone -> Infrastructure -> Blueprints -> Launch the blueprint


4. Access Liferay application

 * Access Liferay application by clicking on **APP link URL** present on the Instance card and verify the LifeRay     




Following video demonstrates how to Launch New Centos Instance and deploy LifeRay in RLCatalyst:


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/TNylGUUhuM8" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****



.. _Create and Launch an AWS CFT Blueprint for 2-node Petclinic:

Scenario 14 : Create and Launch an AWS CFT Blueprint for 2-node Petclinic
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Create CloudFormation Template

 * Go to GallerySetup -> Templates

 * Create Cloud Formation template by uploading your template file and other details


2. Under Desgin create blueprint using cloud formation template

 * Go to Design -> select **Cloud formation** template type -> Next -> select your template -> Next -> Enter Blueprintname, Choose Business Group & project

 * In **Configure Stack Parameters** section provide the valid details for **Region, Provider, KeyName, SecurityGroup, AMImage ID, Instance Username** and other details

3. Launch the Cloud Formation Blueprint

 * Go to Workzone -> your respective Environment -> Infrastruture -> Blueprints -> CloudFormation and launch the Blueprint by entering the ``Unique stack Name``

4. Verify the Stack 

 * Now Verify the Stack at Infrastructure -> CloudFormation, Wait until the Stack shows from **CREATE_IN_PROGRESS** to **CREATE_COMPLETE**

5. Verify the 2 VM/Instances Launched 

 * Go to Infrstructure -> Instances, you will be able to see the 2 nodes/VM's launched and click on **MoreInfo icon** & wait until both the instances **Bootstrap successfully**

6. Run cookbook multitierdb for VM1

* Click on ChefClient run icon and select **multitier_db** cookbook and move to runlist and update. Wait Until the **Instance Runlist updates**


7. Run cookbook tomcat & multitierwar for VM2

 * Click on ChefClient run icon and select **tomcat_all_rl, multitier_war** cookbook and move to runlist and update. Wait Until the **Instance Runlist updates**


8. Verify the petclinic application using the VM2 IPAddress
 
 * Now verify the petclinic application using **http://VM2 Ipaddress:8080/petclinic**. You will be able to access the application


Following video demonstrates how to Create and Launch an AWS CFT Blueprint for 2-node Petclinic in RLCatalyst:


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/4RV0TEvqdZk" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****

.. _Install LAMP Stack on a single-node:

Scenario 15 : Install LAMP Stack on a single node
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Import a Ubuntu Node to RLcatalyst

 * Go to Workzone and expand the Organization tree on the left side to get the environments . Click on Import by IP icon 
 * Enter the **IP Address, Username** & select the **OS, Config Management, pem file**


Please refer to :ref:`import-byip`  for more details


2. Chef Client Run on the Instance with LAMP Role and editing the cookbook attributes
 
 * Click on Chef-Client Run icon, select the **lamp_role** cookbook and move to runlist

 * Edit the **Cookbook attributes** by clicking on the edit button and provide the value for **Root Password** and update the runlist


3. Access Apache

 * Access apache at  **http://$host** of that machine


4. Access PHP
 
 * Access apache at  **http://$host/index.php** of that machine


5. Access MySql

 * From RLCatalyst click on SSH icon of the instance and provide the valid details and submit

 * Now Enter the following command **mysql -u root -p** and enter the same **Root Password** which you provided while editing the cookbook attributes and verify MySql


Following video demonstrates how to Launch New Ubuntu Instance and deploy LAMP[Linux, Apache, MySql, PHP] in RLCatalyst:


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/nZ2K8LZCt04" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****




.. _Configure and Execute a Jenkins-Jobs:

Scenario 16 : Configure and Execute a Jenkins Jobs
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Execute your Jenkins job from rlcatalyst and see the history of each jobs. Jenkins server should be configured in rlcatalyst to initiate the job execution. Please refer to * :ref:`Configure-Jenkins`

Please refer to ``Jenkins Task`` under :ref:`Orchestration-JenkinsTask` to **Create & Execute** Jenkins Task


**Following video demonstrates how to Create and Execute Jenkins Task in RLCatalyst**:


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/fM5nrBBJmko" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

*****

.. _Deploy and Promote-a Java Application:

Scenario 17 : Deploy and Promote a Java Application
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Here we are deploying and promoting petclinic app.

1. Import a ubuntu node or Launch a Blueprint. Wait until the Node Bootstrap successfully.

2. Create a Chef Task in **Orchestration Tab** and Save by adding **tomcat-all-rl** and **deploy_war** cookbooks.

3. Go to Applications and Deploy New App by clicking **+Deploy New App** :

  * Enter Repository Details: **Repository Server**, **Repository**, **Group ID**, **Artifacts** and **Version** which you want to deploy
  * Add the job which you created
  * Wait until task execution is success
  * Verfiy the card with the version you selected in applications.
  * Click on Approve and then promote will be enabled

4. Now, Access petclinic application in the format http://<ipaddress>:8080/petclinic. Petclinic application home page will open.

Now, Promote Petclinic in other enviornment:

1. Import a ubuntu node or Launch a Blueprint. Wait until the Node Bootstrap successfully.

2. Create a Chef Task in **Orchestration Tab** and Save by adding **tomcat-all-rl** and **deploy_war** cookbooks.

3. Go to **applications tab** and click on **promote** and select the target enviornment and Select the job, which you created in step 2 and node, which you launched or imported and click on Promote

4. Now, Access petclinic application in the format http://<ipaddress>:8080/petclinic. Petclinic application home page will open.

**Following video demonstrates how to Deploy and Promote Petclinic:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/pxa5NYhRKDw" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****

.. _Deploy-a 3-tier application:

Scenario 18 : Deploy a 3-tier application
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Here we are deploying petclinic app using petclinic database, petclinic application and loadbalancer.

1. Create  three Blueprints:

  * Create a ubuntu blueprint and add role **petclinic_db** for first blueprint.

  * Create a ubuntu blueprint and add role **petclinic_app** for second blueprint.

  * Create a ubuntu blueprint and add cookbook **loadblncr** for third blueprint.

2. Now, go to **WORKZONE -> Infrastructre -> Blueprints** and launch your created blueprints one by one. Wait until the Node Bootstrap successfully for each blueprint.

3. Now, take the <ipaddress> of **load_balancer node** and Access petclinic application in the format http://<ipaddress>/petclinic. Petclinic application home page will open.

**Following video demonstrates how to Deploy a 3-tier application:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/tA3ps-tRmBQ" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****

.. _Update tags in-AWS:

Scenario 19 : Update tags in-AWS
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Prerequisite:** You must have an AWS account.

1. In SETTING -> DevOps Setup -> Providers, youl will get list of providers. And in **Action** colunm you will find **Syn Instances** button.
By clicking on **Syn Instances** button, you will get 3 tabs, Tags, Mappings and Instances:

  1. Tags: you have two sections, left side you will get the tags which are present in ur AWS acccount will shown here and you can add description for your refrence only. And right side you can map the tags with PROJECT ans ENVIRONMENT, Specify which tags represent project name and the environment name.
  Once you will save it, you can see the refelection in Mapping tab.

  2. Mappings: In Mapping, all the mapped Tag Values would be visible with respect to Projects and Environment. Select one tag name for project from drop down as well as Environment tag name for Environment And save the changes. Now go to Instances tab.

  3. Instances: You have 3 catalyst status:

    * Managed: If catalyst status is 'Managed', you will get all "Bootstraped successfull Instances". You can delete the instances from here.

    * Assigned: In assigned tab you will get mapped instances from mappings. From here you can "Import Instances".

    * Unassigned: Here you will get all other Instances available in your AWS account. Here you can update the tags value by selecting the node.

**Following video demonstrates how to Update tags in AWS:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/c1kRGPCWNnQ" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****

.. _Design and Launch-Application:

Scenario 20 : Design and Launch Application
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Design an entire app and launch instance with the app running.

1. Create a Nexus Server with valid details and add Nexus Group ID - org.catalyst and save.

2. Now, go To project and edit your project Select the Repository server -Nexus and Repository Name - Catalyst then ADD and save the project.

3. Create a Software Stack Template for catalyst or petclinic and save. Add cookbook **deploy_upgrade_catalyst** for **catalyst** and **tomcat-all-rl** & **deploy_war** for **petclinic** accordingly.

4. Go To Design & Create a Softwarestack bluperint using the template, which you created and add call back URL http://catalyst3.rlcatalyst.com/app-deploy or app/deploy and save the blueprint.

5. Go to **Workzone** and launch the Blueprint.

6. Now, go to **Instances** copy the IP of your launced blueprint and open new tab, paste that **IP:3001** to verify- the App is deployed or not. 

**Following video demonstrates how to deploy Application during Instance launch using Nexus Server:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/2gTJ9ppTnVo" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****

.. _Design and Launch 3-tier-Application:

Scenario 21 : Design and Launch 3-tier Application
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Here we are going to launch Petclinic Application. petclinic Data Base, petclinic App and petclinic web(load balancer), for this we need to create blueprint for each of **software stack** type.

1. While creating blueprint for petclinic database add **petclinic_db** role.

  .. image:: /images/CB1.png

2. Add **petclinic_app** role while creating blueprint for petclinic app.

  .. image:: /images/CB2.png

3. Add **loadblncr** cookbook while creating blueprint for petclinic web.

  .. image:: /images/CB3.png

Now, create new **Composite type blueprint**

  .. image:: /images/CB4.png

Add those 3 blueprints in composite type blueprint into Selected Blueprint and Save it.

  .. image:: /images/CB5.png

Once it is created user can see the blueprint under **Composite**. User can delete, Launch the blueprint by clicking on specified buttons.

  .. image:: /images/CB6.png

And user can also see all the details of composite blueprint by clicking on information button.

  .. image:: /images/CB7.png

Launch by clicking on launch button, it will ask for confirmation before start launching it.

  .. image:: /images/CB8.png

Once you will confirm it to launch, it will start launching petclinic_db, petclinic_app and loadbalancer one by one. First it will start launching **petclinic_db**

  .. image:: /images/CB9.png

When **petclinic_db** will be bootstraped successfully then only it will start with petclinic_app.

  .. image:: /images/CB10.png

Similarly when petclinic_app will bootstraped successfully then it will start launching loadbalancer.

  .. image:: /images/CB11.png

Now, to access the application, open new tab and access petclinic app with ip address petclinic app **<ipAddress>:8080/petclinic**

  .. image:: /images/CB12.png

And to access the application with ip address of loadbalancer into new tab type **<ipAddress>/petclinic**

  .. image:: /images/CB13.png


*****

