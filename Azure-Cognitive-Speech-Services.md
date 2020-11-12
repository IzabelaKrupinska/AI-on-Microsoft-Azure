## Azure Cognitive Speech Services

### Transcribe speech input to text
#### 1. Intro
The Speech-to-text aspect of the Speech services, in Azure Cognitive Services, provides real-time transcription of audio streams based on machine learning and artificial intelligence. The Speech services APIs allow to add end-to-end, real-time speech transcription to applications or services.

We can use this service with an SDK client library or a representational state transfer (REST) API.

With this Service we can:
* provide speech-to-text transcription to improve our applications,
* easily translate to and from multiple, supported languages,
* perform Text-to-Speech operations that can accept text input and then output a spoken version of that text, using synthesized speech,
* integrate with LUIS to perform entity recognition.

#### 2. Use cases
Speech services can be use in scenarios like:
* translation of live presentations,
* in-person or remote translated communications,
* customer support,
* business intelligence,
* media subtitling,
* multilingual AI interactions,

more:
* placing an order for a product,
* write articles etc., 
* conduct interviews.


#### 3. How to
To speech-to-text translation we need to create Azure Speech resource by using the Azure portal, the Azure CLI, or the Cloud Shell. 

To access our Speech Service from an application, we will need to get a subscription key that's passed with every request to authenticate the call and the endpoint that exposes our service on the network. 

We need to install Python or C# and Visual Studio Code for coding.

After installing the required components (in case with Python) we are creating a python file with speech_config object - based on the SpeechConfig class (include information related to our subscription - key, region, endpoint, etc.)  and initializing a recognizer.

Then result of the speech to text transcriptions will be displayed in the terminal window.

Speech-translation services are designed to target specific language-translation scenarios. Speech languages are devided by types: speech to text, speech translation, and text to speech. Language support varies by Speech service functionality.

Speech Service is standard and free pricing, more here: https://azure.microsoft.com/en-us/pricing/details/cognitive-services/speech-services/.


### Synthesize Text Input to Speech
#### 1. Intro
Text-to-speech is known as voice synthesizing. Typically a collection of synthesized voices are available for users to choose from. The text that is used for input, is evaluated and then passed to the synthesizer to generate the spoken words. Synthesized speech now sound like a computer-generated representation. 

Every phase sound different if being spoken by a native of another country. The Speech Services API hels in this case. The service provides standard and neural voices for use but also allows customization to meet our unique needs. Two additional features of the text-to-speech service are the ability to handle long audio files and customization of speech output using the Speech Synthesis Markup Language (SSML). 

#### 2. Use cases
Speech synthesis is being adopted when:
* improving accessibility for example for people with visual impairment or reading difficulties,
* responding in multitasking scenarios to absorb important information quickly and comfortably,
* enhancing learning with multiple modes,
* delivering intuitive bots or assistants.

When thinking of text-to-speech I see an app reading a book. We could use this application during work, when we have divided attention, we can do our duties and listen to books - improve our vocabulary and not feel lonely.

#### 3. How to
The process is basically the same as above. The input ise text, the output is synthesized audio played using choosen voice.

Pricing details here: https://azure.microsoft.com/en-us/pricing/details/cognitive-services/speech-services/.

### Translate speech with the speech service
#### 1. Intro
Speech translation is the process by which conversational, spoken phrases are instantly translated (and spoken aloud) in a second language. Most speech translation systems derive from one or more of three base technologies: automatic speech recognition (Site Recovery), machine translation, or voice synthesis. Automatic speech recognition is performed using a neural network system trained on analyzing thousands of hours of incoming audio speech. In the speech translation world, a machine translation system is an application or service that uses machine-learning technologies to translate large amounts of text or spoken content to another supported language. 

Azure Cognitive Services Speech Translation provides robust, machine learning and artificial intelligence-based services focusing specifically on the real-time multi-language translation of speech, enabling developers to add end-to-end, real-time, speech translations to their applications or services.

#### 2. Use cases
Speech translation services are used in many scenarios today:
* live presentation translation,
* in-person or remote translated communications,
* customer support,
* business intelligence,
* media subtitling,
* multilingual AI interactions.

We can learn languages, translate something to write an e-mail, etc.

#### 3. How to
To use speech transaltion we need to make Speech Service recource and create a subscription to the Speech Translation API. We need the subscription keys and endpoint. We need there Python and Visual Studio Code too. After making a needed file we can use it and say something then program will send the audio to the service for translation and next we will see the response indicating the recognized text from our audio and the showing the conversion into the target language.

Pricing details here: https://azure.microsoft.com/en-us/pricing/details/cognitive-services/speech-services/.
