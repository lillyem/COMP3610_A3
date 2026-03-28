# COMP3610 Assignment 3

LLM-Powered Applications and Distributed Computing

This repository contains my submission for COMP3610 Assignment 3. The notebook integrates:

- distributed analytics with PySpark on NYC Yellow Taxi data
- a RAG pipeline over NYC transportation policy PDFs
- a unified natural language application with query routing across structured data and documents

## Repository Structure

- `assignment3.ipynb`: Main notebook with all tasks, outputs, and interpretations
- `docs/`: PDF corpus used for RAG retrieval
- `requirements.txt`: Python dependencies
- `.gitignore`: Exclusions for large/generated artifacts

## Environment and Execution Notes

I developed and ran this assignment in Google Colab due to a local Hadoop/Spark environment issue.

The notebook is organized for reproducible execution from top to bottom.

## Setup

1. Create and activate a Python environment (optional):
   - `python -m venv .venv`
   - Windows: `.venv\Scripts\activate`
2. Install dependencies:
   - `pip install -r requirements.txt`

## How to Run

1. Set your API key using Google Colab Secrets:

   - In Colab, click the **(Secrets)** tab in the left sidebar
   - Add a new secret:
     - Name: `LLM_API_KEY`
     - Value: your provided course API key

2. Open `assignment3.ipynb` in Google Colab.

3. Run all cells sequentially from top to bottom.

4. Ensure all outputs remain visible before submission.

**Note:** The API key is not included in this repository for security reasons.

## Notes

- The NYC taxi parquet file and lookup CSV are downloaded programmatically in the notebook and are not committed to Git.
- The PDF documents are loaded from the `docs/` folder for the RAG pipeline.
- ChromaDB collections are persisted during runtime but excluded from version control.

## Assignment Coverage

- Part 1: Spark setup, cleaning, Spark SQL analytics, and optimization
- Part 2: Document ingestion, chunking, embeddings, RAG implementation, and evaluation
- Part 3: Query router, data query handler, and end-to-end integrated demo
- Part 4: Notebook documentation, code quality improvements, and repository organization

## AI Assistance Disclosure

AI assistance (ChatGPT) was used in the following ways during this assignment:

- Clarifying assignment requirements and marking criteria to ensure all tasks were addressed correctly.
- Providing guidance on implementing key components such as Spark SQL queries, the RAG pipeline, and query routing logic.
- Assisting with debugging issues in SQL generation, data processing, and LLM responses.
- Helping validate whether outputs from different sections (Spark results, RAG retrieval, evaluation metrics, and end-to-end demo outputs) were reasonable and aligned with expectations.
- Suggesting improvements to prompt design for SQL generation, RAG grounding, and hybrid response synthesis.
- Generating the `README.md`, `.gitignore`, and `requirements.txt`, and ensuring consistency with the notebook.