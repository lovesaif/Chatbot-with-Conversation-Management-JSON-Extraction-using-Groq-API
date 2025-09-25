# Chatbot-with-Conversation-Management-JSON-Extraction-using-Groq-API

AI Chat + JSON Extractor

This repository contains projects demonstrating conversation management and JSON schema-based information extraction using Groq API (OpenAI-compatible). It also includes a Streamlit web app for interactive chat.

📂 Version 1: Without LangChain
Features / Tasks

Task 1: Conversation Management & Summarization

Maintains conversation history per session.

Summarizes conversation every k-th turn using Groq API.

Handles multiple users via session_id.

Task 2: JSON Schema Classification & Information Extraction

Extracts structured information (name, email, phone, location, age) from user messages.

Returns missing fields as null.

Web App (Streamlit)

Interactive chat interface.

Dynamically extracts JSON if user mentions json or extract.

Shows collapsible conversation track and full conversation history.



📂 Version 2: With LangChain
1️⃣ Features / Tasks

Task 1: Conversation Management & Summarization (LangChain)

Uses ConversationSummaryMemory to summarize conversations.

Uses RunnableWithMessageHistory for session-based history.

Supports window memory (ConversationBufferWindowMemory) for last k turns.

Summarization after every k-th turn.

Task 2: JSON Schema Classification & Extraction (LangChain)

Uses a dedicated LLM instance to extract structured JSON from chat.

Validates output according to JSON schema.

Web App (Streamlit)

Integrates LangChain for conversation & extraction.

Same workflow as the non-LangChain version.

Supports session-specific history, periodic summarization, and JSON extraction.

2️⃣ Requirements

requirements.txt:

requests
streamlit
python-dotenv
jsonschema
langchain
langchain-openai
langchain-community
openai


Optional: pyngrok for Colab deployment.

3️⃣ Usage

Run locally:

git clone <repo-url>
cd <repo-folder>
pip install -r requirements.txt
streamlit run app_langchain.py


Web app workflow:

Enter session ID.

Type a message.

Press Send.

JSON extraction occurs automatically if user mentions "json".

Collapsible sections show conversation track & full history.

Summarization is performed every k-th turn.

📌 Notes

Replace api_key in the code with your Groq/OpenAI key.
