## Azure Cognitive Language Services

### Classify and moderate text with Azure Content Moderator
#### 1. Intro
We can add text filters to ours apps and services with Microsoft Azure Content Moderator. 
(The Content Moderator service detect potentially offensive or unwanted images too.)
With the Text Moderation API, we can:
* Analyze text to look for unwanted content. It protects agains profanity. We will get a JSON response with the returned profane item in term and the values needed to identify the word.
* Classify the potentially offensive content. We can get the text classified into three categories. We will get a result from 0 to 1 with the probability that the text belongs to the each class.
1. Category - text  sexually explicit or adult in certain situations.
2. Category - text sexually suggestive or mature in certain situations.
3. Category - text offensive in certain situations.
* Get insights into the potential personally identifiable information (PII) that's being shared so we can protect it. Feature of the API help us detect PII and if possible PII values are found, the JSON with relevant information about it is returned.
    
#### 2. Use cases
We can use machine assistance to augment human moderation of environments where partners, employees, and consumers generate text content. These places include:
* chat rooms,
* discussion boards,
* chatbots,
* e-commerce catalogs,
* documents,

more:
* e-mails,
* articles reviews,
* social media,
* preparing labels (from raw text) for the NLP system.

#### 3. How to
To use this service we need to create and subscribe to a Content Moderator resource and get the subscription key for accessing the resource in Azure. We need to select a location close to ours (In some locations this service is not available.) and pricing tier.
We can run task by using the API web-based testing console. We need there to specify parameters, paste subscription key into the Ocp-Apim-Subscription-Key box and leave text in place and click send. Then we will get the answer.

The price list is divided into two parts: standard and free. Sometimes free (or both are not) is not available in all regions. For example, for Northern Europe: 1 transaction/second is available in the free option, and 10 in the standard option. The number of free transactions is limited to 5,000 in the free version, and in the paid: from 0 to 1 million transactions - € 0.844 per 1,000 transactions, from 1 million to 5 million transactions - € 0.633 per 1,000 transactions, from 5 million to 10 million transactions - € 0.506 per 1,000 transactions, over 10 million transactions - € 0.338 per 1,000 transactions.


### Add conversational intelligence to our apps by using Language Understanding Intelligent Service (LUIS)
#### 1. Intro
LUIS is an Azure Cognitive Services API that applies custom machine-learning intelligence to a user's conversational natural-language text. LUIS uses certain aspects of the text to predict the user's overall meaning and pull out relevant detailed information. Our applications can use this information to interact with the user.
We need an API which understand phases and meaning which might not be clear to everyone. That LUIS makes use of three specific aspects which are critical to aiding the algorithm in making comparisons and distinctions.
* Utterances as input data to interpret.
* User's intentions as a purpose or goal.
* Entities as an representation of word, phrase and simply data inside the utterance that we want to extract.

#### 2. Use cases
We can use LUIS in every bots in many applications where we need to read user intent and customize tasks accordingly, for example 
* bots on the websites of online stores, 
* systems that help us find an interesting job after work,
* bots for booking systems, 
* registration bots for patients at clinics, 
* bots helping to choose, for example, president - in Poland something like "Latarnik Wyborczy".

#### 3. How to
To use LUIS we need to create a resource LUIS with Language Understanding in Azure. We need select location and pricing tier. Then we can create LUIS app in the same geographic location as service. We should add intents, utterances and entities in our app and then train the model, if we need retrian too.

The price list is divided into a free and standard part. Northern Europe pricing example: free version is only for text input and 5 transactions/second, and not available at all here, standard version is for 50 transactions/second, prices: € 1.265 per 1000 transactions for text requests and € 4.639 for 1000 transactions for spoken requests.


### Discover sentiment in text with the Text Analytics API
#### 1. Intro
Text Analytics is about understanding and analyzing unstructured text. It covers sentiment analysis, key phrase extraction, language detection, and more. Text Analytics API is cloud-based service which provides advanced natural language processing (NLP) over raw text. The service uses a machine learning classification algorithm to generate a sentiment score between 0 and 1. Scores closer to 1 indicate positive sentiment, while scores closer to 0 indicate negative sentiment. A score close to 0.5 indicates no sentiment or a neutral statement.

#### 2. Use cases
Through the service we can identify language, discover sentiment, extract key phrases, and detect well-known entities from text, usage examples:
* analyze survey results,
* categorize feedback in CRM systems,
* monitor feedback in social media, 
* searching for sensitive infromations and protect them.

#### 3. How to
To use Text Analytics API we need to create an access key. We can call the API from the testing console and make calls to API without writing a line of code. We need to formulate requests using the access key and the correct region. When creating a real product (for example about feedback) solution, we should create a solution based on several Azure components, such as Azure Queue Storage, Azure Functions, and Azure Cognitive Services. We need to create a function app from the portal to host our business logic.

The price list is divided into free and standard. The prices vary widely. The detailed price list can be found here: https://azure.microsoft.com/en-us/pricing/details/cognitive-services/text-analytics/.
