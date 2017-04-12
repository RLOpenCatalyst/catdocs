
.. _install-source:

Install Directly From Source
============================
You can install RLCatalyst locally by downloading the code from our Github Code Repository. The following section gives the instructions to do the RLCatalyst Installation from source


Installation Steps for Ubuntu 16.04
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Here is a step by step plan on how to install RLCatalyst on Ubuntu machine.

Start by updating the System::
    
    sudo apt-get update

Install MongoDB

Import the public key used by the package management system.The Ubuntu package management tools (i.e. dpkg and apt) ensure package consistency and authenticity by requiring that distributors sign packages with GPG keys.

Issue the following command to import the MongoDB public GPG Key::

    sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927

Create a list file for MongoDB::

    echo "deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list

Reload local package database & install MongoDB::

    sudo apt-get update
    sudo apt-get install -y mongodb-org

Check the Mongo version::
    
    mongo -version
    3.2.x

Start the mongodb:

In order to properly launch MongoDB as a service on Ubuntu 16.04, we additionally need to create a unit file describing the service. A unit file tells system how to manage a resource. The most common unit type is a service, which determines how to start or stop the service, when should it be automatically started at boot, and whether it is dependent on other software to run.
We'll create a unit file to manage the MongoDB service. 

Create a configuration file named mongodb.service in the /etc/systemd/system directory using nano or your favorite text editor. ::

    sudo nano /etc/systemd/system/mongodb.service

Paste in the following contents, then save and close the file. ::

    [Unit]
    Description=High-performance, schema-free document-oriented database
    After=network.target


    [Service]
    User=mongodb
    ExecStart=/usr/bin/mongod --quiet --config /etc/mongod.conf


    [Install]
    WantedBy=multi-user.target


Next, start the newly created service with systemctl. ::

    sudo systemctl start mongodb

Use systemctl to check that the service has started properly. ::

    sudo systemctl status mongodb

Output::

    ● mongodb.service - High-performance, schema-free document-oriented database
       Loaded: loaded (/etc/systemd/system/mongodb.service; enabled; vendor preset: enabled)
       Active: active (running) since Mon 2016-04-25 14:57:20 EDT; 1min 30s ago
     Main PID: 4093 (mongod)
        Tasks: 16 (limit: 512)
       Memory: 47.1M
          CPU: 1.224s
       CGroup: /system.slice/mongodb.service
            └─4093 /usr/bin/mongod --quiet --config /etc/mongod.conf

Enable automatically starting MongoDB when the system starts. ::

    sudo systemctl enable mongodb


Install NodeJs 4.x & Curl::

    sudo apt-get install curl

To Install Nodejs version 4.x ::
    
    curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
    sudo apt-get install -y nodejs

Check the version of node after installation. It should be 4.2.2 ::

    node -v
    v4.2.2

Check the version of npm ::

    npm -v

    NOTE - The npm version required is 3.x . If an older version got installed, upgrade the npm version
           sudo apt-get update
           sudo npm install npm -g

    Now check the npm version and make sure it is 3.5.x and above
    npm -v

Install Git(1.9.x) ::

    sudo apt-get install git

NOTE::

    Node Version - 4.2.2
    npm version - 3.6.x
    monogo version - 3.2.x

Clone the repository to get the RLCatalyst code::

    sudo git clone https://github.com/RLOpenCatalyst/core.git

Create a Mongodb path::
    
    sudo mkdir -p /data/db/

Install ChefClient::

    sudo curl -L https://www.opscode.com/chef/install.sh | sudo bash
    
    To Check the chef client version
    knife -v
    It should be 12.6 or above

Install the dependencies- make , g++ , Kerberos & library::

    sudo apt-get install make
    sudo apt-get install g++
    sudo apt-get install libkrb5-dev
    sudo npm install -g kerberos
    sudo apt-get install ruby


To run the application we need to do a client side build as well:

Pre-requisites::

    1. Grunt-cli
        sudo npm install -g grunt-cli


    2. sass gem
        sudo gem install sass

