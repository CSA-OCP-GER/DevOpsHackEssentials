
#  Release Management Hints
This is not a step-by-step guide. Instead it's a collection of screenshots which will help you complete the DevOpsHack challenges.
This is on purpose: We want you to explore and play with the different options of Azure Pipelines.

***Hint: Before you switch windows or close your configuration, make sure you save your modification.***

## Create Release Definition in Azure Pipelines
![Create Release Definition](/ReleaseManagement/images/NewReleaseDefinition.png)

## Choose a Release Definition template in Azure Pipelines
Start with an empty template!
![Choose a Release Definition template in Azure Pipeline](/ReleaseManagement/images/Template.png)

## Modify Release Definition Workflow in Azure Pipeline
* Make sure you connect the Output of the build definition as an input artifact.
* Make sure you set the trigger
* Add additional environments if required - you can specify if they should be targetd automatically
* Add "tasks" for your environment to describe the process of deployment

![Modify Release Definition Workflow in Azure Pipeline](/ReleaseManagement/images/Workflow.png)

## Add task to deploy infrastructure on Azure
![Add task to deploy infrastructure on Azure](/ReleaseManagement/images/DeploymentTask.png)

## Override parameters

**Make sure you copy the whole line and do not forget some leading or trailing parts of the string!**
**Hint:** Some browsers allow to triple-click the following line to mark it end to end. This allows easy copy & paste.)
In case you're wondering what you're doing here:
You're providing parameters for your ARM Template. Your ARM Template (FullEnvironmentSetupMerged.json) describes an infrastructure on Azure (Infrastructure as code). You typically parameterize this ARM template to be more flexible when it comes to e.g. website names or DB connections.

**Hint:** AdminPassword and AdminPasswordTest must be equal!

All parameter values like  $(myParametername) are "variables" within Azure Pipelines which need to be specified in the variables tab. Make sure you choose a globally unique entry for  servername & websitename.
Additionaly click the lock symbol for your passwords - this will make sure that you can use them, however they'll be hidden.

  ``` 
  -WebsiteName $(WebsiteName) -PartsUnlimitedServerName $(ServerName) -PartsUnlimitedServerAdminLogin AdminUser -PartsUnlimitedServerAdminLoginPassword $(AdminPassword) -PartsUnlimitedServerAdminLoginPasswordForTest $(AdminTestPassword) -PartsUnlimitedDBName PartsUnlimitedDB -PartsUnlimitedDBCollation SQL_Latin1_General_CP1_CI_AS -PartsUnlimitedDBEdition Basic -PartsUnlimitedHostingPlanName $(HostingPlan) -PartsUnlimitedHostingPlanSKU Standard -PartsUnlimitedHostingPlanWorkerSize 0 -EnableRules true -CdnStorageAccountName $(StorageAccountName) -CdnStorageContainerName $(ContainerName) -CdnStorageAccountNameForDev $(StorageAccountName)-dev -CdnStorageContainerNameForDev $(ContainerName)-dev -CdnStorageAccountNameForStaging $(StorageAccountName)-stage -CdnStorageContainerNameForStaging $(ContainerName)-stage  
```



## Specify all parameters
Make sure both passwords are equal!

![Specify variables as parameters](/ReleaseManagement/images/Variables.png)

## Add Azure App Service Deployment Task

![Add Azure App Service Deployment Task](/ReleaseManagement/images/AppServiceDeployment.png)
