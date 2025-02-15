
# Project Prompt: digital-rag-chatbot-python

## Overview

The goal of this project is to develop a custom Retrieval Augmented Generation (RAG) application using Python. This application will:

- Extract and preprocess data from a target website.
- Convert the cleaned and structured data into vector representations (embeddings) using the embedding model nomic-embed-text.
- Save these vectors into the Chroma vector database.
- Utilize the vector database to answer user queries by retrieving relevant data.
- Interact with an LLM server (ollama) using the llama3.3 model for answer generation.
- Leverage LangChain to orchestrate the overall RAG workflow.

## Technologies & Tools

- **Language:** Python
- **Orchestration Framework:** LangChain
- **Vector Database:** Chroma
- **LLM Server:** Ollama
- **Embedding Model:** nomic-embed-text
- **LLM Model:** llama3.3

## Core Functionality

1. **Data Ingestion**
   - Implement web-scraping or API-based solutions in Python to load data from the target website.
   - Ensure robustness through error handling, pagination support, and scheduling options.

2. **Data Preprocessing**
   - Utilize Python libraries (e.g., BeautifulSoup, regex) to clean and normalize data.
   - Extract text content and perform linguistic preprocessing such as tokenization using standard Python libraries or LangChain utilities.

3. **Embedding and Vectorization**
   - Integrate the nomic-embed-text embedding model to transform textual data into vector representations.
   - Efficiently process large amounts of text in batches.

4. **Vector Database Integration**
   - Save generated embeddings to the Chroma vector database.
   - Optimize the vector schema for quick similarity searches and updates.

5. **Question Answering Interface**
   - Develop an interface (CLI, web-based UI, or API endpoint) in Python that accepts user queries.
   - Convert user queries into embeddings, retrieve the most relevant documents from Chroma, and generate responses.
   - Serve responses by querying the LLM server (ollama) using the llama3.3 model, orchestrated through LangChain.

## Deliverables

- A well-documented Python codebase with modular components:
  - Data ingestion module.
  - Data preprocessing pipeline.
  - Embedding and vectorization module.
  - Integration module for Chroma.
  - Query interface and response generation module.
- Setup instructions covering environment configuration, dependency management, and model integrations.
- Comprehensive tests (unit and integration) for each component.
- Architecture diagrams, design documents, and maintenance guidelines.

## Additional Considerations

- Implement error handling and monitoring to ensure system resilience.
- Plan for scalability to manage increased data volumes and query loads.
- Address any security implications, particularly regarding web scraping and data privacy.
- Provide mechanisms for updating the embedding model or LLM model as improved versions become available.

## Example Workflow

1. The system scrapes the target website and retrieves updated content.
2. The text data is cleaned and preprocessed using Python libraries.
3. Clean data is embedded using the nomic-embed-text model.
4. The resulting vectors are saved into the Chroma vector database.
5. When a user submits a query, it is converted into a vector embedding.
6. A similarity search on Chroma retrieves relevant documents.
7. LangChain orchestrates the query context, and the LLM server (ollama) using llama3.3 generates the final answer.
8. The application returns a cohesive, informative answer back to the user.

## Next Steps

- Finalize the development environment and select the Python frameworks/libraries required.
- Set up version control and organize the repository structure.
- Create a development timeline with milestones for each module.
- Build a proof-of-concept for the data ingestion and embedding modules before expanding to full question answering capabilities.
