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

1. From your EC2 dashboard, select N.Virginia region . In the Images/AMI link, choose "Public Images" in the dropdown . Search for image with AMI ID ``ami-468cb02c`` and AMI Name ``RLCatalyst3.0.2``
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

**Quick install using RLCatalyst Installer Script** 

RLCatalyst can be installed quickly using a chef-based installer. This installer will be available for installing on Centos and Ubuntu . The catalyst installer will install RLCatalyst and Open Source Chef. Basic seed data to start the application will also be taken care by the installer

**Ubuntu 14.04**

You can install RLCatalyst using the installer script ::

    sudo su
    cd /opt
    git clone https://github.com/RLOpenCatalyst/installer.git
    cd /opt/installer/vagrantwithchef/
    chmod +x installer.sh
    installer.sh 



Working with RL Catalyst
^^^^^^^^^^^^^^^^^^^^^^^^


* :ref:`Import Linux Node and Install latest version of-Tomcat`     

* :ref:`Launch New Ubuntu instance and Install-Jboss`

* :ref:`Launch New CentOS Instance and Install-Liferay`          

* :ref:`Launch Windows Instance and Install-IIS`

* :ref:`Launch Windows Instance and Install-myshopper`                   

* :ref:`Provider Sync and-Import Instances`                                           

* :ref:`Launch Ubuntu Instance and run Docker container for-Wordpress`

* :ref:`Install apache2 on imported node and use service to stop-apache2`        

* :ref:`Import Ubuntu Node and Deploy-petclinic`                        

* :ref:`Launch New ubuntu Instance,Install Tomcat,upgrade to-v8.0[attribute]` 

* :ref:`Update application-version[petclinic]`                  

* :ref:`View History of App deployments &-upgrades`  
           
* :ref:`AWS Cost,Usage-dashboards`                               

* :ref:`Launch Java stack using-CFT`

* :ref:`ARM with 2-VirtualMachines[VM]`                                    

* :ref:`Composite-Docker`




*****







