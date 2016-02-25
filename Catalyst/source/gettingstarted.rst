Getting Started
===============

Install RLCatalyst
^^^^^^^^^^^^^^^^^^
RLCatalyst can be installed either directly from source or using one of our quickinstallers

**Install from Source** 

Refer to :ref:`install-source` to install RLCatalyst directly from source

**Quick Installer** 
	
RLCatalyst can be installed using one of our Quick Installers

**Quick install using RLCatalyst Public AWS Image** 

If you have an AWS account, you can bring up RLCatalyst using the public AMI available. The public image is currently available for US east(N.Virginia) region. This comes with some basic configurations required by RLCatalyst

1. From your EC2 dashboard, select N.Virginia region . In the Images/AMI link, choose "Public Images" in the dropdown . Search for image with AMI ID ``ami-b1e0d3db`` and AMI Name ``rlcatalyst``
2. Select the rlcatalyst image and hit Launch
3. On the "Instance Type" page ,choose the instance size as t2.medium or bigger . We recommend atleast 4 GB RAM
4. On the "Configure Instance Details" page, choose your preferred Network and Subnets. If you want to assign a public IP to RLCatalyst, then enable "Auto-assign Public IP"
5. On "Tag Instance" , name your instance
6. On "Security Group" , add rule to open ports 443 and 3001.
7. Review and launch . Once the instance is in "Running" state , you can access RLCatalyst at http://<ip>:3001 . Login using superadmin/superadmin@123



**Following video demonstrates how to Quick install using RLCatalyst public AWS Image:**
 

.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/tj-Ce5o6-So" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

*****


Import your existing Instance
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
You can import already existing node in to RL Catalyst using IP Address. The Node should have public IP Address and should be reachable from catalyst. Please refer to :ref:`import-byip`  for more help


Deploy a Test Application
^^^^^^^^^^^^^^^^^^^^^^^^^

**Deploy Tomcat Application on the Imported Node**

* Go to Orchestration, Create New **Chef Task** by adding **deploy_tomcat_war** cookbook to the **Runlist**, click on Edit **Cookbook Attribute** Icon and add **Source code URL** and Save

* Execute the Chef Task and wait until task executes successfully



**Following video demonstrates how to do Import By IP and Deploy Tomcat Application in RLCatalyst:**






*****

Add Provider and do Provider Sync
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Once the basic data is loaded, you can start exploring RLCatalyst from the Provider-Sync Feature. You can sync nodes from your AWS provider account and convert the nodes to 'Managed' . This will give a control on your AWS infra by letting you track the capacity, cost and usage . Once sync-ed, you can see the summary dashboard from 'Track'


1. **Add your AWS provider** account details in RLCatalyst . Refer to :ref:`provider-settings` for more help
2. **Sync your provider with RLCatalyst**. Once the provider account is added, you can start importing the nodes into RLCatalyst . Importing will bootstrap the nodes with the configured chef server . The imported instances can be managed from the workzone, under the project and environment to which the nodes are imported. Refer to :ref:`provider-sync` for more help



**Following video demonstrates how to add provider and do sync in RLCatalyst:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/HIMlbwtc8Zc" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****


Create Template, VM Image, Blueprints
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. **Create new Templates** . RLCatalyst provides you with the flexibility to create re-usable Templates for Infra and app automation. By default, it supports 4 types of templates . You can add templates for any of these template types . Refer to :ref:`configure-softwarestack` for more help
2. **Add VM Images** for the providers. Add VM Images for your each of the provider accounts added. This could be any of the images(public/private) accessible from your provider account. The templates will use these as the base to launch new instances . Refer to :ref:`configure-vm` for more help
3. **Create a blueprint** for a software stack . Once the templates and VM Images are added, next step is to design blueprints, which are tied to a provider. Refer to :ref:`design-blueprint` for more help
4. **Launch the blueprints** to create new instance and boootstrap with the runlist added in the blueprint . The new instances will be listed under 'Instances' for the specified project and environment . Refer to  :ref:`launch-instances` for more details



**Following video demonstrates how to create Templates, VM Images and Blueprints in RLCatalyst:**


.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/Hg6kFMLruaY" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>



*****


Application  Deployment
^^^^^^^^^^^^^^^^^^^^^^^

You can now deploy your application in one-click in RLCatalyst . RLCatalyst gets the build or the source from the repository which is associated with the application. The repository need to be configured in RLCatalyst and should be associated with a Project . Currently Docker and Nexus repositories are supported.
  
**Pre-requisites** 


1. A repository (Nexus/Docker) should be added from Settings 
2. Repository should be attached to one or more projects. 
3. There should be connectivity between the repository, the target instances and the RLCatalyst instance
4. There should be to & fro connectivity between RLCatalyst and the target instance


Follow the instructions to deploy an application from Nexus repository

1. Add the Nexus server details in RLCatalyst and associate the repository to a Project. Refer to  :ref:`configure-nexus` for more details.
2. Create new blueprint to  deploy the application . Refer to :ref:`create-app-blueprint` for more details
3. Launch a new instance using the blueprint  . Refer to :ref:`launch-app-blueprint` for more details
4. Update the application to the latest version and see the application running at the URL configured. Refer to :ref:`upgrade-app` for more details


*****
        
View Cost and Usage Dashboards
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

RLCatalyst provides you a consolidated dashboard for tracking your AWS infrastructure cost and usage . This helps you to identify un-used capacity and do better utilization. RLCatalyst summarizes this data for all the AWS provider accounts configured
            
Follow the instructions to configure your dashboards:

1. **Configure the provider dashboard** in Settings . This will give you the snapshot of instances- Total Number vs Number of Managed vs Number of Un-Managed. Refer to :ref:`configure-track` for more details
     
2. A more detailed dashboard on AWS usage and cost can also be configured. This will give you the snapshot of Total cost, Daily cost etc . Refer to :ref:`configure-track` for more details

3. View the Dashboards from **RLCatalyst->Track**





