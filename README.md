# Sahaay AI: Multilingual Civic Access Portal

### *Empowering communities by breaking language and literacy barriers to public services.*

---

## ❖ Overview

**Sahaay AI** is a voice-first, multilingual platform designed to help citizens in rural and semi-urban areas navigate the complex landscape of government schemes, civic rights, and public resources. By utilizing Speech-to-Text and LLMs, it provides instant, simplified information in local dialects (like Marathi, Hindi, etc.), ensuring that literacy is no longer a barrier to social welfare.

## ❖ The Problem

* **Information Asymmetry:**   Many eligible citizens are unaware of schemes like PM-Kisan or Jan Dhan due to complex official jargon.

* **Language Barrier:**  Official portals are often available only in English or standard Hindi, excluding millions who speak regional dialects.
  
* **Digital Divide:**  Navigating complex websites is difficult for elderly or low-literacy populations.

## ❖ Key Features

* **Voice-to-Scheme Matching:**  Users can speak their needs (e.g., *"I am a farmer with 2 acres of land, what help can I get?"*) and receive a curated list of eligible schemes.
  
* **Local Language Support:**  Integrated with **Bhashini API** or **Whisper** for accurate regional language processing.
  
* **Document Summarizer:**  Simplifies 20-page policy documents into 3 bullet points in the user's native tongue.
  
* **Offline-First SMS Bridge:**  For low-bandwidth areas, the AI can send critical scheme details via simple SMS/USSD.

## ❖ Tech Stack

* **Frontend:**  React Native (Mobile-first) or Streamlit.
  
* **AI/NLP:**  LangChain, OpenAI GPT-4o, or Llama-3 (fine-tuned for Indian languages).
   
* **Speech:**  OpenAI Whisper (STT) and Google Text-to-Speech (TTS).
  
* **Backend:**  Python (FastAPI).
  
* **Database:**  Pinecone / ChromaDB (for storing scheme documents).

## ❖ Project Structure

```text

├── docs/               # Government scheme PDFs and data sources

├── embeddings/         # Vectorized scheme information

├── src/

│   ├── voice_engine.py  # Speech-to-text & Text-to-speech logic

│   ├── rag_pipeline.py  # AI logic for scheme matching

│   ├── app.py           # Main application interface

│   └── translator.py    # Local language translation module

├── requirements.txt    # Project dependencies

└── README.md


