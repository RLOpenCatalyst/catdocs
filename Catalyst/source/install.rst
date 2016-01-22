.. _install-Catalyst:

Installation
============

This is a documentation that gives the developer and the user an overview how to install Catalyst on a local instance.

Ubuntu
^^^^^^

Here is a step by step plan on how to install Catalyst on Ubuntu machine.

Install Java::

    sudo apt-get update
    sudo add-apt-repository ppa:webupd8team/java
    sudo apt-get install oracle-java8-installer
    sudo update-alternatives --config java
    java –version and javac –version


Install MongoDB

Import the public key used by the package management system.The Ubuntu package management tools (i.e. dpkg and apt) ensure package consistency and authenticity by requiring that distributors sign packages with GPG keys. 

Issue the following command to import the MongoDB public GPG Key::

    sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927

Create a list file for MongoDB::

    echo "deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list

Reload local package database & install MongoDB::

    sudo apt-get update
    sudo apt-get install -y mongodb-org

    [Alternate Way]

    sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
    echo "deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.0.list
    sudo apt-get update
    sudo apt-get install -y mongodb-org
    mongo

Install NodeJs::

     sudo apt-get update
     sudo apt-get install curl
     sudo curl -L https://www.opscode.com/chef/install.sh | sudo bash
     curl -L http://git.io/n-install | bash

To Install the Current Version 4.x supported by Catalyst::

    curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -sudo apt-get install -y nodejs

To Check the version of node::

    node -v

Install Git::

    sudo apt-get install git

Install npm::
    
    sudo apt-get update 
    sudo apt-get install npm -g
    Note: Catalyst currently supports node version 4.22 and npm version 3.4.x

Install knife and ChefClient::

    sudo apt-get update
    wget https://opscode-omnibus-packages.s3.amazonaws.com/ubuntu/12.04/x86_64/chef-server_11.0.10-1.ubuntu.12.04_amd64.deb
    sudo dpkg -i chef-server*

Install Catalyst::

    mkdir Catalyst
    cd Catalyst
    git clone https://www.github.com/RLIndia/D4D.git
    Note: This is will create a main folder D4D.(Inside D4D- client,server..)

Run the Server::

    cd D4D/server
    Install node packages - sudo npm install
    Install seed data - sudo node install --seed-data 
    Install Forever - sudo npm install forever --global
    Run the app - sudo forever start app.js

Any issues regarding the Mongo Running Status::

    sudo mongod
    sudo killall mongod
    sudo service mongod start

Set the Mongo Path(if required)::

    sudo mkdir -p /data/db/ 

To Run Mongo as a daemon::

    sudo update-rc.d mongodb defaults

Access Catalyst::
    
    localhost:3001
    username- superadmin
    pass - superadmin@123

