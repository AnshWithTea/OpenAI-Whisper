# High-Accuracy Multilingual ASR System (OpenAI Whisper)

This project is a robust, high-fidelity multilingual Automatic Speech Recognition (ASR) system. It leverages OpenAI's state-of-the-art Whisper model to accurately transcribe human speech from a diverse set of over 90 languages, even in the presence of background noise and various accents.

---

## 1. Project Objective

The primary goal is to develop a practical application that demonstrates the power of large-scale, pre-trained transformer models for solving complex, real-world problems. The system provides a reliable tool for transcribing audio content, suitable for applications in media analysis, content subtitling, and accessibility.

---

## 2. Key Features

* **Multilingual Transcription:** Accurately transcribes speech from over 90 different languages.
* **Automatic Language Detection:** Automatically identifies the language being spoken without requiring user input.
* **Speech-to-English Translation:** Includes functionality to directly translate spoken audio from any supported language into English text.
* **Word-Level Timestamps:** Generates precise timestamps for transcribed words, making it ideal for creating subtitles or performing audio analysis.
* **High Robustness:** Demonstrates strong performance against background noise, accents, and technical jargon due to the model's extensive training.

---

## 3. Technical Architecture

The system is built in Python and is centered around the **OpenAI Whisper** model. The core workflow is as follows:

1.  **Audio Input:** The application accepts common audio formats (e.g., MP3, WAV, M4A).
2.  **Preprocessing:** The audio is loaded, resampled, and converted into a log-Mel spectrogram, which is the required input format for the model.
3.  **Inference:** The spectrogram is processed by the Whisper model's encoder-decoder Transformer architecture to generate the text output.

* **AI Model:** OpenAI Whisper (base/large model)
* **Language/Framework:** Python, PyTorch
* **Core Libraries:** Hugging Face `transformers`, `torchaudio` (or `librosa`)

---

## 4. Installation

To set up the project locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/AnshWithTea/OpenAI-Whisper.git](https://github.com/AnshWithTea/OpenAI-Whisper.git)
    cd OpenAI-Whisper
    ```

2.  **Create and activate a virtual environment:**
    ```bash
    python -m venv venv
    .\venv\Scripts\activate
    ```

3.  **Install the required libraries:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: If a `requirements.txt` is not present, you can install the core dependencies manually)*
    ```bash
    pip install torch torchaudio transformers
    pip install openai-whisper
    ```

4.  **Install FFmpeg:**
    Whisper requires the command-line tool FFmpeg to be installed on your system. You can download it from [ffmpeg.org](https://ffmpeg.org/download.html).

---

## 5. Usage

You can use the `whisper` command-line interface to easily transcribe any audio file.

**Basic Transcription:**
```bash
whisper "my_audio_file.mp3"
```
**Detect Language and Transcribe:**
```bash
whisper "marathi_speech.wav" --language Marathi
```
**Translate to English:**
```bash
whisper "spanish_audio.mp3" --task translate
```

---

## 6. License

This project is licensed under the MIT License - see the LICENSE file for details.
