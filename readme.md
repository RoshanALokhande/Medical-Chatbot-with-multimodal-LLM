# AI Doctor Bot – Voice & Vision Powered
This is an AI-powered multimodal medical assistant that allows users (patients) to ask questions via voice, image, or both. The bot responds like a professional doctor using LLMs and text-to-speech technology.

# Features
1. Voice-to-Text: Patients can ask questions using voice.
2. Medical Image Analysis: Upload medical images (X-rays, skin issues, etc.).
3. AI Doctor Response: Uses an LLM (Meta LLaMA) to analyze and respond.
4. Text-to-Speech Output: Converts the response into a doctor-like voice.

# Tech Stack
1. Python 3.x
2. Gradio for UI
4. Whisper + GROQ API for Speech-to-Text
5. Meta LLaMA (via Groq API) for response generation
6. ElevenLabs / gTTS for Text-to-Speech
7. dotenv for secure key handling


# Project Setup Guide

This guide provides step-by-step instructions to set up your project environment, including the installation of FFmpeg and PortAudio on Windows, as well as setting up a Python virtual environment using Pipenv or pip

## Table of Contents

1. [Installing FFmpeg and PortAudio](#installing-ffmpeg-and-portaudio)
   - [Windows](#windows)
2. [Setting Up a Python Virtual Environment](#setting-up-a-python-virtual-environment)
   - [Using Pipenv](#using-pipenv)
   - [Using pip and venv](#using-pip-and-venv)
   
3. [Running the application](#project-phases-and-python-commands)

## Installing FFmpeg and PortAudio

### Windows

#### Download FFmpeg:
1. Visit the official FFmpeg download page: [FFmpeg Downloads](https://ffmpeg.org/download.html)
2. Navigate to the Windows builds section and download the latest static build.

#### Extract and Set Up FFmpeg:
1. Extract the downloaded ZIP file to a folder (e.g., `C:\ffmpeg`).
2. Add the `bin` directory to your system's PATH:
   - Search for "Environment Variables" in the Start menu.
   - Click on "Edit the system environment variables."
   - In the System Properties window, click on "Environment Variables."
   - Under "System variables," select the "Path" variable and click "Edit."
   - Click "New" and add the path to the `bin` directory (e.g., `C:\ffmpeg\bin`).
   - Click "OK" to apply the changes.

#### Install PortAudio:
1. Download the PortAudio binaries from the official website: [PortAudio Downloads](http://www.portaudio.com/download.html)
2. Follow the installation instructions provided on the website.

---

## Setting Up a Python Virtual Environment

### Using Pipenv
1. **Install Pipenv (if not already installed):**  
```
pip install pipenv
```

2. **Install Dependencies with Pipenv:** 

```
pipenv install
```

3. **Activate the Virtual Environment:** 

```
pipenv shell
```

---

### Using `pip` and `venv`
#### Create a Virtual Environment:
```
python -m venv venv
```

#### Activate the Virtual Environment:
**macOS/Linux:**
```
source venv/bin/activate
```

**Windows:**
```
venv\Scripts\activate
```

#### Install Dependencies:
```
pip install -r requirements.txt
```

---

### Using Conda
#### Create a Conda Environment:
```
conda create --name myenv python=3.11
```

#### Activate the Conda Environment:
```
conda activate myenv
```

#### Install Dependencies:
```
pip install -r requirements.txt
```


# Project Phases and Python Commands

## Phase 1: Brain of the doctor
```
python brain_of_the_doctor.py
```

## Phase 2: Voice of the patient
```
python voice_of_the_patient.py
```

## Phase 3: Voice of the doctor
```
python voice_of_the_doctor.py
```

## Phase 4: Setup Gradio UI
```
python Gradio_app.py
```
