# Simple RAG System for Generative AI Course

This repository contains a simple Retrieval Augmented Generation (RAG) system designed to answer questions about the "Hands-on Generative AI Course" offered by Educosys. It uses LangChain, ChromaDB, and HuggingFace embeddings.

## Table of Contents

* [Project Overview](#project-overview)
* [Features](#features)
* [Technologies Used](#technologies-used)
* [Installation](#installation)
* [Usage](#usage)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)

## Project Overview

This project demonstrates a basic RAG pipeline. It ingests course content from a URL, processes it, stores it in a vector database, and then uses a Large Language Model (LLM) to answer user queries by retrieving relevant information.

## Features

* **Document Ingestion:** Reads course content from a URL.
* **Text Chunking:** Splits documents into manageable pieces.
* **Vector Embeddings:** Generates embeddings using HuggingFace's `all-MiniLM-L6-v2` model.
* **Vector Store:** Uses ChromaDB for efficient storage and retrieval.
* **Retrieval Augmented Generation:** Combines retrieved information with an LLM (OpenAI or HuggingFace) for informed answers.
* **Flexible LLM Integration:** Supports both OpenAI and local HuggingFace models.

## Technologies Used

* **Python 3.x**
* **LangChain:** Framework for LLM applications.
* **ChromaDB:** Open-source embedding database.
* **HuggingFace Transformers & `sentence-transformers`:** For models and embeddings.
* **`langchain-openai` (optional):** For OpenAI LLM integration.
* **`langchain-huggingface`:** For HuggingFace LLM integration.
* **Other libraries:** `aiohttp`, `uvicorn`, `httpx`, `jsonschema`, `tiktoken`, etc.

## Installation

To set up the project:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/fatimakhattak2/simple_rag_using_url.git](https://github.com/fatimakhattak2/simple_rag_using_url.git)
    cd simple_rag_using_url
    ```

2.  **Create and activate a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: `venv\Scripts\activate`
    ```

3.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Alternatively, install manually: `pip install langchain_community langchainhub chromadb langchain langchain-openai sentence-transformers transformers`)*

4.  **Set up your OpenAI API Key (if using `ChatOpenAI`):**
    ```bash
    export OPENAI_API_KEY="your_openai_api_key_here"
    ```

## Usage

The core logic is in the `simple_rag_using_url.ipynb` Jupyter Notebook.

1.  **Open the Jupyter Notebook:**
    ```bash
    jupyter notebook simple_rag_using_url.ipynb
    ```

2.  **Run the cells sequentially:**
    The notebook guides you through loading content, creating embeddings, setting up the RAG chain, and asking questions. You can modify the `query` variable in the last cell to ask different questions.

    Example query:
    ```python
    query = "Are the recordings of the course available? For how long?"
    ```


## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions, please contact [Your Name/Email/GitHub Profile].
