**Music Similarity Finder**

A simple and interactive audio-based recommendation system built using Python, Librosa, and Gradio.

**Overview**

This project analyzes audio tracks and recommends similar songs based on their acoustic features.
Each track is converted into a numerical feature vector using MFCCs, chroma, spectral characteristics, and tempo.
Using cosine similarity, the system finds the closest songs and displays the results in a clean, interactive Gradio interface.

This project was created as part of the Algorithmic Data Science coursework.

Features

**1. Audio Feature Extraction**

For every track, the system extracts:

MFCCs (timbre)

Spectral centroid (brightness)

Chroma features (harmonic content)

Tempo (rhythm/speed)

All features are averaged and flattened into a consistent 1-D vector.

**2. Mood Classification**

Each track receives a simple mood label based on:

Tempo

Brightness (spectral centroid)

Possible moods:

Calm

Energetic

Dark

Bright

**3. Similarity Recommendation System**

Computes cosine similarity between all tracks

Returns the Top-K most similar songs

Includes a similarity threshold slider for sensitivity control

**Interactive Gradio App**

The user interface includes:

Track selection dropdown

Similarity threshold slider

Waveform visualization

Mel-spectrogram visualization

Audio playback of selected track

Audio playback of recommended tracks

Bar chart of similarity scores

Everything is displayed in real time.

**Validation Suite**

To ensure correctness, the project performs:

Multi-track testing

Stability tests

Self-similarity avoidance

Similarity distribution analysis

How It Works
1. Load metadata from MP3 files
2. Extract features using Librosa
3. Build a similarity matrix
4. Recommend closest tracks
5. Visualize & listen via Gradio
Project Structure
```
Music-Similarity-Finder/
│
├── MusicSimilarityFinder.ipynb      # Main notebook
├── README.md                        # Project documentation
├── tracks/                          # MP3 dataset (not uploaded)
└── metadata.csv                     # Extracted metadata
```

**Running the Project**

Install dependencies:

`pip install librosa mutagen gradio matplotlib scikit-learn`

Launch the Gradio app:

`music_app.launch()`


**Technologies Used**

Python

Librosa

Mutagen

Scikit-Learn

Matplotlib

Gradio

NumPy / Pandas

**Author**

Rijalda Šaćirbegović
