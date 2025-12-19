# 🎵 PyShazam: Audio Fingerprinting & Identification

![Language](https://img.shields.io/badge/Python-3.8%2B-blue)
![Audio](https://img.shields.io/badge/Audio-Librosa-orange)
![GUI](https://img.shields.io/badge/GUI-PyQt5-green)
![Topic](https://img.shields.io/badge/Topic-Music%20IR-purple)

## 📌 Project Overview
**PyShazam** is a desktop application that identifies songs from audio clips, similar to Shazam. It uses **Digital Signal Processing (DSP)** techniques to extract unique fingerprints from audio files (Spectrogram Peaks) and matches them against a pre-built database.

The tool also features a **Spectrogram Visualizer** and an **Audio Mixer** to test the system's robustness against noise and overlapping tracks.

## ⚙️ How it Works (The Algorithm)
1.  **Spectrogram Generation:** Converts audio signals to the frequency domain using Short-Time Fourier Transform (STFT) via `Librosa`.
2.  **Feature Extraction:** Identifies local maxima (peaks) in the spectrogram (Constellation Map).
3.  **Fingerprinting:** Hashes the peaks based on their frequencies and time deltas to create a unique signature for each song.
4.  **Matching:** Compares the input clip's hashes with the database (JSON) to find the highest similarity score.

## 🚀 Key Features
* **Song Identification:** Identifies tracks even from short or noisy clips.
* **Similarity Score:** Displays a confidence percentage for the matched song.
* **Spectrogram Viewer:** Visualizes the intensity of frequencies over time.
* **Database Management:** Automatically hashes and stores new songs in `fingerprints.json`.
* **Audio Mixing:** Ability to merge two distinct tracks to test the identification capability under interference.

## 🛠️ Tech Stack
* **Core Logic:** Python, NumPy, Pandas.
* **Audio Processing:** Librosa (STFT, Mel-Spectrogram).
* **GUI:** PyQt5.
* **Storage:** JSON (Lightweight Hash Database).

## 🚀 Installation & Usage
1.  **Clone the Repo:**
    ```bash
    git clone [https://github.com/mariamashraf731/PyShazam-Audio-Fingerprinter.git](https://github.com/mariamashraf731/PyShazam-Audio-Fingerprinter.git)
    ```
2.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Run the App:**
    ```bash
    python src/main.py
    ```