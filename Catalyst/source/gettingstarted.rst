Getting Started
===============

Got RLCatalyst installed? if not, please refer to  :doc:`Installation <install>`

**Workflow of Cataylst**

 When Catalyst is installed successfully and on logging into the application by default Organization, Business Group, Project are already Present. If you want to create New **Organization**, **Business group** and **Project** Follow these steps.

Flow1 : **Add seed Data into Catalyst**
   
  * Organization,Business Groups,Projects

  Step1: Create Organization
   1. Go to **Settings** -> **Organization Setup** -> **Organizations** -> **Add New Organization**
   2. Enter the **Organization Name**, **Domain Name** and **Save**


  Step2: Create Business Groups
   1. Click on **Settings** -> **Organization Setup** -> **Business Groups** -> **Add New Business Group**
   2. Enter the **Business Group Name**, **select the Org** and **Save** 
    

  Step3: Create Projects
   1. Click on **Settings** -> **Organization Setup** -> **Projects** -> **Add New Business Group**
   2. Enter the **Project Name**, **select the Org**, **select the Business Group** and **Save** 


  Step4: Create Chef Server
   1. Click on **Settings** -> **Organization Setup** -> **Chef Server** -> **Add New Chef Server**
   2. Enter the **Name** -> **UserName** -> **URL** -> select the **Organization** -> Upload **User Pem,Knife.rb** and **Save** 


  Step5: Create Environments
   1. Click on **Settings** -> **Environments** -> **Add New Environments/Select Environments**
   2. Select the **Organization,Chef Server** -> select the **Environment OR Add New Environment by clicking on Add link** and **Save** 

  Step6: Create Users
   1. Click on **Settings** -> **Users Setup** -> **Users** -> **Add New Users**
   2. Enter the **Login Name** -> **Email Address** -> Enter **Password** -> Enter **Confirm Password** -> Select the **Organization** -> Select the **Role** -> **Assign Team** and **Save** 


  Step7: Create Teams
   1. Click on **Settings** -> **Users Setup** -> **Teams** -> **Add New Teams**
   2. Enter the **Name** -> Select the **Organization** -> Select the **User** ->  Assign the **Project** and **Save** 



Flow2 : **Add Provider and do Provider Sync**

  * Create Provider & Provider-Sync

  Step1: Create Provider
   1. Click on **Settings** -> **Devops Setup** -> **Providers**
   2. Select ** Provider Type** as **AWS** -> Enter **Name** -> Enter valid **Access key , Secret Key ** -> Select **Organization Name** -> Select **Region, Key Pair and uplaod the pem file for provider** and **Save** Button

  Step2: Sync Provider
   1. Click on **Settings** -> **Devops Setup** -> **Providers** - > **Sync Instances**  
   2. Click on **UnManaged Instances** -> Select the **checkbox** of the node to be imported and click **Import Instances** button.
   3. Choose the **Rganization**, **Business group**, **Project** , **Environment** , **Config Management** ,**Username** , Chooose **Authentication Type** , Enter **Password** or Upload **Pemfile** -> Click **Sync** button. -> Close the Node Imported window.
   4. Click on **Workzone** -> Clcik on the *Environment** where you imported Node -> Synced Instances should be present in the environment.
   5. Click on **Settings** -> **Devops Setup** -> **Providers** - > **Sync Instances** -> Synced Instances should be presentin Managed Instances tab.




