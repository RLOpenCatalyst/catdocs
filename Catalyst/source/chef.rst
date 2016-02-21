.. _configure-chef:

Working With Chef
=================

Chef helps you express your infrastructure policy – how your software is delivered and maintained on your servers – as code. When infrastructure is code, it becomes more maintainable, versionable, testable, and collaborative.It allows you to install, configure and manage the packages required by your application without the complication of any client and server configuration. RL Catalyst allows you to use either chef or puppet configuration management to manage your Infrastructure.

To begin with you need to create your organization and an account in chef server to automate your infrastructure.

* Go to the below link and create an account in Chef

 **https://getchef.opscode.com/signup**


.. image:: /images/opscode.png


* Once you provide the details you will get the below message and email in your mailbox

 .. image:: /images/signup.png


* Check the email and go to the link provided in the email and provide the password

 .. image:: /images/emailChef.png


* Once you provided the password, you will get the below message

 .. image:: /images/welcomeChef.png 


* Create an Organization

 .. image:: /images/createOrgchef.png 

Done Now you have a Hosted Chef account.


* Goto The Administrator Tab

 .. image:: /images/saveOrg.png 


* Reset the Validation Key

 .. image:: /images/resetKey.png


 .. image:: /images/resettingKey.png


Download the key in your desktop


* Reset the User key

 .. image:: /images/resetUserkey.png


 .. image:: /images/resettingUserKey.png


Download the key


* Generate the Knife Configuration

 .. image:: /images/genKnife.png


So Now you have the user key, organization key and knife configuration


* Install Chef-Client on your desktop (Windows or Linux)

 **https://downloads.chef.io/chef-client/**


* Create a folder in any location and then under that create chef-repo and chef(windows) and .chef(linux)

The directory structure will be:


 .. image:: /images/dirStructure.png


Put all the files in the chef folder



* To check the connectivity from your workstation to the hosted chef server
 
 Just run any command

 .. image:: /images/knifeCmd.png


* clone the git repository to above directory

 **git clone https://github.com/RLOpenCatalyst/automationlibrary.git**



* Run the ruby program (cookbooks_upload_chef_server.rb) available in the git repo.

 **ruby cookbooks_upload_chef_server.rb**

It will upload all the cookbooks to the hosted chef server along with the dependencies.













































 




