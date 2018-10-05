
#  Build Configuration Hints
This is not a step-by-step guide. Instead it's a collection of screenshots which will help you complete the DevOpsHack challenges.
This is on purpose: We want you to explore and play with the different options of Azure Pipelines. 

*Hint: While editing a build or release definition under the tab 'variables' you can define values which can be accessed during build/release time inside of your task with $(VariableName). There are a few standard variables documented [here for Build](https://www.visualstudio.com/en-us/docs/build/define/variables) and [here for Release](https://www.visualstudio.com/en-us/docs/build/concepts/definitions/release/variables)*
## Create Build Definition in Azure Pipelines
![Create Build Definition](/BuildConfiguration/images/NewCIBuild.png)

## Select your repository
![Select your repository](/BuildConfiguration/images/SelectRepository.png)

## Choose Build Template in Azure Pipelines for .NET Core
![Choose Template](/BuildConfiguration/images/SelectTemplate.png)

## Configure Build Tasks in VSTS
![Configure Build Tasks](/BuildConfiguration/images/ConfigureBuildTasks.png)

## Add Build Tasks to publish Artifacts
![Artifacts](/BuildConfiguration/images/PublishArtefacts.jpg)

## Add build task to publish Arm Templates
* Use the "Publish Artifacts" Task
* Pick the folder "env/templates" as "Path to publish"
* Use e.g. "ArmTemplates" as "Artifact Name".


## Create a private Build Agent for VSTS
![Configure private agent](/BuildConfiguration/images/BuildAgent.png)


