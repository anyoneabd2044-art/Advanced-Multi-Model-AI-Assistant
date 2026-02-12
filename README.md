# Advanced-Multi-Model-AI-Assistant
#  Advanced Multi-Model AI Assistant (100% Google Colab Based)

A fully functional **multi-model AI assistant** built entirely in **Google Colab** — no Flask, no ngrok, no external deployment required.

This project combines conversational AI, sentiment analysis, summarization-based memory, question answering, analytics, and persistent chat logging into a single unified architecture.

---

##  Features

###  Conversational AI

* Powered by **Microsoft DialoGPT-medium**
* Context-aware multi-turn conversation
* GPU accelerated (if available)

###  Sentiment-Aware Responses

* Real-time sentiment detection
* Tone adaptation:

  * Supportive (Negative)
  * Enthusiastic (Positive)
  * Professional (Neutral)

###  Long-Term Memory System

* Uses **BART (facebook/bart-large-cnn)** for summarization
* Automatically compresses conversation into memory
* Memory updates every 5 messages

###  Knowledge Mode (QA System)

* Built-in Question Answering pipeline
* Switch to knowledge mode using:

  ```
  /knowledge
  ```

###  Conversation Analytics

* Sentiment distribution visualization
* Displays positive vs negative message counts
* Command:

  ```
  /stats
  ```

###  Conversation Summary

* Generates full conversation summary using BART
* Command:

  ```
  /summary
  ```

###  Chat Logging

* Saves chat history as structured JSON
* Export file: `advanced_chat_history.json`

---

## 🏗️ Architecture

This project uses a **multi-model architecture**:

| Component              | Model Used                    |
| ---------------------- | ----------------------------- |
| Chat Engine            | microsoft/DialoGPT-medium     |
| Sentiment Analysis     | Default HF Sentiment Pipeline |
| Summarization (Memory) | facebook/bart-large-cnn       |
| Question Answering     | HuggingFace QA Pipeline       |

All models run locally inside Google Colab.

---

##  Tech Stack

* Python
* PyTorch
* HuggingFace Transformers
* Matplotlib
* Google Colab (GPU optional)

---

##  How to Run

### Step 1 — Open Google Colab

### Step 2 — Factory Reset Runtime

`Runtime → Factory reset runtime`

### Step 3 — Enable GPU (Recommended)

`Runtime → Change runtime type → GPU`

Recommended GPU: **T4**

### Step 4 — Paste the Full Code in One Cell

Run the cell and wait for:

```
All models loaded successfully!
System ready.
```

---

##  Commands Inside Chat

| Command      | Description                 |
| ------------ | --------------------------- |
| `/summary`   | Show conversation summary   |
| `/stats`     | Display sentiment analytics |
| `/knowledge` | Activate factual Q&A mode   |
| `/exit`      | Exit assistant              |

---

##  Output Files

After exiting, you can save chat history:

```
advanced_chat_history.json
```

Format example:

```json
{
    "timestamp": "...",
    "user": "Hello",
    "bot": "Hi there!",
    "sentiment": "POSITIVE"
}
```

---

## System Design Highlights

* Modular architecture
* Memory compression strategy
* Emotion-aware response system
* Hybrid chat + QA pipeline
* GPU-aware execution
* Clean separation of components
* No dependency conflicts

---

##  Use Cases

* AI Research Practice
* NLP Portfolio Project
* Multi-Model Architecture Demo
* Emotion-Aware Chatbot Development
* Google Colab AI System Design

---

##  Future Improvements (Optional)

* Retrieval-Augmented Generation (RAG)
* Vector database memory
* Better prompt engineering
* Streaming responses
* Fine-tuned conversational models
* Web deployment version

---



##  Author
Mohd Abdullah arif
Aspiring AI & Machine Learning Engineer

GitHub: https://github.com/anyoneabd2044-art

---

If you like this project, consider starring ⭐ the repository.
