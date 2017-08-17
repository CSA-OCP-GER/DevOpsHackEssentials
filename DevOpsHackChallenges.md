# DevOps Challenge \#1 - VSTS Project Setup #
In this challenge you will create a VSTS account, invite users, set up a project and create a team with your colleagues.

## Achievements ##
| # | Achievement   | Maximum score |
|-|-|-|
|1| Create a Microsoft Account on https://signup.live.com/| 10 |
|1| Create a VSTS account on http://visualstudio.com| 10 |
|1| Give your colleagues access to your account | 10 |
|1| Give your team members an appropriate security level | 10 |
|1| Create a Team Project called RedBlueTeamProject within your VSTS account| 10 |
|1| Invite users to your new Team Project | 10 |
|1| Create a team named "Team Blue" within your Team Project and invite your colleagues |10|

## Bonus Goals ##
|1| Create another team named "Team Red" within your Team Project and invite some colleagues |10|


# DevOps Challenge \#2 - Work Management and process customization #
In this challenge, you will configure VSTS to trace and plan your work.

## Achievements ##
| # | Achievement   | Maximum score |
|-|-|-|
|1.| Create a custom process template called "RedBlueAgileTemplate" based on agile template | 10 |
|1.| Create a new Work Item Type "Vision" above Scenario | 10 |
|1.| Modify your team project to inherit from this template. | 10 |
|1| TODO: Create a bunch of work items with releationship | 10 |
|1| TODO: Link work items, view history | 10 |
|1| TODO: Modify dashboard to show Reports & Stats  | 10 |
|1| Modify dashboard to show team members, your current workitems, nr of bugs | 10 |

## Bonus Goals ##
| # | Bonus Goal   | Maximum score |
|-|-|-|
|1| TODO | 10 |
|1.| Add a custom state *** in your Work Item| 10 |
|1.| Add a custom field *** | 10 |
|1| Modify your work view  to display the new hierarchy level|10|
|1| Customize your board to display Id, owner and the value of your new custom field|10|
|1| Customize your board to display items which haven't been moved for 3 days colored red |10|


# DevOps Challenge \#3 - Version Control #
In this challenge, you will set up version control, upload code and configure policies.

## Achievements ##
| # | Achievement   | Maximum score |
|-|-|-|
|1| Create a new Git repository in your Team Project| 10 |
|1| Clone our sample repository found here XXXX to your machine | 10 |
|1| Push the code to your new repo in your Team Project  | 10 |
|1| Modify your repo to require a pull request to merge code into your master branch  | 10 |
|1|Modify your repo to require a Work Item linked to a pull request |10|
|1| Configure your repo to require at least one of your colleagues as approver  | 10 |
|1| Modify code locally to do XXX, initiate and complete a pull request. Link a work item and follow the review process. | 10 |

## Bonus Goals ##
| # | Bonus Goal   | Maximum score |
|-|-|-|
|1| Investigate the history of the file committed following the trace from the work item | 10 |
|-| (With several teammembers:) Create a merge conflict on purpose and solve it |-|
|1| Integrate an external Git Repository (e.g. hosted on GitHub) and wire it up for CI ||
|-| Discuss: What would be an appropriate code flow & branching stratgey in Git?|-|
|-| Discuss: What are the main differentiators between TFVS and Git?  |-|



# DevOps Challenge \#4 - Build Configuration for CI #
In this challenge, you will set up a build definition for your project and configure it for continuous integration. 
If you need help check out the [Build Configuration Hints](/BuildConfiguration/BuildConfiguration.md).
## Achievements ##
| # | Achievement   | Maximum score |
|-|-|-|
|1| Create a new build definition "CI Build" | 10 |
|1| Configure your build definition to build the ASP.NET Core website | 10 |
|1| Modify your build definiton for CI - so set the trigger to build with every new push to the master branch| 10 |
|1| Clone your build definition, call the clone "PR Build" and set the trigger to Pull Request | 10 |
|1| Modify your PR Build to run unit tests | 10 |
|1| Modify your source code locally, push the code, trigger a PR and follow the Pipeline | 10 |

## Bonus Goals ##
| # | Bonus Goal | Maximum score |
|-|-|-|
|1| Create a private build agent (e.g. on your local machine or any VM) and spin it up so it is connected to your account. (You can find the required agent application in your VSTS portal for download). | 10 |
|1| Modify your CI build to create a work item on failure. | 10 |
|1| TODO: Modify your Build to send a notification to your Slack channel after completion. | 10 |
|1| TODO: Modify your Build to query Web API XXX as a first step. |10|



