# 📧 Cold Email Generator using DeepSeek 70B, LangChain, ChromaDB, and Streamlit

This is an end-to-end Generative AI project that uses the **DeepSeek R1 Distill 70B open-source LLM**, **LangChain**, **ChromaDB (vector store)**, and **Streamlit** to build a tool for generating personalized cold emails.

> ✅ **Use case:** Software and AI service companies can use this tool to craft and send high-conversion cold emails to potential clients based on job descriptions, domains, and portfolio inputs.

---

## 🚀 Features

- ✉️ **Cold Email Generator** based on target job description & company profile
- 🧠 **DeepSeek 70B** for generating human-like, relevant email content
- 📚 **ChromaDB** for semantic search on company portfolio / documents
- 🔗 **LangChain** to orchestrate LLM with retrieval-augmented generation (RAG)
- 🌐 **Streamlit Web UI** for fast and interactive interface

---
## Set-up
1. To get started we first need to get an API_KEY from here: https://console.groq.com/keys. Inside `app/.env` update the value of `GROQ_API_KEY` with the API_KEY you created. 


2. To get started, first install the dependencies using:
    ```commandline
     pip install -r requirements.txt
    ```
   
3. Run the streamlit app:
   ```commandline
   streamlit run app/main.py
   ```

## 🧱 Architecture

```mermaid
    graph LR
        A[User Input via Streamlit UI] --> B[LangChain Pipeline]
        B --> C[DeepSeek 70B LLM]
        B --> D[ChromaDB - Vector Store]
        C --> E[Generated Cold Email]
        D --> C

