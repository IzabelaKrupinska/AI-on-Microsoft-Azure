## Azure Cognitive Language Services

### Classify and moderate text with Azure Content Moderator

#### 1. Intro

We can add text filters to ours apps and services with Microsoft Azure Content Moderator. 
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

    Jak użyć tego serwisu?
    Pricing - ile się za niego płaci
