# Conversational  AI  Healthcare VOICEBOT 
 The goal of the project is to develop a conversational healthcare voice chatbot. This chatbot will use natural language processing and machine learning techniques to diagnose diseases based on user symptoms. The chatbot will be built using Rasa and Spacy, which are software libraries used for natural language processing and machine learning

Install RASA : https://rasa.com/docs/rasa/2.x/installation/

voice bot commands:

 Step 1: Speech to Text

------ pip install SpeechRecognition PyAudio 

Step 2: Externally sending an input to rasa chatbot

------ rasa run -m models --endpoints endpoints.yml --port 5002 --credentials credentials.yml

Step 3: Text to speech conversion 

------ pip install gtts and also install the media player for playing the audio after conversion,

 set any media player path to the project Now to see your voice bot in action run the Voice.py file and also run the action server using

------ rasa run actions          

At last run the voicebot python file
