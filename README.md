## NAME: PREM.R
## REGISTER NO: 212223240124
## EX. NO.8
## DATE: 5/05/2024
## Implementation of Speech Recognition
## Aim: 
 To implement the conversion of live speech to text.
## Algorithm:
Step 1: Import the speech_recognition library
Step 2: Initialize the Recognizer
Step 3: Create an instance of the Recognizer class, which will be used for recognizing speech.
Step 4: Set the duration for audio capture
Step 5: Define a variable to specify the duration (in seconds) for which the program will capture audio from the microphone.
Step 6: Display a message in the console to prompt the user to speak.
Step 7: Capture audio from the default microphone
Step 9: Use the default microphone as the audio source.
Step 10: Record audio for the specified duration using the Recognizer instance.
Step 11: Perform speech recognition with exceptional handling:
•	Attempt to recognize speech from the captured audio using the Google Speech Recognition service.
•	If successful, print the recognized text.
•	Handle specific exceptions: If the recognition result is unknown or if there is an issue with the request to the Google Speech Recognition service, print corresponding error messages.
•	A generic exception block captures any other unexpected errors.
## Program:
```
import speech_recognition as sr
# initialize the reconizer
r=sr.Recognizer()
# set duration for the audio
duration=15 # second=
# record audio
print("say somthing:")

with sr.Microphone() as source:
    audio_date=r.listen(source,timeout=duration)
try:
    text=r.recognize_google(audio_date)
    print("you said:",text)
except sr.UnknownValueError:
    print("sorry ,could not undersand audio")
except sr.RequestError as e:
    print(f'Error with the request to google speech recognation service:{e}')
except Exception as e:
    print(f'Error:{e}')
```

##  Output:
![Screenshot 2024-05-06 160534](https://github.com/PREM3112/Ex-8--AAI/assets/145449383/027ec89d-78a1-4606-9141-0b7c8d333e4a)


## Result:
Thus, we have implemented a program that will transcribe the audio file in the file variable and print the transcribed text on the console, one line at a time.
