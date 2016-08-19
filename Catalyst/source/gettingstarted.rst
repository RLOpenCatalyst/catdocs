Getting Started
===============

Install RLCatalyst
^^^^^^^^^^^^^^^^^^
RLCatalyst can be installed either directly from source or using one of our quickinstallers

**Quick Installer** 
    
RLCatalyst can be installed using one of our Quick Installers

**Quick install using RLCatalyst Installer Script** 

RLCatalyst can be installed quickly using a chef-based installer. This installer will be available for installing on Centos and Ubuntu . The catalyst installer will install RLCatalyst and Open Source Chef. Basic seed data to start the application will also be taken care by the installer

**Ubuntu 14.04 and Centos**

You can install RLCatalyst using the installer script ::

    
    wget https://raw.githubusercontent.com/RLOpenCatalyst/installer/master/installer.sh
    chmod +x installer.sh
    ./installer.sh

**Quick install using Vagrant** 

Setup RLCatalyst on your dektop/laptop using vagrant. You need to have vagrant installed in your machine:
    
RL Catalyst Installation on Vagrant with chef::

    git clone https://github.com/RLOpenCatalyst/installer.git
    cd vagrantwithchef
    vagrant up

RL Catalyst Installation on Vagrant without chef::

    git clone https://github.com/RLOpenCatalyst/installer.git
    cd vagrant
    vagrant up


**Quick install using RLCatalyst Public AWS Image** 

If you have an AWS account, you can bring up RLCatalyst using the public AMI available. The public image is currently available for US east(N.Virginia) region. This comes with some basic configurations required by RLCatalyst

1. From your EC2 dashboard, select N.California region . In the Images/AMI link, choose "Public Images" in the dropdown . Search for image with AMI ID ``ami-14e37203`` and AMI Name ``RLCatalyst3.2.0``
2. Select the image and hit Launch
3. On the "Instance Type" page ,choose the instance size as t2.medium or bigger . We recommend atleast 4 GB RAM
4. On the "Configure Instance Details" page, choose your preferred Network and Subnets. If you want to assign a public IP to RLCatalyst, then enable "Auto-assign Public IP"
5. On "Tag Instance" , name your instance
6. On "Security Group" , add rule to open ports 443, 8080,8081 and 3001.
7. Review and launch . Once the instance is in "Running" state , you can access RLCatalyst at http://<ip>:3001 . Login using superadmin/superadmin@123
8. This image includes the devops role like jenkins at http://<ip>:8080 (default credentials)
9. This image includes the devops role Nexus at http://<ip>:8081 (default credentials)



**Following video demonstrates how to Quick install using RLCatalyst public AWS Image:**
 

.. raw:: html

    
    <div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
        <iframe src="https://www.youtube.com/embed/tj-Ce5o6-So" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

*****

**Install from Source** 

Refer to :ref:`install-source` to install RLCatalyst directly from source



Working with RL Catalyst
^^^^^^^^^^^^^^^^^^^^^^^^

Basic Scenarios - Using RLCatalyst Instance
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Once you install RLCatalyst , basic data to quick-start your experience will be available within the application - Organization setup, chef server , environments, templates, services etc . You can start exploring  by importing RLCatalyst instance into Catalyst

Listed below are few features which RLCatalyst offers out of the box:

* :ref:`Import Linux Node and Install latest version of-Tomcat`  

* :ref:`Install Apache on imported node and use service to stop, start and restart-Apache`     

* :ref:`Deploy Pet-clinic application in the imported node`    

* :ref:`Update Petclinic application-version`    

* :ref:`View History of App deployments &-upgrades`

* :ref:`Deploy a multi-tier application using docker-container`



*****


Advanced Features with Cloud Providers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^                 
Prerequisite : An AWS account should be available

RLCatalyst comes with the flexibility to create blueprints to automate dynamic provisioning on the cloud provider of your choice . Currently AWS, Azure, VMware and Openstack are supported. To start experiencing, add your provider account details in RLCatalyst

* :ref:`Launch New Ubuntu Instance and Install-Jboss`         

* :ref:`Deploy Windows App on-IIS`                

* :ref:`Launch New ubuntu Instance,Install Tomcat,upgrade to-v8.0[attribute]` 

* :ref:`Provider Sync and-Import Instances`  
           
* :ref:`AWS Cost,Usage-Dashboards`     

* :ref:`Deploy Wordpress on multiple docker-container`

* :ref:`Create CentOS instance and launch-Liferay`

* :ref:`Create and Launch an AWS CFT Blueprint for 2-node Petclinic`

* :ref:`Install LAMP Stack on a single-node`



*****



Advanced Continuous Integration & Continuous Deployment [CI/CD] Features
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Jenkins is CI/CD tool which can be used for build and deployment automation. It also allows you to continuously deliver your software by providing powerful ways to define your build pipelines and integrating with a large number of testing and deployment technologies.

**How to Configure, Create, Execute Jenkins Jobs and View History in RLCatalyst ?**

* :ref:`Create & Execute Jenkins Jobs from-RLCatalyst`

* :ref:`Deploy and Promote-a Java Application`

* :ref:`Deploy-a 3-tier application`

* :ref:`Update tags in-AWS`

* :ref:`Application Deployment During Instance Launch using-Nexus Server`

* :ref:`Create Composite-Blueprint`

* :ref:`Audit-Trail`

* :ref:`Script-Gallery`

*****