Flow3 : **Create Template, VM Image, Blueprints**

  * Templates,VM Image,Blueprints

  Step1: Creation of New Templates 
   1. Click on **Settings** -> **Gallery Setup** -> **Templates** -> **Add New Templates**
    
    **SoftwareStack Template**
     2. Enter the **Template Name** -> Choose **Template Type[SoftwareStack] ,Org** and **Save**
  

    **CloudFormation Template**
     2. Enter the **Template Name** -> Choose **Template Type[CloudFormation] ,Org** -> Upload **Template File** and **Save**

    **Azure ARM Template**
     2. Enter the **Template Name** -> Choose **Template Type[ARMTemplate] ,Org** -> Upload **Template File** and **Save**

    **Docker Template**
     **NOTE-** a. You can create docker template for Private Repo and also for Public Repo.

              b. To create Docker Template for Private Repo, Select Docker Repo in the dropdown and add valid private docker repo path.

              c. To create Docker Template for Public Repo donot select any docker repo in the dropdown and and valid public docker repo path.

      2. Enter the **Template Name** -> Choose **Template Type[Docker] ,Org**, **public/private** repo and **Save**   

    


  Step2: Create VM Images
   1. Click on **Settings** -> **Gallery Setup** -> **VM Image** -> **Add New VM Images**

   2. Enter the **Image Name** -> **Choose Org** -> Choose the respective **Provider, Operating System** -> Enter **Image ID, Admin User Name, Admin Password**


  Step3: **Create Software Stack Blueprint**
          1. Go to **Design** -> select **AWS** provider -> select **SoftwareStack** Template type -> select your **Template** -> Select the **OS, Provider, Image, Region, VPC, Subnet, KeyPair, Instance Type, Security Group, Organization**, Enter **Blueprint Name**, Choose **Business group, Project**, Configure Runlist by adding **Cookbooks and Roles** and Save.

          2. You can View your Blueprint in **Workzone** -> **Infrastructure** -> **Blueprints** -> Under **SoftwareStack**.

        **Create Docker Blueprint**
         1. Go to **Design** -> select **AWS** provider -> select **Docker** Template type -> select your **Template** -> Enter **Blueprint Name** -> Choose **Business Group, Project** -> **Launch Parameters icon[Add the other details based on docker images for public/private reposs]** and Save.

         2. You can View your Blueprint in **Workzone** -> **Infrastructure** -> **Blueprints** -> Under **Docker**.
       
        **Create Cloud Formation Blueprint**
         1. Go to **Design** -> select **AWS** provider -> select **Cloud Formation** Template type -> select your **Template** -> Enter **Blueprint Name** -> Choose **Org , Business Group , Project** -> Select **Region, Provider** and add other details based on your template file. 
         
         2. You can View your Blueprint in **Workzone** -> **Infrastructure** -> **Blueprints** -> Under **CloudFormation**.

        **Create Azure ARM Template**
         **NOTE** - Make sure You have created Resource group in your Azure portal
          1. Go to **Design** -> select **AZURE** provider -> select **ARM Template** Template type -> select your **Template** -> Enter **Blueprint Name**, Choose **Org , Business Group , Project** -> Select **Provider, Resource Group** and add other details based on your template file. 

          2. You can View your Blueprint in **Workzone** -> **Infrastructure** -> **Blueprints** -> Under **ARMTemplate**.


**Launch Blueprints**
 * **Software Stack Blueprint** - Go to **Workzone** -> **Infrastructure** -> **Blueprints** -> **Software Stack** -> select the Blueprint and Launch -> Verify the newly launched Instance under **Instances**.

 * **Cloud Formation Blueprint** - Go to **Workzone** -> **Infrastructure** -> **Blueprints** -> **CloudFormation** -> select the Blueprint and Launch -> Enter **Unique Stack Name** -> Verify the **CFT-Stack** under **Infrastructure** -> **CloudFormation** and wait until stack shows **CREATE_COMPLETE**. Verify the newly launched Instance under **Instances** with your stack name.

 * **Azure ARM Blueprint** - Go to **Workzone** -> **Infrastructure** -> **Blueprints** -> **ARMTemplate** -> select the Blueprint and Launch -> Enter **Deployment Name** -> Verify the **ARM-Deployment** under **Infrastructure** -> **AzureARM** and newly launched Instance under **Instances** with your deployment name.

 * **Docker Blueprint**
   
   Step1: Identify Ubuntu Instance which is already launched and Run Docker Cookbook on that node
    1. Cliik on **Workzone** -> **Infrastructure** -> **Instances** tab
    2. Click on **Chef Client run** icon -> Serach for **docker** cookbook -> Clcik on ** > ** icon to move to runlist.
    3. Click on **Update Runlist** button -> Click **OK** button in the confirmation popup -> Wait untill "instance runlist updated" logs is displayed.
    4. Close the Instance logs window
    5. Verify Docker image is displayed on the instances after few seconds.

   Step2: Launching docker blueprints
    1. Click on **Workzone** -> **Infrastructure** -> **Blueprints** tab
    2. Click **+** icon for Docker
    3. Select the blueprint and click on **Launch** button  
    4. Click **Ok** button in confirmation popup 
    5. Click **Next** button in **Launch Docker Blueprint** window.
    6. Select the ubuntu Instance in which docker cookbook is installed in Step1
    7. Click on **Start** button.
    8. Wait untill image pull completes.
    9. Close the Instance logs window.
    10. Click on **Infrastructure** -> **Containers** -> verify container is launched with the columns details **Actions**  **State** , **Created**, **Name** , **Instance IP**, **Container ID** , **Image** , **Info**



