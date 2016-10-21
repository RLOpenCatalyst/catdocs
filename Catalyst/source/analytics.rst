Analytics
=========

this section tells you the **cost of RLCatalyst** based on day wise, week wise, month wise or yearly basis.

Click on **Analytics** link in the header. Page has two tabs Dashboard and Reports. 


1. Dasboard: Bydefault it will show Dashboard details in the form of graph.

 .. image:: /images/updated_img/analyticsDashboard01.png

 .. image:: /images/updated_img/analyticsDashboard02.png

 Currently we can have data only in monthly basis, other options are disabled. We have total cost, and aggregated cost for different services EC2, S3, R53, other and etc throughout the month segregated by Business Group, Region, Environment and Provider. To show the graph we have to do the mapping in provider sync, mapping tag values with Business Group, Project and Environment respectively. Graphs are in three forms: 

 1. Aggregate Cost: It is a Pie Chart, which display all aggregated total cost details.

 2. Distribution of all services across Business Group: Here we have Bar chart, it is drill down of pie chart - grouped and stacked for services, in grouped the services would be available in single bar chart and in stacked the services would be in multiple bar charts.

 .. image:: /images/updated_img/analyticsDashboard03.png

 .. image:: /images/updated_img/analyticsDashboard04.png

 3. Daily trends of cost across organization: It is a Line chart, the data would be on daily basis accross organization.

2. Reports: In Reports tab the data will be in tabular form.

 .. image:: /images/updated_img/analyticsReports01.png

 We have few options available for the table, on the right side of the table

 .. image:: /images/updated_img/analyticsReports02.png 

 We can remove any colunm from the table by just clicking on the field name, let say remove "Total Cost"

 .. image:: /images/updated_img/analyticsReports03.png

 Now, "Total Cost" field is not available in the table.

 We have two more options "Export all data as cvs", it will export all data from the table in cvs format. And "Export visible data as cvs", it will save only the visible data from the table, it will not save the removed data from the table.

* Filter: We can filter the data on the basis of Organization and Provider.

 .. image:: /images/updated_img/analyticsFilter01.png

 If we want to filter the data on the basis of provider, we can select any provider from the drop down

 .. image:: /images/updated_img/analyticsFilter02.png







