## Azure DevOps Bot Composer Framework CICD

* Bot Framework Composer, built on the Bot Framework SDK, is an open-source IDE for developers to author, test, provision and manage conversational experiences. 
  It provides a powerful visual authoring canvas enabling dialogs, language-understanding models, QnAMaker knowledgebases and language generation responses to be authored from   within one canvas and crucially, enables these experiences to be extended with code for more complex tasks such as system integration. Resulting experiences can then be  tested within Composer and provisioned into Azure along with any dependent resources. For more details on Bot Composer, please look into the documentation at   https://docs.microsoft.com/en-us/composer/introduction?tabs=v2x 

* Composer developers can use this CI/CD pipeline to easily deploy new versions of their bots. Using Composer and Azure DevOps developers can seamlessly deliver their software updates.


## Features of this Repository

This sample code will enhance the existing CICD Pipeline for Bot Composer Framework further in the following ways: 
  
  **a.** Multi stage deployments are implemented for multiple environments.  
  
  **b.** Importing the existing Knowledge Bases (KB) into the repository while deployment instead of manually adding the file. 
  
  **c.** Enhances the QnA Maker deployment. 
  
  **d.** Gives user the option to either deploy only web appliaction or the model files of LUIS and QnA Maker if required 
  
  **e.** Implements further security by demostrating how to pass key vault value to the app settings in the bot's application configuration 
  
  **g.** LUIS limits the maximum number versions of the previous builds to 100 as per the Microsoft documentation at https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-limits . This solution retains only the last five versions and deletes the older versions of the LUIS. This value can be configured based on the number of versions as needed.
  
  **h.** This solution also automates the creation of Prediction Resources for LUIS as per the documentation at https://docs.microsoft.com/en-us/azure/cognitive-services/luis/luis-how-to-azure-subscription?tabs=without-portal 
  
  Detailed article at https://lkgforit.com/create-a-cicd-pipeline-to-publish-your-bot-developed-in-bot-framework-composer
