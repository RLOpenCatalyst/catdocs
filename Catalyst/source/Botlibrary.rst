BOTs Library
-------------

BOTs Library contains information about BOTs.There is a two buttons at top right corner of the page one for refresh the page and second one is filter. In the filter we have options like functionality ,action and type.

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
 
We can know the  information about the BOTs through the cards color and cards count.

 * We can see the total BOTs count with light blue color card.

 * We can see the total passed runs count with green color card.

 * We can see the total failed runs count with red color card. 

 * We can see the tickets resolved count with blue color card.

 * We can see the saved time with yellow color card.

     .. image:: /images/updated_img/count.png
	 
When you clicked on any card it will display options like total,day,week,month and custom.When you clicked on any option it will display following information:

+-------+----------+-------------+--------+------------+------------+-------------+
| Name  | category | Description | status | priority   | created at | Resolved at |
+-------+----------+-------------+--------+------------+------------+-------------+

We can see the old records with *custom* field.Fill the details like start date and end date later click on search button.

 .. image:: /images/updated_img/custom.png
	 
When you clicked on **Grid** tab it will display BOTs in grid view. When you clicked on **List** tab display bots in list view.

     .. image:: /images/updated_img/Grid.png
 
We can search the BOTs through search button.Type BOTs first word in the search button than it will display related BOTs. For example type Test in the search button it will display test related BOTs in the page.
 
  .. image:: /images/updated_img/list_view.png
  
 

