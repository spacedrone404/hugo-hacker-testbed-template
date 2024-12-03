---
title: HOW TO TRANSCRIBE AUDIO SPEECH INTO TEXT USING PYTHON
date: 2023-11-15
thumbnail: "img/gallery/1946.jpg"
categories:	
- "Technology"
- "Software"
- "Windows 7"
- "FAQ"
tags:
- "Audio"
- "Python"

weight: 1

---

<br>

Recently i was asked for a simple & free way of transcribing audio speech into plain text. 
<br>
Problem was solved via Python library called [[Vosk]](https://alphacephei.com/vosk/).
<br>
It is a speech recognition toolkit working in offline environment. 

To make things happen do the following:

* [[Install vosk]](https://alphacephei.com/vosk/install)

```
pip install vosk

```
* [[Download speech model]](https://alphacephei.com/vosk/models) of required language, larger libraries bring just marginal improvement over the smaller ones despite the fact that they are over 40 times bigger in a size.
* PyAdio should be insalled also
```
pip install PyAudio

```

> Note that old versions of vosk work only with 8kHz audio files, but now it is fixed and you can use generic 44Khz.

**EXAMPLE CODE TO RECOGNIZE FROM WAV FILE**
```
from vosk import Model, KaldiRecognizer
import sys
import json
import os
import time
import wave
import vosk

model = Model(r"C:\vosk")

wf = wave.open(r'C:\vosk\demo.wav', "rb")
rec = KaldiRecognizer(model, 44100)

result = ''
last_n = False

while True:
    data = wf.readframes(44100)
    if len(data) == 0:
        break

    if rec.AcceptWaveform(data):
        res = json.loads(rec.Result())

        if res['text'] != '':
            result += f" {res['text']}"
            last_n = False
        elif not last_n:
            result += '\n'
            last_n = True

res = json.loads(rec.FinalResult())
result += f" {res['text']}"

print(result)
```

Resulting text should be printed into Python console.


**CODE TO RECOGNIZE FROM AUDIO LINE IN**


```
from vosk import Model, KaldiRecognizer
import sys
import json
import os
import time
import wave

model = Model(r"C:\vosk")

wf = wave.open(r'test.wav', "rb")
rec = KaldiRecognizer(model, 44100)

result = ''
last_n = False

while True:
    data = wf.readframes(44100)
    if len(data) == 0:
        break

    if rec.AcceptWaveform(data):
        res = json.loads(rec.Result())

        if res['text'] != '':
            result += f" {res['text']}"
            last_n = False
        elif not last_n:
            result += '\n'
            last_n = True

res = json.loads(rec.FinalResult())
result += f" {res['text']}"

print(result)

```

<br>

<hr>

<div class="demo_line_two_stock_links">

<p style="text-align:right; margin-bottom: 0;">
<br>
<a href="https://stock.adobe.com/contributor/204789995/spacedrone808" target="_blank">Imagery by spacedrone808 @Adobe </a></p>
<a href="https://www.freepik.com/author/spacedrone808" target="_blank">Imagery by spacedrone808 @Freepik </a></p>

</div>