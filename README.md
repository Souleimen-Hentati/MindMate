# MindMate

**MindMate** is a friendly AI chatbot designed to provide **mental health guidance** using **RAG (Retrieval-Augmented Generation)** and **Large Language Models (LLMs)**.  
It helps users ask questions, get **explainable answers with sources**, and expand its knowledge by uploading PDFs.

---

## Project Description

MindMate aims to create an AI-based mental health assistant that:

- Provides **reliable and explainable answers** to health-related questions.
- Uses **PDF documents as a knowledge base**.
- Supports **multilingual queries**.
- Allows users to **upload new PDFs** to improve the knowledge base.
- Stores and allows downloading **chat history**.

---

## Database / Knowledge Base

The chatbot uses PDF documents as its main knowledge source. Example PDFs:

1. [Medical_Book.pdf]("C:\Users\LENOVO\Downloads\medical_book (1).pdf")  
2. [EmotionalIntelligence.pdf](server/uploaded_docs/EmotionalIntelligence.pdf)
3. [Combined_Docs.pdf](server/uploaded_docs/combined_docs.pdf)
4. [The-Social-Skills-Guidebook-fhc-dr-notes.pdf](server/uploaded_docs/the-social-skills-guidebook-fhc-dr-notes.pdf)
5. [Managing-Stress-Principles-and-Strategies-for-Health-and-Wellbeing.pdf](server/file:///C:/Users/LENOVO/Downloads/Managing-Stress-Principles-and-Strategies-for-Health-and-Wellbeing%20(1).pdf)      

---

## Steps of the Work / Workflow

1. **PDF Processing**  
   - Extract text from PDFs.  
   - Store extracted text and metadata.

2. **Vector Store Creation**  
   - Convert text into embeddings using OpenAI embeddings.  
   - Store embeddings in **FAISS** for fast similarity search.

3. **Query Handling (RAG)**  
   - User submits a question.  
   - System retrieves relevant PDF content from vector store.  
   - LLM generates an answer based on retrieved content.  
   - Provide sources for transparency and explainability.

4. **Multilingual Support**  
   - Translate question to English (if needed).  
   - Generate answer with LLM.  
   - Translate answer back to the user’s language.

5. **Frontend Interaction**  
   - Chat UI for user input and displaying answers + sources.  
   - Upload PDF feature to dynamically update knowledge base.  
   - Save chat history for future reference.
