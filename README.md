# Azure Sitecore Templates
Azure template(s) for Sitecore on Azure.

This template will deploy Sitecore 8.1 in CMS only mode.

Following resources are created by the template-
- A virtual network with three subnets.
- Content delivery on two(configurable) VMs and content management on one VM.
- A SQL Server on a VM.
- A load balancer for content delivery roles.

The template will download and deploy Sitecore 8.1 from the user provided URLs.

User will need to provide the following two URLs-
- license.xml URL
- sitecore zip file URL.

**It is highly advisable to use the secure SAS urls for the above two.**

To learn about creating secure SAS urls please see the video tutorial here (@ 2:40)-
http://storageexplorer.com/

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fdavesamuelson%2Fazure-templates-sitecore%2Fmaster%2FMicrosoft.Sitecore%2FMicrosoft.Sitecore.ResourceGroupDeployments%2FTemplates%2FSitecoreIaaS.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>

<a href="http://armviz.io/#/?load=https://raw.githubusercontent.com/davesamuelson/azure-templates-sitecore/master/Microsoft.Sitecore/Microsoft.Sitecore.ResourceGroupDeployments/Templates/SitecoreIaaS.json" target="_blank">
  <img src="http://armviz.io/visualizebutton.png"/>
</a>

**If your template does not Visualise, this usually indicates invalid JSON - try validating in http://jsonlint.com/**

Once deployed, use the following url to access the Sitecore web portal-
http://[loadbalancer ip address]/sitecore

Please note this is a work in progress and some of the features in the pipeline are-
- SQL AlwaysOn
- MongoDB Cluster
- Better Network/Security Design

MICROSOFT MAKES NO WARRANTIES, EXPRESS, IMPLIED, OR STATUTORY, BY POSTING SUCH DOCUMENTS OR ABOUT THE INFORMATION IN SUCH DOCUMENTS.
