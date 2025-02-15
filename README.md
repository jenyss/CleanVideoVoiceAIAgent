# Clean Voice Over AI Agent (LangGraph)

This ReAct LangGraph Agent 𝗽𝗿𝗼𝗱𝘂𝗰𝗲𝘀 𝗮 𝘃𝗶𝗱𝗲𝗼 𝘄𝗶𝘁𝗵 𝗮 𝗰𝗹𝗲𝗮𝗻 𝘃𝗼𝗶𝗰𝗲-𝗼𝘃𝗲𝗿 𝗯𝘆 𝗿𝗲𝗽𝗹𝗮𝗰𝗶𝗻𝗴 𝘁𝗵𝗲 𝗼𝗿𝗶𝗴𝗶𝗻𝗮𝗹 𝗿𝗲𝗰𝗼𝗿𝗱𝗲𝗱 𝘃𝗼𝗶𝗰𝗲 𝘄𝗶𝘁𝗵 𝗮𝗻 𝗔𝗜-𝗴𝗲𝗻𝗲𝗿𝗮𝘁𝗲𝗱 𝗼𝗻𝗲, which can also be your own cloned voice.<br>

❗❗❗ I would recommend checking [CleanVoiceOverAIAgent](https://github.com/jenyss/CleanVoiceOverAIAgent) as it is an improved version of this one, that provides timestamps for both the transcribed audio and the cleaned script, enabling forced alignment - matching the AI-generated voice to the exact timestamps in the transcript. In other words, it ensures the AI voice is properly aligned with the original recording.

1. Extracting audio from the video.
2. Transcribing speech using OpenAI Whisper API.
3. Cleaning the transcript to remove filler words and improve clarity and flow (GPT-4o).
4. (ElevenLabs) Generating a new AI voice from the refined text. You can use your own cloned voice, works great!
5. Merging the AI-generated voice back into the video while removing the original voice.
6. **TODO:** The AI-genrated voice and the original voice must be aligned, which is not done yet. I am looking into different strategies for how to do it.

If you have any questions or would like to collaborate, feel free to reach out to me on [LinkedIn](https://www.linkedin.com/in/jenya-stoeva-60477249/). You're more than welcome!

## Agent Tools
* ExtractAudio - FFmpeg
* TranscribeAudio - OpenAI Whisper API
* CleanTranscript - OpenAI GPT-4o
* GenerateAIVoice - ElevenLabs ❗You must specify ```voice_id``` in the tool. You can either select one of the ElevenLabs ones or clone your own voice.
* RemoveOldVoice - FFmpeg
* MergeAudio - FFmpeg

## Intallation

<b>Prerequisites</b>

* Access to <b>JupyterLab, Google Colab</b>, or another interactive computing environment to run this Jupyter Notebook.

### Step 1: Clone the Repository

Clone this repository to your local machine:
```
git clone <REPOSITORY_URL>
cd <PROJECT_FOLDER>
```

### Step 2: Open Jupyter Notebook in JupyterLab

Ensure that ```<PROJECT_FOLDER>``` is accessible in JupyterLab by setting it as your working directory in JupyterLab.
 * In JupyterLab, use the "Open from Path" option to load ```CleanVideoVoiceAIAgent.ipynb```.
 * Similarly, load ```.env``` and populate the variable keys with appropriate values.
 * The first cell in the Notebook installs the required libraries: **%pip install langgraph openai ffmpeg-python requests python-dotenv**

### Step 3: Run the Jupyter Notebook

To execute the notebook, select each cell and press ```Shift + Enter```.
