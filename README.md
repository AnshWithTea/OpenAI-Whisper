<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ASR Project Readme</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');
        body {
            font-family: 'Inter', sans-serif;
        }
        pre {
            white-space: pre-wrap;       /* CSS 3 */
            white-space: -moz-pre-wrap;  /* Mozilla, since 1999 */
            white-space: -pre-wrap;      /* Opera 4-6 */
            white-space: -o-pre-wrap;    /* Opera 7 */
            word-wrap: break-word;       /* Internet Explorer 5.5+ */
        }
    </style>
</head>
<body class="bg-gray-900 text-gray-200 leading-relaxed">

    <div class="max-w-4xl mx-auto p-6 md:p-12">
        
        <!-- Header -->
        <h1 class="text-4xl font-bold text-white mb-4">
            High-Accuracy Multilingual ASR System (OpenAI Whisper)
        </h1>
        <p class="text-lg text-gray-400 mb-8">
            This project is a robust, high-fidelity multilingual Automatic Speech Recognition (ASR) system. It leverages OpenAI's state-of-the-art Whisper model to accurately transcribe human speech from a diverse set of over 90 languages, even in the presence of background noise and various accents.
        </p>

        <!-- Section 1: Project Objective -->
        <section class="mb-10">
            <h2 class="text-3xl font-semibold text-white border-b border-gray-700 pb-2 mb-4">
                1. Project Objective
            </h2>
            <p class="text-gray-300">
                The primary goal is to develop a practical application that demonstrates the power of large-scale, pre-trained transformer models for solving complex, real-world problems. The system provides a reliable tool for transcribing audio content, suitable for applications in media analysis, content subtitling, and accessibility.
            </p>
        </section>

        <!-- Section 2: Key Features -->
        <section class="mb-10">
            <h2 class="text-3xl font-semibold text-white border-b border-gray-700 pb-2 mb-4">
                2. Key Features
            </h2>
            <ul class="list-disc list-inside space-y-3 text-gray-300">
                <li><strong class="text-white">Multilingual Transcription:</strong> Accurately transcribes speech from over 90 different languages.</li>
                <li><strong class="text-white">Automatic Language Detection:</strong> Automatically identifies the language being spoken without requiring user input.</li>
                <li><strong class="text-white">Speech-to-English Translation:</strong> Includes functionality to directly translate spoken audio from any supported language into English text.</li>
                <li><strong class="text-white">Word-Level Timestamps:</strong> Generates precise timestamps for transcribed words, making it ideal for creating subtitles or performing audio analysis.</li>
                <li><strong class="text-white">High Robustness:</strong> Demonstrates strong performance against background noise, accents, and technical jargon due to the model's extensive training.</li>
            </ul>
        </section>

        <!-- Section 3: Technical Architecture -->
        <section class="mb-10">
            <h2 class="text-3xl font-semibold text-white border-b border-gray-700 pb-2 mb-4">
                3. Technical Architecture
            </h2>
            <p class="text-gray-300 mb-4">
                The system is built in Python and is centered around the <strong class="text-white">OpenAI Whisper</strong> model. The core workflow is as follows:
            </p>
            <ol class="list-decimal list-inside space-y-3 mb-6 pl-4 text-gray-300">
                <li><strong class="text-white">Audio Input:</strong> The application accepts common audio formats (e.g., MP3, WAV, M4A).</li>
                <li><strong class="text-white">Preprocessing:</strong> The audio is loaded, resampled, and converted into a log-Mel spectrogram, which is the required input format for the model.</li>
                <li><strong class="text-white">Inference:</strong> The spectrogram is processed by the Whisper model's encoder-decoder Transformer architecture to generate the text output.</li>
            </ol>
            <ul class="list-disc list-inside space-y-3 text-gray-300">
                <li><strong class="text-white">AI Model:</strong> OpenAI Whisper (base/large model)</li>
                <li><strong class="text-white">Language/Framework:</strong> Python, PyTorch</li>
                <li><strong class="text-white">Core Libraries:</strong> Hugging Face `transformers`, `torchaudio` (or `librosa`)</li>
            </ul>
        </section>

        <!-- Section 4: Installation -->
        <section class="mb-10">
            <h2 class="text-3xl font-semibold text-white border-b border-gray-700 pb-2 mb-4">
                4. Installation
            </h2>
            <p class="text-gray-300 mb-4">To set up the project locally, follow these steps:</p>
            <ol class="list-decimal list-inside space-y-6 text-gray-300">
                <li>
                    <strong class="text-white">Clone the repository:</strong>
                    <pre class="bg-gray-800 rounded p-4 text-sm text-green-300 mt-2"><code>git clone https://github.com/AnshWithTea/OpenAI-Whisper.git
cd OpenAI-Whisper</code></pre>
                </li>
                <li>
                    <strong class="text-white">Create and activate a virtual environment:</strong>
                    <pre class="bg-gray-800 rounded p-4 text-sm text-green-300 mt-2"><code>python -m venv venv
.\venv\Scripts\activate</code></pre>
                </li>
                <li>
                    <strong class="text-white">Install the required libraries:</strong>
                    <pre class="bg-gray-800 rounded p-4 text-sm text-green-300 mt-2"><code>pip install -r requirements.txt</code></pre>
                    <p class="mt-2 text-gray-400 text-sm">*(Note: If a `requirements.txt` is not present, you can install the core dependencies manually)*</p>
                    <pre class="bg-gray-800 rounded p-4 text-sm text-green-300 mt-2"><code>pip install torch torchaudio transformers
pip install openai-whisper</code></pre>
                </li>
                <li>
                    <strong class="text-white">Install FFmpeg:</strong>
                    <p class="mt-1">Whisper requires the command-line tool FFmpeg to be installed on your system. You can download it from <a href="https://ffmpeg.org/download.html" class="text-blue-400 hover:underline" target="_blank">ffmpeg.org</a>.</p>
                </li>
            </ol>
        </section>

        <!-- Section 5: Usage -->
        <section class="mb-10">
            <h2 class="text-3xl font-semibold text-white border-b border-gray-700 pb-2 mb-4">
                5. Usage
            </h2>
            <p class="text-gray-300 mb-4">You can use the `whisper` command-line interface to easily transcribe any audio file.</p>
            
            <div class="space-y-4">
                <div>
                    <strong class="text-white">Basic Transcription:</strong>
                    <pre class="bg-gray-800 rounded p-4 text-sm text-green-300 mt-2"><code>whisper "my_audio_file.mp3"</code></pre>
                </div>
                <div>
                    <strong class="text-white">Detect Language and Transcribe:</strong>
                    <pre class="bg-gray-800 rounded p-4 text-sm text-green-300 mt-2"><code>whisper "marathi_speech.wav" --language Marathi</code></pre>
                </div>
                <div>
                    <strong class="text-white">Translate to English:</strong>
                    <pre class="bg-gray-800 rounded p-4 text-sm text-green-300 mt-2"><code>whisper "spanish_audio.mp3" --task translate</code></pre>
                </div>
            </div>
        </section>

        <!-- Section 6: License -->
        <section>
            <h2 class="text-3xl font-semibold text-white border-b border-gray-700 pb-2 mb-4">
                6. License
            </h2>
            <p class="text-gray-300">
                This project is licensed under the MIT License - see the LICENSE file for details.
            </p>
        </section>

    </div>

</body>
</html>
