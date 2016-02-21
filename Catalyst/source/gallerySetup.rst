.. _temp-settings:

Gallery Setup
^^^^^^^^^^^^^

**The Gallery Setup option in RL Catalyst provides you four options**:

 * **Template Types:** RL Catalyst supports the following template types **SoftwareStack, OSImage, CloudFormation, Docker, ARMTemplate**. You can create various templates using these template types.

  **Software Stack:** Software Stack Template type allows you to create a blueprint with set of cookbooks that work sequentially to produce a result.

  **OSImage:** OSImage template type allows you to create blueprint with the help of VMimages


  **CloudFormation:** It simplifies provisioning and management on AWS. You can create templates which is in JSON format for the service or application architectures you want and have AWS CloudFormation use those templates for quick and reliable provisioning of the services or applications (called “stacks”). 

  **Docker:** Docker provides an integrated technology suite that enables development and IT operations teams to build, ship, and run distributed applications anywhere.


  **ARM Template:** An Azure ARM Template is a JSON file that captures the infrastructure requirements of your application. An Azure Template defines a number of related resources that are required by your application. When an Azure Template is deployed on Azure, Azure Resource Manager ensures that all resources are brought to the specified states so that your application runs under the exact desired environments.


 * **Templates:**  You can create different templates in RL Catalyst for all supported Cookbooks. You can also add new templates for newly added Cookbooks. To know more on what is a Cookbook please click: http://docs.chef.io/cookbooks.html

 * **Service Command:** Service command allows you to setup the service running options. You can choose between Chef Cookbooks based services or System service based commands. 

 * **VM Image:**  You can create multiple VM Images in RL Catalyst. RL Catalyst allows you create multiple VM images which is independent of Operating System.

*****

.. _templates-setup:

.. toctree::
   :maxdepth: 2

   gallerydefined

