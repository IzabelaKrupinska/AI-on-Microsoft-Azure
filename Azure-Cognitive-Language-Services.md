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
* e-mails,
* articles reviews,
* social media.

#### 3. How to
To use this service we need to create and subscribe to a Content Moderator resource and get the subscription key for accessing the resource. We need to select a location close to ours (In some locations this service is not available.) and pricing tier.
We can run task by using the API web-based testing console. We need there to specify parameters, paste subscription key into the Ocp-Apim-Subscription-Key box and leave text in place and click send. Then we will get the answer.

The price list is divided into two parts: standard and free. Sometimes free (or both are not) is not available in all regions. For example, for Northern Europe: 1 transaction/second is available in the free option, and 10 in the standard option. The number of free transactions is limited to 5,000 in the free version, and in the paid: from 0 to 1 million transactions - € 0.844 per 1,000 transactions, from 1 million to 5 million transactions - € 0.633 per 1,000 transactions, from 5 million to 10 million transactions - € 0.506 per 1,000 transactions, over 10 million transactions - € 0.338 per 1,000 transactions.
