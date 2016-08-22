


.. _install-installer:


Install Using QuickInstaller
============================

RLCatalyst can be installed quickly using a chef-based installer. This installer will be available for installing on Centos, Ubuntu and Windows. The catalyst installer will install RLCatalyst and Open Source Chef. Basic seed data to start the application will also be taken care by the installer

**Ubuntu 14.04 and Centos**

You can install RLCatalyst using the installer script ::

    wget https://github.com/RLOpenCatalyst/installer/blob/master/installer.sh
    chmod +x installer.sh
    ./installer.sh


.. _install-docker:
Install using Docker
====================

Download the docker image from::

    https://hub.docker.com/r/relevancelab/opensc-catalyst/

and run these commands::

    docker pull relevancelab/opensc-catalyst
    docker run -d --name <any_name> -p <free_port>:3001 relevancelab/opensc-catalyst:3.0.5



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

1. From your EC2 dashboard, select N.California region . In the Images/AMI link, choose "Public Images" in the dropdown . Search for image with AMI ID ``ami-14e37203`` and AMI Name ``RLCatalyst3.2.0``
2. Select the image and hit Launch
3. On the "Instance Type" page ,choose the instance size as t2.medium or bigger . We recommend atleast 4 GB RAM
4. On the "Configure Instance Details" page, choose your preferred Network and Subnets. If you want to assign a public IP to RLCatalyst, then enable "Auto-assign Public IP"
5. On "Tag Instance" , name your instance
6. On "Security Group" , add rule to open ports 443, 8080,8081 and 3001.
7. Review and launch . Once the instance is in "Running" state , you can access RLCatalyst at http://<ip>:3001 . Login using superadmin/superadmin@123
8. This image includes the devops role like jenkins at http://<ip>:8080 (default credentials)
9. This image includes the devops role Nexus at http://<ip>:8081 (default credentials)




