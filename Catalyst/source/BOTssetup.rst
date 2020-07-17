BOTs 
^^^^^

BOTs are ready-made automated scripts.

If you have not configured your BOTs setup, ask your admin to set up BOTs.

***********

BOT Executor
^^^^^^^^^^^^

BOT is nothing but a piece of an Automation. It would be in the form of scripts, cookbooks etc..It can start the work<<Execute the task<<stop.RLCatalyst BOTs Factory work as the job scheduler.

Connect RLCatalyst to BOT Executor 
---------------------------------

Please follow the below steps in order to configure the Executor from Catalyst UI

* Login to the Catalyst UI >> Go to the Settings >> Move your cursor on Menu (Top left side) >> Click on BOTs >> Click BOTs Executor

* Now Click on New (Top  Right side) >> Give the Name of the Executor >> Select Organisation >> Put the BOT engine IP in BotEngine URL section >> Put 2687  in Host Port >> Select the same OS of the Botengine Machine. >> Click Save. 

*  When the BOTs Server executes a BOT, it chooses the appropriate executor based on the type of BOT. E.g. Linux BOT will run on Linux executor only. If an appropriate executor is not configured or available, the execution will fail.

  .. image:: /images/updated_img/botexecutor_new.png


Follow the steps to make your executor Active and Inactive
----------------------------------------------------------

* Login to the Catalyst UI >> Go to the Settings >> Move your cursor on Menu (Top left side) >> Click on BOTs >> Click BOTs Executor >> Click on the edit button (Pencil)

* Now click active or inactive as per your requirement >> Click on the Save button 

 .. image:: /images/updated_img/active_bot.png
 
 ************
 
 ServiceNow Server
 ^^^^^^^^^^^^^^^^^^
 
 ServiceNow is a software platform which supports IT Service Management (ITSM). It helps you to automate IT Business Management.This is cloud-based platform.We are configuring ServiceNow with catalyst to get the BOT ticket details. BOTs Server can integrate with ITSM platform like ServiceNow to integrate with the ITSM process.


 Connect ServiceNow server with RLCatalyst
 ------------------------------------------
 
 Please follow the below steps in order to configure the ServiceNow  from Catalyst UI
 
 *  Login to the Catalyst UI >> Go to the Settings >> Move your cursor on Menu (Top left side) >> Click on BOTs >> Click ServiceNow server
 
 *  Now Click on New (Top  Right side) >> Give the Name of configuration >> give URL of ServiceNow >>provide ServiceNow username and password details<<select orgarnization<<click on save button
 
 
   .. image:: /images/updated_img/service_new.png

 


