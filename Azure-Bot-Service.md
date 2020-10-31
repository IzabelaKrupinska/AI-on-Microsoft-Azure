## Azure Bot Service

### Build a bot with QnA Maker and Azure Bot Service
#### 1. Intro
Bots are a popular way to provide support through multiple communication channels.

#### 2. Use cases
Bots can be used on websites to help you use the site. On websites where we can buy something as a customer advisor. On the hotline of companies' websites, hospitals, sanitary services, police, travel agencies. These are just a few examples. Because bots can be used wherever the client needs an appropriate, individual answer on a given topic. Bots are use to provide a first-line of automated support through the full range of channels that we use to communicate. 

#### 3. How to
We can easily create a user support bot solution on Microsoft Azure using a combination of two core technologies:
* QnA Maker. This cognitive service enables to create and publish a knowledge base with built-in NLP capabilities.
* Azure Bot Service. This service provides a framework for developing, publishing, and managing bots on Azure.

First we need to provision a QnA Maker resource and then create a knowledge base that consists of question-and-answer pairs. After creating a set of question-and-answer pairs, we must train our knowledge base. After training, we can use the built-in test interface in the QnA Maker portal to test our knowledge base by submitting questions and reviewing the answers that are returned. When we are satisfied with our trained knowledge base, we can publish it so that client applications can use it over its REST interface. Now we can deliver it to users through a bot.

We can create a custom bot by using the Microsoft Bot Framework SDK or use the automatic bot creation functionality of QnA Maker, which enables us create a bot for our published knowledge base and publish it as an Azure Bot Service application with just a few clicks. We can manage it in the Azure portal.

While creating the automatic bot we need Azure Subscription and Python environment. First, we must create Machine Learning Resource, then create a compute instance.

When our bot is ready to be delivered to users, we can connect it to multiple channels; making it possible for users to interact with it through web chat, email, Microsoft Teams, and other common communication media.

Price lists for QnA Maker Ai Machine Learning come in two versions: free and standard. The exact price lists can be found here: https://azure.microsoft.com/en-us/pricing/details/cognitive-services/qna-maker/, https://azure.microsoft.com/en-us/pricing/details/machine-learning-studio/.
