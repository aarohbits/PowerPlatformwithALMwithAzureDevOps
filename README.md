# PowerPlatformwithALMwithAzureDevOps
## Step by step document how to use Power Platform with ALM using AzureDevOps

0. Build CI/CD with Azure for Microsoft Power Platform 
Overall Microsoft Power Platform with Azure DevOps can be viewed here
![Build CI/CD with Azure for Microsoft Power Platform ](<images/01 Build CICD with Azure for Microsoft Power Platform.png>)

1. Here is STEP by STEP Guide with screenshots on how to leverage Power Platform with Azure DevOps. 
[Build CI/CD with Azure for Microsoft Power Platform](https://learn.microsoft.com/en-us/azure/architecture/solution-ideas/articles/azure-devops-continuous-integration-for-power-platform)



The guide is located here [Step by Step Guide leverage Power Platform with Azure DevOps](<20231228StepbyStepGuide/20231219 - ALM with Power Platform - Azure DevOps - GitHub.pdf>)

2. The code block for Azure DevOps Pipeline is in this as follows

```

Power Platform Export Solution
Solution Name: $(SolutionName)
Solution Output File: $(Build.StagingDirectory)\$(SolutionName)_Unmanaged.zip

Power Platform Unpack Solution
Solution Input File: $(Build.StagingDirectory)\$(SolutionName)_Unmanaged.zip
Target Folder to Unpack Solution: $(Build.SourcesDirectory)\$(SolutionName)\Unmanaged

Publish Artifact: drop
Path to publish: $(Build.SourcesDirectory)\$(SolutionName)\Unmanaged

```