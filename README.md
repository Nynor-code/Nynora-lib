# 📚 Nynora AI Agents Library (v0.1.0)

**Nynora** is a modular AI Agent Library for data science learning and automation tasks, including audio transcription, NLP, computer vision, data cleaning, and external integrations.

> 🔐 This is a private project. This README is safe for public sharing to present the capabilities of version 0.1.0.

---

## 🚀 Features

- 🎧 YouTube meeting analysis with summarization, sentiment, language, keywords, entities
- 🧠 Speaker diarization using WhisperX + pyannote
- 🖼️ Image analysis including face detection and GPS location extraction
- 🗺️ Interactive map generation for geolocated photos
- 📄 PDF and text tools: summarization, QA, keyword extraction
- 📍 Geolocation tools with map visualizations
- 💬 Chatbot summarization interface via OpenAI API
- 📦 Modular architecture for extensibility

---

## 🗂️ Modules Overview

### `nynora/text_tools.py`
*Technologies:* HuggingFace Transformers, spaCy
- `summarize_text(text)`
- `extract_keywords(text)`
- `extract_entities(text)`
- `detect_language(text)`
- `classify_sentiment(text)`
- `answer_question(question, context)`

➡️ NLP tools powered by HuggingFace and spaCy.

---

### `nynora/audio_tools.py`
*Technologies:* Whisper, WhisperX, yt_dlp, torchaudio
- `summarize_youtube_video(url)`
- `transcribe_with_speakers(audio_path)` *(WhisperX + diarization)*
- Uses `whisper`, `whisperx`, `torchaudio`, `yt_dlp`

---

### `nynora/image_tools.py`
*Technologies:* OpenCV, MediaPipe, Tesseract (OCR), Pillow, ExifTags
- `preprocess_image(image_path)`
- `detect_faces(image_path)` *(with MediaPipe fallback to Haar)*
- `extract_photo_metadata(image_path)`
- `resize_image(image_path, output_path)`
- `read_table_from_image(image_path)`

➡️ For EXIF parsing, OCR, and face recognition.

---

### `nynora/geo_tools.py`
*Technologies:* geopy, networkx
- `geocode_address(address)`
- `shortest_path(graph, source, target)`

➡️ For location mapping and route calculation using `geopy` and `networkx`.

---

### `nynora/integration_tools.py`
*Technologies:* OpenAI API, Whisper, yt_dlp
- `chatbot_interface(prompt, history)`
- `summarize_youtube_video(url)`
- `whatsapp_interface()` *(placeholder)*

➡️ Connects external AI services and APIs.

---

### `nynora/utils.py`
*Technologies:* Python stdlib (logging, json, pathlib)
- `setup_logging()`
- `save_config(data, filepath)`
- `load_config(filepath)`

➡️ Helpers for logging and config persistence.

---

## 🧪 Examples

### `examples/analyze_meeting.py`
Analyze a YouTube meeting:
- Transcript + summary
- Keywords, named entities, sentiment
- Chatbot response
- Saves report to JSON

### `examples/photo_geo_analysis.py`
Detect faces, extract EXIF GPS, and place the photo on an interactive map.

### `examples/geo_route_demo.py`
Plot a route between two geocoded addresses on a folium map.

---

## 🗃️ Version History

| Version | Date       | Highlights                                      |
|---------|------------|-------------------------------------------------|
| 0.1.0   | 2024-05-22 | Initial public-readable release with full doc. |

➡️ Next: more functionalites, export modules, API docs, test suite, Streamlit UI

---

## 📦 Requirements

Recommended Python version: `>=3.10`

Install all dependencies:

```bash
make setup
```

Create minimal clean requirements:

```bash
make clean-reqs
```

---

## 🛠️ Run Examples

```bash
run_example1         # analyze a you tube meeting videomake run
run_example2:        # geocoding two addresses
run_example3:        # geocoding photo location
...
```

---

## Directory Structure
```text
nynora/
├── nynora/
│   ├── __init__.py
│   ├── audio_tools.py        # AUDIO related tools
│   ├── text_tools.py         # TEXT related tools
│   ├── data_tools.py         # DATA related tools
│   ├── image_tools.py        # IMAGE related tools
│   ├── integration_tools.py  # Platforms integration related tools
│   ├── geo_tools.py          # GEO related tools
│   └── utils.py              # UTILITIES generic tools
├── examples/         # Examples of Nynora realive applications
├── setup.py
├── README.md
├── LICENSE
├── requirements.txt
└── pyproject.toml
```

---

## 🤖 Notes

- The project uses `mediapipe`, `whisperx`, `transformers`, `spaCy`, and `folium`.
- WhisperX requires login with `huggingface-cli login`
- For diarization, ensure torch==1.10 and pyannote.audio==0.0.1 (see requirements-diarization.txt)

---

## 📬 Contact

Made with curiosity and care by **Nynor**  
For AI agents, real-world data, and meaningful tools.

---# Nynora-lib
This project is private. Keeping visible the README.md for information
