# Conversational  AI  Healthcare VOICEBOT 
 The goal of the project is to develop a conversational healthcare voice chatbot. This chatbot will use natural language processing and machine learning techniques to diagnose diseases based on user symptoms. The chatbot will be built using Rasa and Spacy, which are software libraries used for natural language processing and machine learning

 Step 1: Speech to Text

Speech to text conversion is the process of converting spoken words into written texts. This process is also often called speech recognition. Although these terms are almost synonymous, Speech recognition is sometimes used to describe the wider process of extracting meaning from speech, i.e. speech understanding. The term voice recognition should be avoided as it is often associated to the process of identifying a person from their voice, i.e. speaker recognition.

In this step, we will ask the user to say a message and that message will be recording using the microphone connected to your system and the this recording audio will be send to the object created using SpeechRecognition module that we will use here for speech to text conversion.

The python module SpeechRecognition and PyAudio are used here where SpeechRecognition is created by google, which makes it easier for speech to text conversion.First install the required module for the conversion by typing the following command in the terminal and installing it in the virtual environment,

pip install SpeechRecognition PyAudio Step 2: Externally sending an input to rasa chatbot

In this step, we will use our trained rasa chatbot that we have already built in the previous sessions and we will setup few easy things that are required for calling the rasa chatbot externally and to send an input message t it that we have received in step 1 and futher the chatbot will reply you accordingly. Here we need to make changes in the credentials file, endpoints file and to call it seperately to call rasa chatbot in backend.

If this is your first post that you are reading on my website and if you have skipped how to build your own rasa chatbot the do checkout this playlist and get the understanding of Rasa chatbot to become and expert in this field,In credentials file, add these lines and uncomment it if those are commented:

rest:

you don't need to provide anything here
rasa: url: "http://localhost:5002/api" In endpoints file, action_endpoint: url: "http://localhost:5055/webhook" When these files has been setup then run the following command in your project directory in terminal,

----rasa run -m models --endpoints endpoints.yml --port 5002 --credentials credentials.yml

Step 3: Text to speech conversion Text to speech, abbreviated as TTS, is a form of speech synthesis that converts text into spoken voice output. Text to speech systems were first developed to aid the visually impaired by offering a computer-generated spoken voice that would “read” text to the user.

In this step, we will learn how to convert the text to speech using the most useful and easiest way of conversion using gTTS module that is google Text to Speech which is designed by google for the needy one like the blind person or those who can’t view properly. For this we will use the gTTs class that is use to convert the text to speech and we will further save it to any of the audio format and then we will play it with the inbuilt module named subprocess that will help play and exit the audio using any of the installed media player.

Firstly we will install the gTTs module by simple typing the following command in the terminal and to install it in the virtual environment.

-----pip install gtts and also install the media player for playing the audio after conversion,

----- sudo apt-get install mpg321 or else set any media player path to the project Now to see your voice bot in action run the Voice_bot.py file and also run the action server using

---------- rasa run actions At last run the voicebot python file