Process to bluid the client side::

    cd core/client/cat3
    sudo npm install --production (any other environment)
    sudo npm run-script build-prod (any other environment)

Install Node Packages::

    cd core/server
    sudo npm install

To Install seed data::

    sudo node install --seed-data

To Install forever & start the RLCatalyst Application::

    sudo npm install forever –global
    cd core/server/app
    sudo forever start app.js

Now you can access RLCatalyst at http://localhost:3001 ::

    Login Credentials
    superadmin/superadmin@123

You are ready to start using RLCatalyst now. 
Please see :doc:`Getting Started <gettingstarted>` for next steps.


Installation Steps for Ubuntu 14.04
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Here is a step by step plan on how to install RLCatalyst on Ubuntu machine.

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
    
Start the mongodb::

    sudo service mongod start



Install NodeJs 4.x & Curl::

     sudo apt-get install curl

To Install Nodejs version 4.x::

     curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
     sudo apt-get install -y nodejs


Check the version of node after installation. It should be 4.2.2 and above ::

    node -v
    v4.2.2


Check the version of npm ::
    
    npm -v
  

    NOTE - The npm version required is 3.x . If an older version got installed, upgrade the npm version
           sudo apt-get update
           sudo npm install npm -g

    Now check the npm version and make sure it is 3.5.x and above
    npm -v
    




Install Git(1.9.x) ::

    sudo apt-get install git
    
    


NOTE::

    Node Version - 4.2.2 and above
    npm version - 3.6.x and above
    monogo version - 3.2.x


Clone the repository to get the RLCatalyst code::

    sudo git clone https://github.com/RLOpenCatalyst/core.git



Create a Mongodb path::

    sudo mkdir -p /data/db/ 



Install ChefClient::

    sudo curl -L https://www.opscode.com/chef/install.sh | sudo bash
    To Check the chef client version
    knife -v
    It should be 12.6 or above


Install the dependencies- make , g++ , Kerberos & library::

    sudo apt-get install make
    sudo apt-get install g++
    sudo apt-get install libkrb5-dev
    sudo npm install -g kerberos


To run the application we need to do a client side build as well:

Pre-requisites::

    1. Grunt-cli
        sudo npm install -g grunt-cli

    2. sass gem
        sudo apt-get install ruby
        sudo gem install sass 


Process to bluid the client side::

    cd core/client/cat3
    sudo npm install --production (any other environment)
    sudo npm run-script build-prod (any other environment)


Install Node Packages::

    cd ~
    cd core/server
    sudo npm install


To Install seed data::

    sudo node install --seed-data


To Install forever & start the RLCatalyst Application::

    sudo npm install forever --global
    cd ~
    cd core/server/app
    sudo forever start app.js


Now you can access RLCatalyst at http://localhost:3001 ::
    
    Login Credentials
    superadmin/superadmin@123


You are ready to start using RLCatalyst now. 
Please see :doc:`Getting Started <gettingstarted>` for next steps . 


Installation Steps for Centos7
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Here is a step by step plan on how to install RLCatalyst on Centos7 machine.

Update your System with yum::

    yum update



To Install node.js & npm::


    # Install the repository
    rpm -Uvh https://rpm.nodesource.com/pub_4.x/el/7/x86_64/nodesource-release-el7-1.noarch.rpm

    # Install NodeJS
    yum install nodejs

    checking the node version
    node -v
    4.2.2

    Check the npm version 
    npm -v
    


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



To Install RLCatalyst and to create a db path folder::

    To pull the catalyst code
    git clone https://github.com/RLOpenCatalyst/core.git
    Check the current directory for the presence of catalyst code i.e core folder.
    

    Create a db path folder
    mongo db path -  mkdir -p /data/db/

    Go to cd core/server
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
    cd core/server/app
    node app.js


To run the application forever::

    forever start app.js



Access RLCatalyst::

    http://localhost:3001
    username- superadmin
    pass - superadmin@123

Now you are ready to start using RLCatalyst . Please see :doc:`Getting Started <gettingstarted>` for next steps

