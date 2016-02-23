


.. _install-installer:


Install Using QuickInstaller
============================

RLCatalyst can be installed quickly using a chef-based installer. This installer will be available for installing on Centos, Ubuntu and Windows. The catalyst installer will install RLCatalyst and Open Source Chef. Basic seed data to start the application will also be taken care by the installer

Please download the installer from https://github.com/RLOpenCatalyst/RLCatInstallers

 **How to Run the script**

1. Move installer.sh into the folder in which you are installing RLCatalyst
2. Run ./installer.sh
3. If you have a Chef server, please skip the part to install Chef server.Once Catalyst is installed, go ahead and add your chef server details in Settings
4. If you dont have a Chef server, please follow the instructions from the installer script

.. _install-ami:

Install from AWS AMI
====================

If you have an AWS account, you can bring up RLCatalyst using the public AMI available. The public image is currently available for US east(N.Virginia) region. This comes with some basic configurations required by RLCatalyst

1. From your EC2 dashboard, select N.Virginia region . In the Images/AMI link, choose "Public Images" in the dropdown . Search for image with AMI ID ``ami-b1e0d3db`` and AMI Name ``rlcatalyst``
2. Select the rlcatalyst image and hit Launch
3. On the "Instance Type" page ,choose the instance size as t2.medium or bigger . We recommend atleast 4 GB RAM
4. On the "Configure Instance Details" page, choose your preferred Network and Subnets. If you want to assign a public IP to RLCatalyst, then enable "Auto-assign Public IP"
5. On "Tag Instance" , name your instance
6. On "Security Group" , add rule to open ports 443 and 3001.
7. Review and launch . Once the instance is in "Running" state , you can access RLCatalyst at http://<ip>:3001 . Login using superadmin/superadmin@123

.. _install-vagrant:
Install using Vagrant
=====================

.. _install-docker:

Install using Docker Image
==========================

.. _install-vm:
Install using VM
================