


.. _install-installer:


Install Using QuickInstaller
============================

RLCatalyst can be installed quickly using a chef-based installer. This installer will be available for installing on Centos, Ubuntu and Windows. The catalyst installer will install RLCatalyst and Open Source Chef. Basic seed data to start the application will also be taken care by the installer

**Ubuntu 14.04 and Centos**

You can install RLCatalyst using the installer script ::

    wget https://raw.githubusercontent.com/RLOpenCatalyst/installer/master/installer.sh
    chmod +x installer.sh
    ./installer.sh

.. _install-Docker:
Install using Docker
====================

You can install RLCatalyst on Containers. Use below commands to pull docker images for catalyst::

    docker pull relevancelab/catalyst-db:latest
    docker pull relevancelab/rlcatalyst:4.0

and run below commands. ::

    docker run --name rlcdb -d relevancelab/catalyst-db:latest
    docker run --link rlcdb:rlcdb -e DB_HOST=rlcdb --name rlcat -d -p 3001:3001 relevancelab/rlcatalyst:4.0

Now you can access RLCatalyst using http://<hostip>:3001::

    Login Credentials

        UN:  superadmin 
        PWD: superadmin@123

.. _install-vagrant:
Install using Vagrant
=====================
Setup RLCatalyst on your dektop/laptop using vagrant. You need to have vagrant installed in your machine::
    
RL Catalyst Installation on Vagrant with chef::

    git clone https://github.com/RLOpenCatalyst/installer.git
    cd vagrantwithchef
    vagrant up

RL Catalyst Installation on Vagrant without chef::

    git clone https://github.com/RLOpenCatalyst/installer.git
    cd vagrant
    vagrant up

To install the entire devops roles along with catalyst please follow the below mentioned instructions::

    git clone https://github.com/RLOpenCatalyst/installer.git
    cd RLCatalyst3.0.4
    vagrant up

The devops roles contain the following third party softwares::
    
    Jenkins
    Nexus



.. _install-ami:

Install from AWS AMI
====================

If you have an AWS account, you can bring up RLCatalyst using the public AMI available. The public image is currently available for US east(N.Virginia) region. This comes with some basic configurations required by RLCatalyst

1. From your EC2 dashboard, select N.California region . In the Images/AMI link, choose "Public Images" in the dropdown . Search for image with AMI ID ``ami-f4270294`` and AMI Name ``RLCatalyst4.0.0-stage``
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

