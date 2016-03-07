


.. _install-installer:


Install Using QuickInstaller
============================

RLCatalyst can be installed quickly using a chef-based installer. This installer will be available for installing on Centos, Ubuntu and Windows. The catalyst installer will install RLCatalyst and Open Source Chef. Basic seed data to start the application will also be taken care by the installer

**Ubuntu 14.04**

You can install RLCatalyst using the installer script ::

    sudo su
    cd /opt
    git clone https://github.com/RLOpenCatalyst/installer.git
    cd /opt/installer/vagrantwithchef/
    chmod +x installer.sh
    installer.sh 

.. _install-ami:

Install from AWS AMI
====================

If you have an AWS account, you can bring up RLCatalyst using the public AMI available. The public image is currently available for US east(N.Virginia) region. This comes with some basic configurations required by RLCatalyst

1. From your EC2 dashboard, select N.Virginia region . In the Images/AMI link, choose "Public Images" in the dropdown . Search for image with AMI ID ``ami-9a3903f0`` and AMI Name ``RLCatalyst3.0.3``
2. Select the image and hit Launch
3. On the "Instance Type" page ,choose the instance size as t2.medium or bigger . We recommend atleast 4 GB RAM
4. On the "Configure Instance Details" page, choose your preferred Network and Subnets. If you want to assign a public IP to RLCatalyst, then enable "Auto-assign Public IP"
5. On "Tag Instance" , name your instance
6. On "Security Group" , add rule to open ports 443 and 3001.
7. Review and launch . Once the instance is in "Running" state , you can access RLCatalyst at http://<ip>:3001 . Login using superadmin/superadmin@123

.. _install-vagrant:
Install using Vagrant
=====================
Setup RLCatalyst on your dektop/laptop using vagrant. You need to have vagrant installed in your machine::
    

    git clone https://github.com/RLOpenCatalyst/installer.git
    cd vagrantwithchef
    vagrant up


.. _install-docker:

Install using Docker Image
==========================
Coming in the next release ...

.. _install-vm:
Install using VM
================
Coming in the next release ...