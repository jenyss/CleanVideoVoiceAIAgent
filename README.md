# Clean Video Voice AI Agent (LangGraph)

An AI agent for cleaning, enhancing, and replacing voices in videos with AI-generated speech, which can also be your own cloned voice.

1. Extracting audio from the video.
2. Transcribing speech using OpenAI Whisper API.
3. Cleaning the transcript to remove filler words and improve clarity (GPT-4o).
4. (ElevenLabs) Generating a new AI voice from the refined text. You can use your own cloned voice, works great!
5. Merging the AI-generated voice back into the video while removing the original voice.
6. **TODO:** The AI-genrated voice and the original voice must be aligned, which is not done yet. I am looking into different strategies for how to do it.

❗ **PAY ATTENTION:** you must change this line in the code:<br>
```voice_id = "!!!REMOVED SINCE IT WAS MY VOICE, USE THE ONE ABOVE OR CLONE YOURS!!!" # JENYS```

## Tools

TODO

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
