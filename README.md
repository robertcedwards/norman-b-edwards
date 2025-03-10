# David Attenborough narrates your life. 

https://twitter.com/charliebholtz/status/1724815159590293764

## Want to make your own AI app?
Check out [Replicate](https://replicate.com). We make it easy to run machine learning models with an API.

## Setup

Clone this repo, and setup and activate a virtualenv:

*nix
```bash
python3 -m pip install virtualenv
python3 -m virtualenv venv
source venv/bin/activate
```
Windows
```bash
python3 -m pip install virtualenv
python3 -m virtualenv venv
venv\Scripts\activate
```




Then, install the dependencies:
`pip install -r requirements.txt`

Make a [Replicate](https://replicate.com), [OpenAI](https://beta.openai.com/), and [ElevenLabs](https://elevenlabs.io) account and set your tokens:

*nix
```
export OPENAI_API_KEY=<token>
export ELEVENLABS_API_KEY=<eleven-token>
```

*Windows
```
setx OPENAI_API_KEY token
setx ELEVENLABS_API_KEY eleven-token
```

Make a new voice in Eleven and get the voice id of that voice using their [get voices](https://elevenlabs.io/docs/api-reference/voices) API, or by clicking the flask icon next to the voice in the VoiceLab tab.

*nix
```
export ELEVENLABS_VOICE_ID=<voice-id>
```
*Windows
```
setx ELEVENLABS_VOICE_ID voice-id
setx model eleven_multilingual_v1 (etc. set for your model)
```
## Run it!

In on terminal, run the webcam capture:
```bash
python capture.py
```
In another terminal, run the narrator:

```bash
python narrator.py
```

