# MultiPDF Chat App

> You can find the tutorial for this project on [YouTube](https://youtu.be/dXxQ0LR-3Hg).

## Introduction
------------
The MultiPDF Chat App is a Python application that allows you to chat with multiple PDF documents. You can ask questions about the PDFs using natural language, and the application will provide relevant responses based on the content of the documents. This app utilizes a language model to generate accurate answers to your queries. Please note that the app will only respond to questions related to the loaded PDFs.

## How It Works
------------

![MultiPDF Chat App Diagram](./docs/PDF-LangChain.jpg)

The application follows these steps to provide responses to your questions:

1. PDF Loading: The app reads multiple PDF documents and extracts their text content.

2. Text Chunking: The extracted text is divided into smaller chunks that can be processed effectively.

3. Language Model: The application utilizes a language model to generate vector representations (embeddings) of the text chunks.

4. Similarity Matching: When you ask a question, the app compares it with the text chunks and identifies the most semantically similar ones.

5. Response Generation: The selected chunks are passed to the language model, which generates a response based on the relevant content of the PDFs.

## Dependencies and Installation
----------------------------
To install the MultiPDF Chat App, please follow these steps:

1. Clone the repository to your local machine.

2. Install the required dependencies by running the following command:
   ```
   pip install -r requirements.txt
   ```

3. Obtain an API key from OpenAI and add it to the `.env` file in the project directory.
```commandline
OPENAI_API_KEY=your_secrit_api_key
```

## Usage
-----
To use the MultiPDF Chat App, follow these steps:

1. Ensure that you have installed the required dependencies and added the OpenAI API key to the `.env` file.

2. Run the `main.py` file using the Streamlit CLI. Execute the following command:
   ```
   streamlit run app.py
   ```

3. The application will launch in your default web browser, displaying the user interface.

4. Load multiple PDF documents into the app by following the provided instructions.

5. Ask questions in natural language about the loaded PDFs using the chat interface.

**This one is interesting — but be honest about it.**

---

### What it actually is

This is a YouTube tutorial project (the README literally links to the tutorial video and says "does not accept contributions"). You followed along with someone else's code — LangChain, FAISS, OpenAI embeddings, Streamlit. You didn't architect this yourself.

---

### Should you keep it?

**Keep it, but reframe it honestly and extend it.** Here's why it has value despite being tutorial-based — the stack is genuinely modern and impressive: Python, LangChain, vector embeddings, RAG architecture, Streamlit. That's real technology.

The problem is every person who watched that YouTube video has the exact same repo.

---

### How to make it yours for BFSI

Extend it in a way that shows domain thinking. Replace the generic PDF chat with something specific:

**"BFSI Policy & Regulatory Document Analyser"**

- Feed it actual CBK (Central Bank of Kenya) circulars, KRA tax guidelines, or Basel III documents
- Add a prompt template that frames answers in compliance/risk context
- Add a feature that flags which regulatory clause answered the question
- Rename it: *"RegBot — Regulatory Document Q&A for BFSI Analysts"*

That turns a tutorial clone into a portfolio-worthy domain tool.

---

### Updated scorecard

| Project | Verdict |
|---|---|
| Tanzania Waterpoint ML | ✅ Keep |
| Rental Management System | ✅ Keep |
| Note-Taking App | ✅ Pivot |
| MultiPDF Chat App | ✅ Extend with BFSI domain spin |
| All HTML/CSS/JS (~20 projects) | 🗑️ Delete |

**Four keepers now.** That's a solid portfolio. Stop auditing.
