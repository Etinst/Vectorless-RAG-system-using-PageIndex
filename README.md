# Vectorless RAG System using PageIndex - Student Improved Version

**Made by:** Darshan Nitin Barhate

This project demonstrates a vectorless Retrieval-Augmented Generation (RAG) system using PageIndex. Instead of using embeddings and a vector database, the project uses a document tree created by PageIndex. An LLM reads that tree, selects the most relevant sections, and then answers the question using those selected sections.

## What This Project Does

1. Uploads a PDF document to PageIndex.
2. Builds a tree-like index of the document.
3. Uses an LLM to search the tree and select useful sections.
4. Generates an answer using only the selected document sections.
5. Optionally compares the custom pipeline with the PageIndex chat API.

## Improvements Made

- Reorganized the notebook into clear sections.
- Removed hardcoded API keys and added `.env` support.
- Added checks for missing API keys and missing PDF files.
- Added helper functions for tree printing, node counting, tree compression, and safe JSON parsing.
- Replaced confusing finance-based routing rules with general course/document routing rules.
- Added a small evaluation section with multiple test questions.
- Cleared old notebook outputs so the notebook is cleaner for GitHub.
- Added this README, a requirements file, an `.env.example`, and a LaTeX improvement report.

## Files

- `Vectorless_RAG_PageIndex_Student_Improved.ipynb` - improved main notebook
- `README.md` - GitHub project explanation
- `requirements.txt` - Python dependencies
- `.env.example` - example environment variables
- `Darshan_Barhate_Improvement_Report.tex` - LaTeX report explaining the improvements

## Requirements

- Python 3.10 or newer
- Jupyter Notebook or JupyterLab
- PageIndex API key
- OpenAI API key
- A PDF document to test

Install dependencies:

```bash
pip install -r requirements.txt
```

## Setup

Create a `.env` file in the project folder:

```text
PAGEINDEX_API_KEY=your_pageindex_key_here
OPENAI_API_KEY=your_openai_key_here
PDF_PATH=./sample_document.pdf
OPENAI_MODEL=gpt-4o
```

Put your PDF in the same folder and update `PDF_PATH` if needed.

## How to Run

1. Open `Vectorless_RAG_PageIndex_Student_Improved.ipynb`.
2. Run the cells from top to bottom.
3. Change the sample questions to match your PDF.
4. Check which sections were selected and read the final answer.

## Project Idea in Simple Words

Normal RAG often converts text into vectors and searches a vector database. This project uses a different idea. PageIndex creates a tree of the document, almost like a table of contents. The LLM looks at that tree and chooses the sections that seem most useful. Then the LLM writes the answer from those sections.

This makes retrieval easier to understand because we can see the selected section titles and node IDs.

## Author

Darshan Nitin Barhate
