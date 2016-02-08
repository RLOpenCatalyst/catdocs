.. _install-Catalyst:

Installation
============
This is a documentation that gives the developer and the user an overview of how to install Catalyst on a local instance 

**Supported Platforms**

RLCatalyst is currently supported on
 * Ubuntu 14.04
 * CentOS 7

Software Requirements
^^^^^^^^^^^^^^^^^^^^^

     ===========     ==========================================================
     Softwares       Versions
     ===========     ==========================================================
     MongoDB         3.2
     Node.JS         4.22 and above
     Npm             3.4 and above
     Chef Server     12.3 Open Source or Latest Enterprise Chef Server version.
     Chef Client     12.6
     LDAP Server     OpenLDAP 2.4.39 or an existing corporate LDAP server.
     ===========     ==========================================================
    
    SCM – Any version of GIT or SVN

Catalyst can be installed using one of the following methods

Install Directly From Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
You can install Catalyst locally by downloading the code from our Github Code Repository. The following section gives the instructions to do the Catalyst Installation from source

Installation Steps for Ubuntu
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Here is a step by step plan on how to install Catalyst on Ubuntu machine.

Start by updating the System::

    sudo apt-get update


Install MongoDB

Import the public key used by the package management system.The Ubuntu package management tools (i.e. dpkg and apt) ensure package consistency and authenticity by requiring that distributors sign packages with GPG keys. 

Issue the following command to import the MongoDB public GPG Key::

    sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927

Create a list file for MongoDB::

    echo "deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list

Reload local package database & install MongoDB::

    sudo apt-get update
    sudo apt-get install -y mongodb-org


Check the Mongo version::

    mongo -version
    3.2.x
    




Install NodeJs 4.x & Curl::

     sudo apt-get install curl

To Install Nodejs version 4.x::

     curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
     sudo apt-get install -y nodejs


Check the version of node after installation.It should be 4.2.x ::

    node -v
    v4.2.x


Check the version of npm ::
    
    npm -v
    2.4.x

    NOTE - The npm version required is 3.6.x . If an older version got installed, upgrade the npm version
           sudo apt-get update
           sudo npm install npm -g

    Now check the npm version
    npm -v
    3.6.x




Install Git(1.9.x) ::

    sudo apt-get install git
    
    


NOTE::

    Node Version - 4.2.x
    npm version - 3.4.x
    monogo version - 3.2.x


Clone the repository to get the Catalyst code::

    sudo git clone https://github.com/RLOpenCatalyst/D4D.git



Create a Mongodb path::

    sudo mkdir -p /data/db/ 



Install ChefClient::

    sudo curl -L https://www.opscode.com/chef/install.sh | sudo bash
    To Check the chef client version
    knife -v
    12.6.x


Install the make , g++ , Keerberos & library::

    sudo apt-get install make
    sudo apt-get install g++
    sudo apt-get install libkrb5-dev
    sudo npm install -g kerberos



Run the Server::

    cd D4D/server
    Install node packages - sudo npm install


To Install seed data::

    sudo node install --seed-data


To Install forever & start the catalyst Application::

    sudo npm install forever --global
    Run the app - sudo forever start app.js


Now you can access RLCatalyst at http://localhost:3001 ::
    
    Login Credentials
    superadmin/superadmin@123


Installation Steps for Centos7
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Here is a step by step plan on how to install Catalyst on Centos7 machine.

Update your System with yum::

    yum update



To Install node.js & npm::


    # Install the repository
    rpm -Uvh https://rpm.nodesource.com/pub_4.x/el/7/x86_64/nodesource-release-el7-1.noarch.rpm

    # Install NodeJS
    yum install nodejs

    checking the node version
    node -v
    4.2.5

    Check the npm version 
    npm -v
    2.4.12


    NOTE - The npm version required is 3.5.x . If an older version got installed, upgrade the npm version.
           npm install npm -g
    
    Now check the npm version
    npm -v
    3.5.3 




To Install MongoDb (version 3.x)::

    Go to directory /etc/yum.repos.d/

    Create a file mongodb-enterprise.repo
    cat > mongodb-enterprise.repo
    Edit the above file and add the contents

    [MongoDB]
    name=MongoDB Repository
    baseurl=http://repo.mongodb.org/yum/redhat/$releasever/mongodb-org/3.2/x86_64/
    gpgcheck=0
    enabled=1

    Save the file 

    Run the Command 
    yum install mongodb-org

    check the mongo version
    mongod --version
    3.2.1
    

NOTE::

             npm version 3.5.3
             node version 4.2.5
             monogd verison 3.2.1




To Install Chef-Client (version 12.6.0)::
    

    curl -L https://www.opscode.com/chef/install.sh | sudo bash
    To check the chef client version
    knife -v
    Chef:12.6.0



To Install git::

    yum install git
    To check the git version
    git –version
    1.7.x



To Install Catalyst and to create a db path folder::

    To pull the catalyst code
        git clone https://github.com/RLOpenCatalyst/D4D.git
    Check the current directory for the presence of catalyst code i.e D4D folder.
    
    NOTE – Take the latest code from dev_catalyst.

    Run the command
    git status
    git checkout dev_catalyst
    git pull

    Create a db path folder
    mongo db path -  mkdir -p /data/db/

    Go to cd D4D/server
    npm install

Start the mongodb::
    
    sudo service mongod start

To Install gcc library::
 
    yum install gcc-c++


To Install the seed data::

    node install --seed-data


To Start the Application::

    Run (node app) to start your application.
    npm install forever –g
    node start app.js


To run the application forever::

    forever start app.js



Access Catalyst::

    localhost:3001
    username- superadmin
    pass - superadmin@123
    
Install Using QuickInstaller  
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
RLCatalyst can be installed quickly using a chef-based installer. This installer will be available for installing on Centos, Ubuntu and Windows. The catalyst installer will install RLCatalyst and Open Source Chef. Basic seed data to start the application will also be taken care by the installer

Please download the installer from <Link>
