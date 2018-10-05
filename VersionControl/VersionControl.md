# Version Control Hints
This is not a step-by-step guide. Instead it's a collection of screenshots which will help you complete the DevOpsHack challenges.
This is on purpose: We want you to explore and play with the different options of VSTS.

## Create a new Git repository in your Team Project ##
![Create a new Git repository in your Team Project](/VersionControl/images/NewRepositoryImport.PNG)

## Import our sample repository found [here](https://github.com/AndreasM009/DevOpsHackEssentialsPartsUnlimitedDotNetCore2.0Slick) to your new VSTS Repository ##
![Import our sample repository found here to your new VSTS Repository](/VersionControl/images/ImportRepositorySettings.PNG)

## Modify your repo to require a pull request to merge code into your master branch ##
![Modify your repo to require a pull request to merge code into your master branch](/VersionControl/images/BranchPolicies.PNG)

## Modify your repo to require a Work Item linked to a pull request ##
![Modify your repo to require a Work Item linked to a pull request](/VersionControl/images/RequireWorkItemLinked.PNG)

## Configure your repo to require at least one of your colleagues as approver ##
![Configure your repo to require at least one of your colleagues as approver](/VersionControl/images/RequireOneReviewer.PNG)

## Clone the Repository to your local machine
* Use either Visual Studio and connect to your Team Project
* Or use git command line to clone the repo and use Visual Studio Code 

##  Modify code locally then proceeding to create a pull request ##
![Create a branch and check it out](/VersionControl/images/NewBranch.PNG)

*Hint: find the file shown in src\PartsUnlimitedWebsite\Views\Home\index.cshtml*
![Modify code locally ](/VersionControl/images/ChangeCodeHereMaybe.PNG)

![Commit your change to your new branch then proceed to create a pull request into master](/VersionControl/images/NewPullRequest.PNG)