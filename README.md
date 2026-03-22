# Audio Source Seperation  
**Music Instrument Manipulation based on Multi-directional Microphones**

## Overview
This project explores **music instrument manipulation** in a simulated concert environment using **multi-directional microphone arrays**.  
An **eight-channel UMA-8 USB microphone** is used to capture sound sources coming from different directions toward the stage center.

The core objective is to separate and enhance instrument audio by reducing interference and noise caused by intersecting sound waves, enabling further instrument-level audio manipulations.

## Project Motivation
In live performance or rehearsal settings, multiple instruments often overlap in both time and space.  
Traditional single-channel methods struggle to isolate individual sources when wavefronts intersect.

This work investigates a **multi-channel frequency-domain** approach to:
- exploit directional information from microphone arrays,
- suppress unwanted components and environmental interference,
- preserve useful instrument content for downstream editing/manipulation.

## Methodology
The proposed pipeline includes:

1. **Multi-channel Recording**
   - Capture audio with an 8-channel UMA-8 microphone array.
   - Emulate a stage scenario where instruments are positioned at different directions.

2. **Frequency-domain Analysis**
   - Transform each channel signal into the frequency domain.
   - Analyze cross-channel spectral relationships and directional characteristics.

3. **Noise/Interference Reduction**
   - Identify and attenuate components caused by intersecting sonic waves.
   - Preserve target instrument features using multi-channel cues.

4. **Instrument Audio Manipulation**
   - Apply downstream manipulations to separated or enhanced instrument tracks.
   - Examples: gain adjustment, selective enhancement, or remix-oriented processing.

## Experimental Setup
- **Microphone Device:** UMA-8 USB microphone (8 channels)
- **Scene:** Concert-like setup with multi-directional instrument sources
- **Input:** Raw multi-channel recordings
- **Output:** Cleaner instrument-focused signals for further processing

## Repository Structure
> _This repository is currently notebook-based (100% Jupyter Notebook).  
> You can organize notebooks as the project grows, for example:_
- `notebooks/` – experiments, prototyping, and analysis
- `data/` – input recordings and metadata (optional, often excluded from git)
- `outputs/` – processed audio examples and plots
- `docs/` – figures, notes, and reports

## Results (Planned / Suggested Reporting)
To make experiments reproducible and comparable, consider reporting:
- Signal-to-Noise Ratio (SNR) improvement
- Source-to-Distortion Ratio (SDR)
- Per-instrument perceptual quality (listening tests)
- Before/after spectrogram visualizations

## Getting Started
Since this repository is notebook-centric:

1. Clone the repository
   ```bash
   git clone https://github.com/CUHK-CMD/Audio-Source-Seperation.git
   cd Audio-Source-Seperation
   ```

2. Create a Python environment (recommended)
   ```bash
   python -m venv .venv
   source .venv/bin/activate   # On Windows: .venv\Scripts\activate
   ```

3. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```
   > If `requirements.txt` is not available yet, install packages used in notebooks manually.

4. Launch Jupyter
   ```bash
   jupyter notebook
   ```

## Future Work
- Integrate direction-of-arrival (DoA) estimation for improved source localization.
- Benchmark against baseline source separation methods.
- Extend to real-time or low-latency processing for live applications.
- Evaluate robustness under reverberant and noisy environments.

## Acknowledgements
This project is developed around the topic:  
**“Music Instrument Manipulation based on Multi-directional Microphones”**  
with a focus on multi-channel signal processing in realistic stage-like audio capture scenarios.
