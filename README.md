# speech_to_text
Audio to text conversion
  1 - From speech recording to text
  2 - From Audio file to text
 
 Converting Speech to Text is very easy in python. Let’s follow this simple tutorial to implement the same.

# Step#1: 
Get the below python libraries

1) pip install SpeechRecognition

2) pip install PyAudio

# Step#2: 
Open your favorite IDE, we are choosing Jupyter Notebook, and write the below code.

# Step#3: 
Now after you run the above code snippet, whatever you say on the microphone, gets converted into text :)

# Note
The below code snippet works with the default language is English. If we speak in any other language example Hindi, the text is interpreted in the form of English, like as below-

import speech_recognition as sr
r = sr.Recognizer()
with sr.Microphone() as source:
    print("Please say something...")
    audio = r.listen(source)
    print("Time out..")
    
try:
    print("Text : "+r.recognize_google(audio))
except:
    pass;
    
# In case you want to display text in the language spoken, we have to introduce a very minor change
Now, if we speak anything in Hindi, the text is displayed in the same language.

try:
    print("Text : "+r.recognize_google(audio, language='hi-IN'))
except:
    pass;
    
Hope it helps.