Flow4 : **App Deploy**

  * Application Deployment

  Step1: Configure Nexus Server
   1. Click on **Settings** -> **Devops Setup** -> **Nexus Server**
   2. Enter **Nexus Server Name** , **User Name** , **Password** , **Nexus Server URL** -> Select **Organization Name** -> Click on ** + ** icon to add Nexus Group ID        -> Enter **Nexus Group ID** and click **Save** Button

  Step2: Associate Repository Details to your Project
   1. Click on **Settings** -> **Organization Setup** -> **Projects** -> Click on **Edit** icon
   2. Click on ** + ** icon to add Repository Details.
   3. Select **Nexus Server** and choose the **Repository** and click **Save** Button

  Step3: Create New Blueprint and Deploy application during Bootstrap
   1. Click on **Design** link at the top -> Choose **Software Stack** Template type and click **Next** button
   2. Choose the **Template** and and click **Next** button
   3. Choose Operating System as **Ubuntu** -> Choose the **Provider** -> Choose the **VMImage** -> Choose **Region** ->Select **VPC** -> Select **SUbnet** -> Select **KeyPair** -> Select **Instance Type** -> Select **Security Group** -> Select **Instances to Launch** as **1**.
   4. Click on **Configure Organization Parameters** -> Choose **Organization** -> Enter **Blueprint Name** -> Choose **Business Group** -> Choose **Project** 
   5. Click on **Configure Runlist Parameters** -> Click on ** + ** icon to edit the runlist
   6. Search for Cookbook **deploy_upgrade_catalyst** and select that cookbook -> Click on ** > ** to add to **Runlist** -> Click on **Update Runlist** 
   7. Click on **Configure Application** and Select checkbox **Deploy app during Bootstrap**.
   8. Select **Repository Server** , **Repository Name** , **GroupID** , **Artifacts**, **Versions**
   9. Click on **New** button to add Application Name and URL
   10. Enter **Application Name** and add the URL in the format **http://$host:3001** -> Click on **Add** button.
   11. Click on **Next** button -> Click on **OK** button in Confirm popup window.

  Step4: Launch Instance from Blueprint and check application is installed after bootstrap
   1. Click on **Workzone** -> **Infrastructure** -> **Blueprints** 
   2. Select the Blueprint created in Step3 -> Click **Launch** button -> Click **OK** on Confirmation window.
   3. Wait untill **Instance Bootstraped successfully* log is displayed in Launching Blueprint window.
   4. Close the Launchinf Blueprint window.
   5. Click on **Infrastructure** -> **Instances**
   6. Click on More link present at bottom right corner on the Instance.
   7. Clcik on the **App name** link
   8. Verify New window opened and Catalyst appliaction home page is displayed with Version number, Now close the newly opened window.
   9. Go to Applications tab and check Application details like **Application Name** , **Version Number** , **Ipaddress** of the Instance with **Date** and **Time** is displayed in pipeline view.

  Step5: Application version upgrade and check latest version is upgraded
   1. Click on **Workzone** -> **Applications**
   2. Click on **Deploy New APP** button -> Select **Repository Server** -> Choose **Repository** -> Choose **Group ID** -> Choose **Artifacts** -> Choose **Versions** 
   3. Click on **Create New Job** button -> Select Job type as **Chef** -> Enter **Job Name** -> Select **Node** on which you are going to upgrade application -> Click on ** + ** icon to edit the runlist -> Search for Cookbook **deploy_upgrade_catalyst** and select that cookbook -> Click on ** > ** to add to **Runlist** -> Click on **Update Runlist**
   4. Click on **Jobs** dropdown and select the **Job** you created in previous step
   5. Click on **Deploy** button -> Click **OK** button in confirmation popup and wait untill **Task Executed successfully** message is displayed -> Close  **Execute Logs** window
   6. Click on **Infrastructure** -> **Instances** 
   7. Click on More link present at bottom right corner of the Instance
   8. Click on the **App name** link
   9. Verify New window opened and Catalyst appliaction home page is displayed with upgraded Version number, Now close the newly opened window
   10. Go to Applications tab and check new card with application details like **Application Name** , upgraded **Version Number** , **Ipaddress** of the Instance with **Date** and **Time** is displayed in pipeline view in another row.


        
Flow5 : **Tracks Setup** 
            
  * View Cost & Usage Dashboards
     
  Step1 Track Setup for Provider Dashboard
   1. Click on **Settings** -> **Track Setup** -> Click **New** button
   2. Select Type as **Provider** -> Enter the **Description** , **Item Name** and Enter **Item URL** in the format **http://Nodeipaddress:port/Dashboard.html** -> Click on **Save** button.


  Step 2: Track setup for AWS Summary Dashboard
   1. Click on **Settings** -> **Track Setup** -> Click **New** button
   2. Select Type as **Provider** -> Enter the **Description** , **Item Name** and Enter **Item URL** in the format **http://Nodeipaddress:port/dashing.html** ->Click on **Save** button.

  Step 3: View Provider Dashboard and AWS Summary Dashboard
   1. Click on **Track** link present at the top. You are able to see dashboard for providers with **provider name** , **Total number of Instances** , **Total number of Managed instances** and **Total number of unmanged Instances** present in your provider.
   2. Click on AWS Summary dashboard. Here you are bale to see **Billing Period Cost** , **Monthly Cost**, **Todays cost**, **Yesterday Cost**, **Active Instances**, **EBS Volume**, **S3 Buckets**, **Elastic IPS**, **R53 Zones**




