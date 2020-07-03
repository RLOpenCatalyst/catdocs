BOTs
====

BOTs is readymade automated scripts.

If you have not configured your BOTs setup, ask your admin to setup BOTs.

We have 3 types of BOTs:

* Check: These type of BOTs used to provide service management(start, stop, restart), monitoring services and chef provider is used to deliver these services

* Run: These type of BOTs used to launch any blueprint, upgrade any application and chef provider is used to deliver these services

* UI: These type of BOTs are used to provide different kind of services using UI automation(selenium) and jenkin is used to deliver these services

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

	.. image:: /images/bots.png

* click on execute button one popup will appear

.. image:: /images/botsexecute.png

* Select any Tag Server from the drop down

* Enter the parameters

* Now click on ok button 

* Execution will start.We can the logs through logs tab.

* We can also schedule the bots.


**How to schedule the BOT**

*Click on Bots tab.Click on any bot like "Terraform bot".Navigate to schedule tab.Enter the deatils like start date and end date  and choose minutes/hourly/daily/weekly/monthly and howmany times we want execute the bots.If yu want to execute the bot 
 with remote server enable the checkbox and If you want skip alternate runs in the execution enable the checkbox.Click on "schedule" button.
 
 image:: /images/Schedule_bot.PNG
 
 
 
 
 
 



