
## 📄 DESIGN

### 1. System Architecture

The solution utilizes a **Voice-to-Knowledge (V2K) Pipeline** centered around a RAG (Retrieval-Augmented Generation) framework to ensure factual accuracy.

* **Speech Layer:**  Uses **OpenAI Whisper** for robust speech-to-text (STT) and **Google TTS** for natural language responses.
  
* **Cognitive Layer:**  **LangChain** manages the logic, using **Llama-3** to process queries and summarize data.
  
* **Knowledge Layer:**  A Vector Database (**ChromaDB**) stores verified government handbooks and community resources.

### 2. Data Flow

1. **Audio Input:**  Citizen speaks a query in their native language.
   
3. **Transcription & Translation:**  The audio is converted to text and translated into a standardized prompt.
   
5. **Semantic Search:**  The system retrieves the most relevant "Scheme Paragraphs" from the vector store.
   
7. **Grounded Response:**  The LLM generates a response based *only* on the retrieved text to prevent hallucinations.
   
9. **Audio Synthesis:**  The answer is read back to the user in their chosen language.

### 3. Component Design

| Component | Technology | Purpose |
| --- | --- | --- |

| **Mobile App** | Flutter / React Native | Cross-platform accessibility for community members. |

| **API Gateway** | FastAPI | Asynchronous handling of voice data and AI calls. |

| **Embedding Model** | HuggingFace (mBART) | Ensures multilingual support for Indian regional languages. |

### 4. Security & Ethics

* **Bias Mitigation:**  Regular testing against regional dialects to ensure the AI doesn't favor one demographic.
  
* **Source Verification:**  Every AI-generated response includes a "Source Reference" to the official government portal to ensure transparency.

