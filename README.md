# PDF Structured Data Extraction using Gemini RAG

## Overview
This project extracts structured information from unstructured PDF documents using a Retrieval-Augmented Generation (RAG) pipeline powered by Google Gemini. The system parses PDF files, converts the content into searchable chunks, retrieves the most relevant sections, and uses a large language model to generate structured answers.


## What is this project?
This repository implements a pipeline that allows users to query PDF documents and extract meaningful structured information from them. Instead of manually reading long documents, the system retrieves relevant sections and uses an LLM to interpret and summarize the content.

Key features:
- Upload and process PDF documents
- Semantic search over document content
- LLM-powered structured information extraction
- Simple Streamlit interface for interacting with documents

---

## Why is this helpful?
Many documents such as research papers, reports, and invoices contain important information buried inside large blocks of text. Manually scanning these documents is time-consuming.

This project helps by:
- Automatically extracting key information from PDFs
- Reducing time spent reading long documents
- Enabling quick document search and analysis
- Making unstructured data easier to work with

---

## Who can use this?
This tool can be useful for:

- **Researchers** analyzing academic papers  
- **Business analysts** extracting insights from reports  
- **Students** quickly understanding long documents  
- **Developers** building AI document processing systems  

---

## How was this built?
The system uses a Retrieval-Augmented Generation architecture.

Pipeline:

```

PDF → Loader → Text Splitter → Embeddings → Vector Database → Retriever → Gemini LLM → Structured Response

```

Main technologies used:
- **Python**
- **LangChain**
- **Google Gemini (Gemini Flash 2.5)**
- **ChromaDB** for vector storage
- **PyPDF** for document loading
- **Streamlit** for the web interface

---

## Project Structure

```

pdf-structured-data-extraction
│
├── app
│   ├── streamlit_app.py
│   └── functions.py
│
├── data
│   └── sample PDFs
│
├── requirements.txt
├── .env
└── README.md

````

---

# Running the Project

## 1. Clone the repository

```bash
git clone https://github.com/amruthavedantham/pdf-structured-data-extraction.git
cd pdf-structured-data-extraction
````

---

## 2. Create a virtual environment

```bash
python -m venv myenv
```

Activate it:

### Windows

```bash
myenv\Scripts\activate
```

### Mac/Linux

```bash
source myenv/bin/activate
```

---

## 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 4. Add your Gemini API key

Create a `.env` file in the project root:

```
GOOGLE_API_KEY=your_gemini_api_key_here
```

You can obtain a key from Google AI Studio.

---

## 5. Run the Streamlit application

```bash
streamlit run streamlit_app.py
```

This will start a local web app where you can upload PDFs and ask questions about them.

---

# Future Improvements

Possible enhancements include:

* Support for multiple PDFs at once
* Improved structured JSON extraction
* Document summarization features
* Exporting results to CSV or databases

---

# License

This project is open source and available for educational and research purposes.

```
```

