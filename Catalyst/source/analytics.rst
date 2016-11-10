Analytics
=========

Analytics is the cost, usage and capacity of cloud. Analytics unlocks more insightful questions and produces more accurate outcomes by mapping relationships among high volumes of connected data

**Prerequisites:** A cloud account should be added in RLCatalyst settings.

**How it is working:**

* Aggregate and graphically represent statistical AWS resource cost data at different granuralities across time intervals to assist end user to easily analyse and optimize resource usage.

* Collect and graphically represent usage trends data of provisioned AWS resources across time intervals to assist end user in identifying resource utilizations patterns and optimize deployment strategies.

* Provide APIs to access usage and cost analytics data at different granuralities across time intervals to enable automation of usage analysis to gain insights and to develop prediction algorithms based on these insights to optimize resource utilization and reduce cost.

**How to use:**

Click on **Analytics** link in the header. And we have three menu at the left side of the page:

1. Cost

2. Capacity

3. Usage

Cost
^^^^

Page has two tabs Dashboard and Reports. 


1. Dashboard: By default it will show Dashboard details in the form of graph. Dashboards let you monitor many data at once, so you can quickly check the health of your accounts or see correlations between different reports.

 .. image:: /images/updated_img/analyticsDashboard01.png

 .. image:: /images/updated_img/analyticsDashboard02.png

**AWS cost analytics:**

* Collect hourly costs for all AWS resources for all added providers.

* Aggregate hourly, daily, monthly and yearly costs for catalyst entities and provider specific entities based on resource allocation.

        - Catalyst entities: organization, business unit, project, environment, provider type, provider, resource

        - Provider specific entities: region, resource types (EC2, S3, RDS etc)

* Provide API to query for aggregated data based on catalyst and provider specific entities across time periods. Start date for aggregation shall be decided based on specified period. End date shall be specified by the consumer of the API

        - Periods: hour, month, day, year, 5 years, 10 years

* Provide APIs to query for resource cost trend for specific catalyst and provider specific entities across time periods, for specified intervals. Intervals shall be limited based on the specified period, limited by the cap of number of data points in the response. 

        - Intervals: hourly, daily, weekly, monthly, yearly

* Time series data will be stored with UTC timestamps

 We have total cost, and aggregated cost for different services EC2, S3, R53, other etc for the month segregated by Business Group, Region, Environment and Provider. To show the graph we have to do the mapping in provider sync, mapping tag values with Business Group, Project and Environment respectively. Graphs are in three forms: 

 1. Aggregate Cost: It is a Pie Chart, which display all aggregated total cost details.

 2. Distribution of all services across Business Group: Here we have Bar chart, it is drill down of pie chart - grouped and stacked for services, in grouped the services would be available in single bar chart and in stacked the services would be in multiple bar charts.

 .. image:: /images/updated_img/analyticsDashboard03.png

 .. image:: /images/updated_img/analyticsDashboard04.png

 3. Daily trends of cost across organization: It is a Line chart, the data would be on daily basis accross organization.

2. Reports: In Reports tab the data will be in tabular form Name, Total Cost, Services.

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







