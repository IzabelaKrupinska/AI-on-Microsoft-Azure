## Azure Bot Service

### Build a bot with QnA Maker and Azure Bot Service
#### 1. Intro
Bots are a popular way to provide support through multiple communication channels. When combined with Azure Bot Service, we can use QnA Maker to deliver a bot that responds intelligently to user questions over multiple communication channels.

#### 2. How to
We can easily create a user support bot solution on Microsoft Azure using a combination of two core technologies:
* QnA Maker. This cognitive service enables to create and publish a knowledge base with built-in NLP capabilities.
* Azure Bot Service. This service provides a framework for developing, publishing, and managing bots on Azure.

First we need to provision a QnA Maker resource and then create a knowledge base that consists of question-and-answer pairs. After creating a set of question-and-answer pairs, we must train our knowledge base. After training, we can use the built-in test interface in the QnA Maker portal to test our knowledge base by submitting questions and reviewing the answers that are returned. When we are satisfied with our trained knowledge base, we can publish it so that client applications can use it over its REST interface. Now we can deliver it to users through a bot.

We can create a custom bot by using the Microsoft Bot Framework SDK or use the automatic bot creation functionality of QnA Maker, which enables us create a bot for our published knowledge base and publish it as an Azure Bot Service application with just a few clicks. We can manage it in the Azure portal.

While creating the automatic bot we need Azure Subscription and Python environment. First, we must create Machine Learning Resource, then create a compute instance.

When our bot is ready to be delivered to users, we can connect it to multiple channels; making it possible for users to interact with it through web chat, email, Microsoft Teams, and other common communication media.

Price lists for QnA Maker and Machine Learning Studio come in two versions: free and standard. The exact price lists can be found here: https://azure.microsoft.com/en-us/pricing/details/cognitive-services/qna-maker/, https://azure.microsoft.com/en-us/pricing/details/machine-learning-studio/.


### Create a Bot with the Bot Framework Composer
#### 1. Intro
Composer integrates language understanding services such as LUIS and QnA Maker and allows sophisticated composition of bot replies using Language Generation. Composer is built using the latest features of the Bot Framework SDK. 

With Bot Framework Composer we can quickly and easily build sophisticated conversational bots without writing code. Using Bot Framework Composer have advantages:
* we can simplify interruption handling and give bots character using Adaptive Dialogs (they allow for Language Generation),
* it eliminates the need for boilerplate code thanks to visual design surface,
* it saves time with little steps to set up environment,
* in projects we have reusable assets in the form of JSON and Markdown files that can be bundled and packaged with a bot's source code.

#### 2. How to
We need to install the Composer - correct desktop application for our operating system (Windows, macOS, Linux) and Bot Framework Emulator and .NET Core SDK 3.1. Bot Frameork Composer is easy to use, to create a bot we need to clik on the Home screen New and enter the next necessary informations. On the Home screen we can open an existing bot on our computer, view some tutorial videos, and also examine some example bots created using the Composer. 

Dialogs are one of the bot funcionality. Each dialog will contain instructions for the bot. We can use SDK and write code to implement dialog funcionality or we can use Bot Framework Composer and the visual designer and the environment without writing code. In Composer we have two types of dialogs: main dialog and a child dialog. We have various components in the dialogs: LU Recognizer - is responsible for interpreting what the user wants, based on the input, Triggers (types: Intent recognized, Unknown intent, Dialog events, Activities, Custom events) - typically contain a series of actions that are performed to satisfy the user request. 

In our bot we can provide the ability to help users navigate our bot or cancel the current request.

To understand what the user means conversationally and in the proper context Composer integrates with the Bot Framework Language Generation library - set of powerful templating and message formatting tools at let us include variation, conditional messages, and dynamic content. In the Properties pane we can modify the contents of the Language Generation.

Interaction methods can be buttons or cards too. We can edit it in Send a response. The Bot Framework Composer offers the LUIS recognizer as a means to access the Language Understanding technology.

Bot Framework Composer is free tool.

### Use cases of bots
Bots can be used on websites to help you use the site. On websites where we can buy something as a customer advisor. On the hotline of companies' websites, hospitals, sanitary services, police, travel agencies. These are just a few examples. Because bots can be used wherever the client needs an appropriate, individual answer on a given topic. Bots are use to provide a first-line of automated support through the full range of channels that we use to communicate. 
