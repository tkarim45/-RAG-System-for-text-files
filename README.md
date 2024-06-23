<h1 align="center">RAG using LangChain</h1>

<p align="center">
  <img src="assets/Logo.png" alt="Project Overview" width="350">
</p>


## Table of Contents

1. [Overview](#overview)
2. [Features](#features)
3. [Setup](#setup)
4. [Example Questions](#example-questions)
5. [Notes](#notes)


### Overview
This repository contains a Question Answering (QA) system built using LangChain, a framework for assembling NLP pipelines. The system uses Hugging Face embeddings, FAISS for efficient document retrieval, and OpenAI's GPT-3.5-turbo model for answering questions based on provided context.

### Features
- **Document Loading:** Loads documents from PDF files using PyPDFLoader.
- **Text Splitting:** Splits the loaded documents into smaller texts for efficient processing.
- **Embeddings:** Utilizes Hugging Face embeddings to encode text.
- **Vector Store:** Stores encoded texts using FAISS for fast document retrieval.
- **Question Answering:** Uses LangChain to create a pipeline that answers questions based on the provided context.
- **Contextual Question Answering:** Answers questions by using the provided context to guide the answer generation process.

### Setup
1. Clone the repository:
   ```
   git clone https://github.com/tkarim45/RAG-System-for-text-files.git
   cd your-repo
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Set up environment variables:
   ```
   touch .env
   ```
   - Set `OPENAI_API_KEY = "Your OPENAI Key"` to your OpenAI API key in the .env file.


### Example Questions
The system is designed to answer questions based on the provided documents. Example questions include:
- What is the focus of the 'MeshAnything' project?
- Which paper discusses the integration of Large Language Models with Monte Carlo Tree Search?
- What advancements does the 'VideoLLaMA 2' paper propose?
- Which paper was published most recently?
- Identify a paper that deals with language modeling and its scalability.
- Which paper aims at improving accuracy in Google-Proof Question Answering?
- List the categories covered by the paper titled 'TextGrad: Automatic "Differentiation" via Text'.
- Which paper received the highest number of stars per hour?

### Notes
- If the question is not related to the provided context, the system will respond with "No information" or I'm sorry, but based on the provided context I cannot answer that question.
