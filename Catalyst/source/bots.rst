BOTs
====

BOTs are readymade automated scripts.

If you have not configured your BOTs setup, ask your admin to setup BOTs.

* BOTs

	* :doc:`BOT Library <Botlibrary>`

	* :doc:`Audit Trail <Audittrail>`

	* :doc:`BOT Report <BOTreport>`

* :doc:`Runbooks <runbooks>`

We have 3 types of BOTs:

* Check: These type of BOTs used to provide service management(start, stop, restart), monitoring services and chef provider is used to deliver these services

* Run: These type of BOTs used to launch any blueprint, upgrade any application and chef provider is used to deliver these services

* UI: These type of BOTs are used to provide different kind of services using UI automation(selenium) and jenkins is used to deliver these services

These BOTs are used to provide following services:

* Active Directory: We can create user, delete user and reset password using Run type BOTs

* OpenDJ LDAP: We can create user, delete user and reset password using Run type BOTs

* Monitoring: We can use sensue to monitor any service using check BOTs

* Application Deployment: We can deploy new application on any machine using Run BOTs

* Service Management: We can start, stop, restart service using check BOTs 

* Upgrade: We can use Run BOTs to upgrade any service running on any machine

* Installation: We can install new services on any machine using Run BOTs


**How to execute BOTs**

* User can select any BOTs for execution

	.. image:: /images/updated_img/bots.png

* click on execute button one popup will appear

    .. image:: /images/updated_img/botsexecute.png

* Select any Tag Server from the drop down

* Enter the parameters

* Now click on ok button 

* Execution will start.We can see logs through logs tab.

* We can also schedule the BOTs.


**How to schedule the BOTs**

* Select any BOT in BOTs library then navigate to schedule tab in the BOT.

* Enter the details like start date and end date  and choose minutes/hourly/daily/weekly/monthly and how many times we want execute the BOT.

* If you want to execute the bot with remote server enable the checkbox .If you want skip alternate runs in the execution enable the checkbox.Click on "schedule" button.
 
   .. image:: /images/updated_img/Schedule_bot.png
 
 
**Remote Execution of BOTs**

* Select Service Manager BOT in BOTs library 

* Enter the input parameters : 1. Service Name(nginx) 2. Service Action (stop/start)

* select the checkbox : Do you want to execute on Remote Server? - and select the remote intstance that you want to stop the service nginx -192.1.1.2 and click on execute
 
  .. image:: /images/updated_img/remote_exe.png


 
 
 
 