# DevOps Challenge \#4 - Release Management #
In this challenge, you will release your application to Azure. If you need help check out the [Release Management Hints](/ReleaseManagement/ReleaseManagement.md).
## Achievements ##
| # | Achievement   | Maximum score |
|-|-|-|
|1| Create a release definition which will be triggered automatically after a successful build of "CI build" | 30 |
|1| Add a task to deploy the required infrastructure on Azure. Use the ARM Template provided  in /env/Templates/FullEnvironmentSetupMerged.json.  | 10 |
|1| Modify your release definition to deploy your application.| 10 |
|1| Modify your code locally, push the code and watch the pipeline. | 10 |
|1| Create another release environment which deploys to another deployment slot. | 10 |

## Bonus Goals ##
| # | Bonus Goal   | Maximum score |
|-|-|-|
|1|Add a 3rd deployment slot called "Test" by modifiying your ARM template accordingly.|20|
|1| DEMO: Modify your Release Definition to automatically create an Azure Dev Test Lab virtual machine image with the latest version of your software installed|100|

# DevOps Challenge #5 - Automated Testing #
In this challenge, you will integrate automated tests into your application.
If you need help check out the [Auto Test Hints](/AutoTest/AutoTest.md).

## Achievements ##
| # | Achievement   | Maximum score |
|-|-|-|
|1|  Create an automated performance test for the start page of your website which will be executed after deploying to environment "Dev". Configure it to simulate 100 users over 2 minutes. Configure it to fail if response times are larger then 5 seconds.| 10 |
|1|  Create an cloud based load test for your website which will be executed after release to test environment. Use the provided XXX.loadtest & XXX.webtest files. Check the results after you ran them.| 10 |

## Bonus Goals ##
| # | Bonus Goal   | Maximum score |
|-|-|-|
|1| Using VS create a new Loadtest and use it during release. | 10 |

# DevOps Challenge #6 - Applicaton Monitoring #
In this challenge, you will set up monitoring for your application in Azure.
If you need help check out the [Auto Test Hints](/ApplicationMonitoring/ApplicationMonitoring.md).
## Achievements ##
| # | Achievement   | Maximum score |
|-|-|-|
|1| Find the Application Insights component for your app in Azure portal. Search for the different instances of AI for your slots. | 10 |
|1| TODO: Add Release Annotations for your release definition for every environment. What could you do to avoid doing modifications like this for every environment?| 10 |
|1| TODO: Custome Telemetry | 10 |
|1| TODO: Instrument your Web Pages | 10 |
|1| Add an Availability test from 5 locations in a 5 min frequency with dependencies; Match content for a string found in your startpage. Set alerts to send you an email. Provoke an error.| 10 |
|1| Find the place to create a work item from AI in Azure Portal. Configure the settings to create a Work Item in your VSTS project. | 10 |
|1| Adjust your dashboard to show AI metrics. | 10 |

## Bonus Goals ##
| # | Bonus Goal   | Maximum score |
|-|-|-|
|1| Create a bug from the Azure portal | 10 |


# DevOps Challenge 7 - DevOps for Container #
In this challenge, you will create a pipeline for container deployment.
## Achievements ##
| # | Achievement   | Maximum score |
|-|-|-|
|1| Dockerize your application | 10 |
|1| Create a new build definition for your application which creates a container image| 10 |
|1| On Azure create an Azure Container Registry|10|
|1| Extend your pipeline to automatically deploy this image into a container registry |10|
|1| Create a release pipeline which deploys your container to Azure Container Instances|10|

# DevOps Challenge 8 - Start in the cloud #
In this challenge you will set up an end to end devops pipeline starting in the Azure Portal. Azure Portal can do a lot of the steps we did so far on it's own. 
If you need help check out the [Azure Portal Deployment Hints](/StartInTheCloud/StartInTheCloud.md).
## Achievements ##
| # | Achievement   | Maximum score |
|-|-|-|
|1| In Azure Portal create a new Azure Web App.| 10 |
|1| Connect it to VSTS and configure it to configure a pipeline for you.| 10 |
|1| Investigate the pipeline and trigger a release. | 10 |

<!-- # Bonus Challenge 9 - Extensibility #
In this challenge, you will create a custom extension for your application.
## Achievements ##
| # | Achievement   | Maximum score |
|-|-|-|
|1| Clone XXXX and modify the code to create a new extension called YYYY| 10 |
|1| Investigate the code and change it to accept additional input and to XXXX  | 10 |
|1| Build the extension and upload it to VSTS to make it available in your account -->

