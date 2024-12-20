# Chat-With-PDF-Using-RAG-Pipeline

## Overview

This project implements a Retrieval-Augmented Generation (RAG) pipeline that enables users to interact with semi-structured data extracted from PDF files. The system extracts, chunks, embeds, and stores the data for efficient retrieval, allowing users to ask natural language queries and get precise, context-aware responses.

## Features

- **PDF Text Extraction**: Extracts text content from PDF files.
- **Chunking**: Segments extracted text into manageable chunks for embedding and retrieval.
- **Embedding**: Converts text chunks into vector embeddings using a pre-trained model.
- **Vector Database**: Stores embeddings for efficient similarity-based retrieval using FAISS.
- **LLM Integration**: Uses OpenAI's GPT-4 to generate responses based on retrieved chunks.
- **Dynamic Querying**: Handles user input queries and provides accurate, context-driven answers.

## Requirements

To run this project, ensure the following libraries are installed:

- `PyPDF2`
- `langchain`
- `faiss`
- `numpy`
- `scikit-learn`

Install the dependencies using pip:

```bash
pip install PyPDF2 langchain faiss numpy scikit-learn
```

## How It Works

1. **Text Extraction**: The text is extracted from the PDF files using `PyPDF2`.
2. **Chunking**: The extracted text is divided into smaller chunks for better granularity during embedding and retrieval.
3. **Embedding**: The chunks are embedded using OpenAI's pre-trained embedding model.
4. **Storage**: The embeddings and chunks are stored in a FAISS vector database for efficient retrieval.
5. **Querying**: User queries are embedded and compared to stored embeddings to find the most relevant chunks.
6. **Response Generation**: Retrieved chunks are used as context for the GPT-4 model to generate accurate and detailed responses.

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/your-usrname/rag-pipeline.git
   cd rag-pipeline
   ```

2. Run the script:

   ```bash
   python script_name.py
   ```

3. Input the paths to the PDF files (comma-separated) and your query when prompted:

   ```plaintext
   Enter the paths of PDF files, separated by commas: file1.pdf, file2.pdf
   Enter your query: What is the unemployment rate for degree holders?
   ```

4. View the generated response in the terminal.

## Example

For a query like:

```plaintext
What is the unemployment rate for degree holders?
```

The system retrieves relevant information from the PDFs and generates a detailed answer based on the extracted context.

## File Structure

- `script_name.py`: Main script implementing the RAG pipeline.
- `README.md`: Documentation for the project.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

