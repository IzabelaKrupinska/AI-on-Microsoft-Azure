## Process and classify images with the Azure cognitive vision services

### Computer Vision API
#### 1. Intro
The Computer Vision API provides algorithms to process images and return insights. The Computer Vision API is a powerful tool for processing images, it is a helpful solution that makes computer vision simple and fast. A facility by which a computer acquires human vision. Computer Vision API can be used to analyze images for insights, extract text from images, and generate high-quality thumbnails.

Face API consists of few categories:
* probability based verification,
* detection of human faces in images,
* face search and identification,
* finding similar faces,
* grouping unidentified faces.

Face API uses artificial intelligence for example to detect human activity in image. The Face API provides methods to detect human faces in images and can return face locations, landmarks and attributes.

The Emotion API provides advanced face analysis algorithms to assign a confidence level for the following emotions: anger, contempt, disgust, fear, happiness, neutral (the absence of emotion), sadness, and surprise.

#### 2. Use cases
This API can be used in many cases, e.g.:
* security cameras,
* social credit system in China,
* searching for ancestors in photos,
* detecting handwritten text from the manuscripts of writers.

#### 3. How to
The first step to use the Face API is to subscribe to the service. The Face API requires authorization with a subscription key (API key). The endpoint is also required to connect to our service. The endpoint is the internet URL for locating the service. So, first, we need to get subscripton keys, next, setup environment with Python or C#.

To recognize emotion, the Emotion API sends an authorized web request to another subscription endpoint. 

5000 transactions per month, 20 per minute are free. A detailed price list can be found here: https://azure.microsoft.com/en-gb/pricing/details/cognitive-services/computer-vision/.

### Custom Vision
#### 1. Intro
Purpose of Custom Vision Service is to create image classification models that "learn" from labeled images we provide.  The Custom Vision Service enables virtually anyone to build sophisticated image-classification models. And once a model is built and trained, an app that uses it is only few lines of code away.

#### 2. Use cases
This API can be used in many cases too, e.g.:
* shop app for recognizing products,
* medical diagnostics,
* checking the production line.

#### 3. How to
The first step in building an image-classification model with the Custom Vision Service is to create a project. Then we need to upload tagged images and next train the model with those images. And we are going to test the model using the portal's Quick Test feature. Last point is to call the model's prediction endpoint over http.

The Custom Vision APIs use a pair of subscription keys (the training key and the prediction key) to control access to the two APIs of the service.

Custom Vision API is free for: 2 transactions per second, upload, training and prediction transactions, up to 2 projects, up to 1 hour training per month and 5000 training images free per project and 10000 predictions per month. A detailed price list can be found here: https://azure.microsoft.com/en-gb/pricing/details/cognitive-services/custom-vision-service/.

### Video Indexer
#### 1. Intro
The Video Indexer API is using to upload, index, retrieve insights, and search for content in video files. The Video Indexer can extract insights from posted videos to help build a stunning platform with easy to implement features. It uses machine learning models that can be further customized and trained. The video insights include face identification, text recognition, object labels, scene segmentations, and more.

#### 2. Use cases
This Indexer can be used in many cases too, e.g.:
* live stream analysis,
* video processing of the wedding (removing unwanted behavior, words),
* extracting contact from a video and recommending it in advertisements,
* positioning the relevant video moments to users (e.g. educational films).

#### 3. How to
To use Video Indexer we need to sing up and create a subscribtion. To set up our API calls we will need to use the Video Indexer Developer Portal. From the portal we can find existing API subscriptions add new API subscriptions and retrieve credentials needed for programmatic access. Then we need to set up the wnvironment and upload and index videos. Next: examine the Video Indexer insights, find moments in video files using search, detect scenes, shots, and keyframes in your videos, view and edit insights related to your videos.

The Cognitive Services Video Indexer provides up to 10 hours of free indexing to website users and up to 40 hours of free indexing to API users. A detailed price list can be found here: https://azure.microsoft.com/en-gb/pricing/details/cognitive-services/video-indexer/.
