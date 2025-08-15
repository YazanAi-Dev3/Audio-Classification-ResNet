# AI-Powered Speech Analysis and Correction Pipeline

This project demonstrates a complete, multi-stage pipeline for analyzing and processing speech audio files. The system showcases an end-to-end solution that goes from classification to transcription and finally to audio regeneration.

##  Key Features

-   **Stutter Detection (Classification):** A custom-trained `ResNet18` model analyzes spectrogram images of audio to classify the speech's fluency (e.g., normal, stuttered).
-   **High-Accuracy Transcription (STT):** OpenAI's powerful `Whisper` model is used to generate a precise text transcription of the original audio.
-   **Corrected Audio Generation (TTS):** The transcribed (and thus corrected) text is used by the `pyttsx3` library to generate a new, clean audio file without speech impediments.
-   **Innovative Technique:** Solves an audio classification problem by creatively transforming it into an image classification problem (Spectrograms + CNN), a powerful and effective technique.

---

## ⚙ Setup & Installation

To run this project on your local machine, follow these steps:

1.  **Clone the Repository:**
    ```sh
    git clone [https://github.com/YazanAi-Dev3/Audio-Classification-ResNet.git]
    cd Audio-Classification-ResNet
    ```

2.  **Install FFmpeg:** This project requires FFmpeg to process various audio formats. Please install it on your system. On Windows, the easiest way is using `winget`:
    ```sh
    winget install Gyan.FFmpeg
    ```

3.  **Create a Virtual Environment & Install Dependencies:**
    ```sh
    # Create and activate a virtual environment
    python -m venv venv
    # On Windows: venv\Scripts\activate
    # On macOS/Linux: source venv/bin/activate

    # Install the required libraries
    pip install -r requirements.txt
    ```

You are now ready to open and run the `Audio_Classification_Demo.ipynb` notebook.

---

##  How to Use

The entire workflow is demonstrated in the **`Audio_Classification_Demo.ipynb`** notebook. Open it and run the cells sequentially to see the full pipeline in action on sample audio files.

---

##  Technologies Used

-   Python
-   PyTorch & Torchvision (for ResNet18 model)
-   OpenAI Whisper (for Speech-to-Text)
-   pyttsx3 (for Text-to-Speech)
-   Librosa (for audio processing and spectrograms)
-   Jupyter Notebook
