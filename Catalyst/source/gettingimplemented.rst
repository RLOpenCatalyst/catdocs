
.. _Features-RL:Catalyst

Working with RL Catalyst
========================


.. _Import Linux Node and Install latest version of-Tomcat:

Import Linux Node and Install latest version of Tomcat
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Import Node by IP

Import one of your existing Linux instances into RLCatalyst .The instance should have a public IP and should be reachable from the catalyst network . 

 * Click on Import by IP icon in the respective **Environment** of **Workzone** 
 * Enter all the details and click on import button and wait until **Instance Bootstrap Successfully**

If you are importing RLCatalyst VM, which is running using vagrant, IP is 127.0.0.1 and user/password - vagrant/vagrant. 
Please refer to :ref:`import-byip`  for more details

2. Install latest version of Tomcat
 * Click on Chef-Client Run icon on the imported node in Infrastructure -> Instances tab
 * Search for **tomcat-all-rl** cookbook and add to runlist and click on update runlist button and Wait until instance runlist updates

3. Access Tomcat
 * Once the runlist updates go to Controlpanel -> Additional Parameters -> New Application URL and add **Name** and **URL - http://$host:8080** and save. Now click on your Applink in Infrastructure -> Instances and verify Tomcat installtion.



**Following video demonstrates how to import Linux node and install latest version of Tomcat in RLCatalyst:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/rc_QHKGBWeo" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****

.. _Install apache2 on imported node and use service to stop-apache2:

Install apache2 on imported node and use service to stop apache2
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Creating a Service command
 * In Settings, Under Gallery setup -> Service command, create a new service by selecting service command type as **chef cookbook/recipe**. Search for the **service_apache** in service cookbooks dropdown. Select actions **Start,Stop,Restart** and save.
   
   Please refer :ref:`Service-Command` for more details.


2. Import a Linux Node
 * Click on Import by IP icon in the respective **Environment** of **Workzone**
 * Enter all the details and click on import button and wait until **Instance Bootstrap Successfully**

   Please refer to :ref:`import-byip`  for more details.


3. Install Apache using chef client run
 * Click on Chef-Client run button in the Workzone -> Infrastructure -> Instances tab, of the imported node and add **apache2** cookbook and click on Update runlist button and Wait until instance runlist updates


4. SSH in to the Node from RLCatalyst and check the apache status
 * SH in to the box from catalyst and run **sudo service apache2 status**
   apache2 is running

5. Add the service apache to the node
 * Go to Controlpanel -> Service Tab -> Click on Add New Service. Select the service and save.
 

6. Stop the service and check the status
 * Go to Controlpanel -> Services and Click on Stop icon
 * SSH in to the box from catalyst and run **sudo service apache2 status**
   apache2 is not running


7. Start the service and check the status
 * Go to Controlpanel -> Services and Click on Start icon
 * SSH in to the box from catalyst and run **sudo service apache2 status**
   apache2 is running


**Following video demonstrates how to Install apache2 on imported node and use service to stop apache2 in RLCatalyst:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/pt2Pg3rzFuc" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


*****


.. _Import Ubuntu Node and Deploy-petclinic:

Import Ubuntu Node and Deploy petclinic
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Import a Linux Node
 * Click on Import by IP icon in the respective **Environment** of **Workzone**
 * Enter all the details and click on import button and wait until **Instance Bootstrap Successfully**

   Please refer to :ref:`import-byip`  for more details.


2. Install Tomcat Cookbook(tomcat-all-rl)
 * Click on Chef-Client Run icon on the imported node in Workzone -> Infrastructure -> Instances tab
 * Search for **tomcat-all-rl** cookbook and add to runlist and click on update runlist button and Wait until instance runlist updates


3. Create a Chef orchestration task, Choose the node and add the cookbook deploy_war & Edit cookbook attributes and save
  * In Workzone, Under Orchestration Create a New Chef Task and add **deploy_war** cookbook and edit the following attributes
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


.. _Launch New Ubuntu Instance and Install-Jboss:

Launch New Ubuntu Instance and Install Jboss
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Add Provider
 * In Settings, under DevopsSetup -> Providers, add a New provider by entering the valid details
   
   Please refer to :ref:`provider-settings` for more details.

2. Add VMImage for Ubuntu
 * In Settings, under Gallery setup -> VMImage, add a New VMImage for Ubuntu
   
   Please refer to :ref:`configure-vm` for more details.

3. Create Blueprint using Ubuntu as base Image by adding Jboss Cookbook to runlist
 * In Design, under OSImage template type select ubuntu template and create blueprint by entering the other details and by adding **jboss7_rl** cookbook in configure runlist parameters and save

4. To verify Jboss installtion
 * Launch the Blueprint from Workzone -> Infrastructure -> Blueprints. After launch of Blueprint go to Infrastructure -> Instances, once the node bootstraps go to Controlpanel -> Additional Parameters -> New Application URL and add **Name** and **URL - http://$host:8080** and save. Now click on your Applink in Infrastructure -> Instances and verify Jboss installtion.


**Following video demonstrates how to Launch New Ubuntu Instance and Install Jboss in RLCatalyst:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/Ifsh6gjeeeo" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****


.. _Launch Windows Instance and Install-IIS:

Launch Windows Instance and Install IIS
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Add Provider
 * In Settings, under DevopsSetup -> Providers, add a New provider by entering the valid details

   Please refer to :ref:`provider-settings` for more details.

