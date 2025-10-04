# RAG-on-Legal-Documents
This repository demonstrates how to build a Retrieval-Augmented Generation (RAG) system for extracting information from legal documents, such as NDAs, contracts, and privacy policies. The project covers data loading, preprocessing, exploratory analysis, chunking, vector database creation, RAG chain setup, and evaluation.

## Project Overview

- **Objective:** Transform raw legal text data into a clean, structured format for use in RAG-based information retrieval and question-answering.
- **Business Value:** Automate legal research, contract analysis, compliance monitoring, and decision support for law firms and businesses.

## Key Steps

1. **Data Loading & Preprocessing**
    - Load `.txt` files from multiple legal document folders.
    - Clean and normalize text (remove noise, special characters, stop words, etc.).
    - Handle encoding issues and log errors for corrupted files.

2. **Exploratory Data Analysis**
    - Analyze document lengths, word frequencies, and document similarities.
    - Visualize distributions and identify common/rare legal terms.

3. **Document Chunking**
    - Split documents into manageable chunks for retrieval and LLM context windows.

4. **Vector Database Creation**
    - Generate embeddings using HuggingFace models.
    - Store chunk embeddings in a Chroma vector database for efficient similarity search.

5. **RAG Chain Setup**
    - Configure a retriever and a HuggingFace LLM (e.g., Flan-T5).
    - Build a RetrievalQA chain to answer questions using retrieved context.

6. **Evaluation**
    - Extract benchmark questions and answers.
    - Evaluate generated answers using ROUGE, BLEU, and RAGAS metrics.
    - Visualize and interpret results.

## Results & Insights

- Legal documents often use standardized templates, leading to high similarity scores.
- The RAG pipeline architecture is robust, but LLM quality and API limitations can be bottlenecks.
- Evaluation showed that free-tier LLMs may fail to generate meaningful answers for complex legal queries.
- Recommendations include using more powerful LLMs, refining chunking, and optimizing retrieval strategies.

## How to Run

1. Clone the repository and install dependencies (see notebook for pip commands).
2. Place your legal document corpus and benchmark files in the appropriate folders.
3. Run the Jupyter notebook step by step to process data, build the RAG system, and evaluate results.

## Dependencies

- Python 3.8+
- Jupyter Notebook
- langchain, chromadb, sentence-transformers, transformers
- scikit-learn, pandas, numpy, matplotlib, seaborn
- nltk, rouge_score, ragas

## License

This project is for educational and research purposes. Please ensure you have rights to use the legal documents in your corpus.

## Contact

For questions or collaboration, please open an issue or submit a pull request.
