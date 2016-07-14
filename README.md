# node-red-flows

This a place where I copy flows from other places and mach them up for my own use

##`watson-translator.json`
* requires a Watson Language translation service from Bluemix
  * use username and password given by the service
* use postman to generate the POST request to this url http://localhost:1880/translate
  * add the header `Content-Type = application/json`
  * add the follwing raw body
```json
{
    "text":"one small step for men one giant leap for mankind",
    "target":"fr",
    "source":"en"
}
```

##`watson-text-speech.json`
* requires a Watson Text toSpeech service from Bluemix
  * use username and password given by the service

In the browser type the url [http://localhost:1880/audio](http://localhost:1880/audio) keep this page open.
Then press the inject button on the flow. The web page (http://localhost:1880/audio) should speak out the text contained in the inject module. Open the inject module and change the text.


##`mashup-watson-translator+text-speech.json`
This combines watson-translator.json and watson-text-speech.json
This time the POST request is made to http://localhost:1880/translate_speech
And the audio is heard at this url http://localhost:1880/translate_speech_audio
