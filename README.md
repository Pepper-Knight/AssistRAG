# AssistRAG: AI-Driven Customer Support System

**AssistRAG** is an AI-powered Retrieval-Augmented Generation (RAG) project designed to streamline and enhance customer support. By combining the capabilities of retrieval systems and large language models (LLMs), AssistRAG delivers accurate, context-aware answers to customer queries while continuously enriching its knowledge base.

## Project Goals

The primary objective of AssistRAG is to create an intelligent customer support assistant that can:
1. Understand user queries and determine their relevance to the product.
2. Seamlessly integrate with a product-specific knowledge base.
3. Enhance query clarity, retrieve relevant information, and provide structured answers.
4. Continuously improve by asynchronously storing resolved queries and answers in the knowledge base.

---

## Key Modules

The project is divided into several core components:

### 1. **User Input Handling**
   - **Goal:** Receive and process user queries.
   - **Details:** This module ensures that the system captures queries accurately, preprocessing them for further analysis.

### 2. **Intent Classification**
   - **Goal:** Determine whether the user's intent is product-related.
   - **Details:** 
     - If **not product-related**, the system delegates the query to a general-purpose LLM to provide a response and concludes the conversation.
     - If **product-related**, the system proceeds to refine the query.

### 3. **Query Refinement**
   - **Goal:** Rewrite the user's query to make it more specific and clear.
   - **Details:** This step improves retrieval precision by ensuring the query aligns well with the knowledge base's structure and content.

### 4. **Knowledge Retrieval**
   - **Goal:** Fetch relevant information from the product-specific knowledge base.
   - **Details:** Uses vector-based similarity search (e.g., FAISS or other retrieval tools) to locate the most relevant documents or data points.

### 5. **Answer Generation**
   - **Goal:** Organize the retrieved information into a concise and helpful response.
   - **Details:** Combines retrieved data with LLMs to format the final answer in a user-friendly way.

### 6. **Async Answer Logging**
   - **Goal:** Asynchronously log the query and its generated answer in a fixed format.
   - **Details:** 
     - Ensures consistency in how questions and answers are recorded.
     - Allows for easy reference and analysis of resolved issues.

### 7. **Knowledge Base Update**
   - **Goal:** Store resolved queries and answers into the knowledge base.
   - **Details:** Updates the knowledge base dynamically to improve future query handling and expand the system's understanding.

---

## Architecture Overview

The AssistRAG system architecture is built around the following workflow:

1. **Input Handling**: Accepts user input via APIs or chat interfaces.
2. **Intent Analysis**: Classifies the intent using machine learning models.
3. **Query Optimization**: Refines product-related queries.
4. **Information Retrieval**: Fetches data from the knowledge base.
5. **Response Generation**: Combines retrieved data with LLMs to generate responses.
6. **Logging & Updating**: Asynchronously records and updates the knowledge base.

---

## Getting Started