2. Add VMImage for Windows(Public AMI to be added for Windows2012)
 * In Settings, under Gallery setup -> VMImage, add a New VMImage for Windows

   Please refer to :ref:`configure-vm` for more details.

3. Create Blueprint using Windows base image by adding IIS cookbook to runlist
 * In Design, under OSImage template type select windows template and create blueprint by entering the other details and by adding **iis** cookbook in configure runlist parameters and save

4. Launch Blueprint and Verify IIS Installation
 * Launch the Blueprint from Workzone -> Infrastructure -> Blueprints. After launch of Blueprint go to Infrastructure -> Instances, once the node bootstraps RDP to the machine and in search options search for IIS.Internet Information Services Manager should be available.


**Following video demonstrates how to Launch Windows Instance and Install IIS in RLCatalyst:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/m0yFKmCM4ak" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****



.. _Launch New ubuntu Instance,Install Tomcat,upgrade to-v8.0[attribute]:

Launch New ubuntu Instance,Install Tomcat and upgrade to latest version
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Add Provider
 * In Settings, under DevopsSetup -> Providers, add a New provider by entering the valid details

   Please refer to :ref:`provider-settings` for more details.

2. Add VMImage for Ubuntu
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

Provider Sync and Import Instances
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Add Provider
 * In Settings, under DevopsSetup -> Providers, add a New provider by entering the valid details
   Please refer to :ref:`provider-settings` for more details.

2. Provider Sync
 * Click on Sync instances button of your provider -> **UnManaged Instances** of the created provider

3. Import the instances into Catalyst **[Unmanaged to managed]**
 * Select the Instances and click on Import Instances and enter the valid details and Sync
 * You can see the nodes imported in the respective environments and verify the imported instances is present under **managed instances** tab.


Please refer to :ref:`providersync and-import` for more details.

*****


.. _Update application-version[petclinic]:

Update application version[petclinic]
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Import a Linux Node
 * Click on Import by IP icon in the respective Environment of Workzone

 * Enter all the details and click on import button and wait until Instance Bootstrap Successfully

   Please refer to :ref:`import-byip` for more details.

2. Install Tomcat Cookbook(tomcat-all-rl)
 * Click on Chef-Client Run icon on the imported node in Workzone -> Infrastructure -> Instances tab
 * Search for tomcat-all-rl cookbook and add to runlist and click on update runlist button and Wait until instance runlist updates

3. Create a Chef orchestration task, Choose the node and add the cookbook deploy_war & Edit cookbook attributes and save
 * In Workzone, Under Orchestration Create a New Chef Task and add deploy_war cookbook and edit the following attributes
 * Source code url - https://s3-us-west-2.amazonaws.com/catalystcode/petclinic-2.02.71.war
 * Application version – 2.02.71
 * Node publice IP – enter the public IP where tomcat is running and present as node in catalyst 


4. Execute the task
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

View History of App deployments & upgrades
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Import node or launch a new node[ubuntu]
2. Install Tomcat Cookbook(tomcat-all-rl)
3. Add cookbook deploy_war and  Edit attributes
  a. Source code url - **https://s3-us-west-2.amazonaws.com/catalystcode/petclinic-2.02.71.war**
  b. Application version – 2.02.71
  c. Node publice ip – enter the public ip where tomcat is running and present as node in catalyst.
4. Once application is installed on on the node navigate to applications tab and click on **H** icon[History], you will find history of the application deployed



*****


.. _AWS Cost,Usage-Dashboards:

AWS Cost,Usage Dashboards
^^^^^^^^^^^^^^^^^^^^^^^^^
RLCatalyst provides you a consolidated dashboard for tracking your AWS infrastructure cost and usage . This helps you to identify un-used capacity and do better utilization. RLCatalyst summarizes this data for all the AWS provider accounts configured.

Follow the instructions to configure your dashboards:

1. Add Provider
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


.. _providersync and-import:

Add Provider and do Provider Sync
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Once the basic data is loaded, you can start exploring RLCatalyst from the Provider-Sync Feature. You can sync nodes from your AWS provider account and convert the nodes to 'Managed' . This will give a control on your AWS infra by letting you track the capacity, cost and usage . Once sync-ed, you can see the summary dashboard from 'Track'


1. **Add your AWS provider** account details in RLCatalyst . Refer to :ref:`provider-settings` for more help
2. **Sync your provider with RLCatalyst**. Once the provider account is added, you can start importing the nodes into RLCatalyst . Importing will bootstrap the nodes with the configured chef server . The imported instances can be managed from the workzone, under the project and environment to which the nodes are imported. Refer to :ref:`provider-sync` for more help



**Following video demonstrates how to add provider and do sync in RLCatalyst:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/HIMlbwtc8Zc" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****




.. _Create & Execute Jenkins Jobs from-RLCatalyst:

Create & Execute Jenkins Jobs from RLCatalyst
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Please refer to ``Jenkins Task`` under :ref:`Orchestration-JenkinsTask` to **Create & Execute** Jenkins Task


**Following video demonstrates how to Create and Execute Jenkins Task in RLCatalyst**:


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/fM5nrBBJmko" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

*****


*****


.. _View Jenkins Job-History:

View Jenkins Job History
^^^^^^^^^^^^^^^^^^^^^^^^

Please refer to ``Jenkins Task`` -> ``Task History`` under :ref:`Orchestration-JenkinsTask` to view **Jenkins Job History**



*****