# RAG Document Q&A Chatbot 

# Conversational RAG With PDF Uploads and Chat History

This project allows you to have a conversation with a Retrieval-Augmented Generation (RAG) system based on uploaded PDF files. The system uses Langchain, Groq LLM, and Streamlit to facilitate chat interactions that incorporate both PDF content and conversation history.

## Features

- **PDF Upload**: Upload one or more PDFs and interact with their content.
- **Chat History Awareness**: The system retains chat history and allows for conversational Q&A with the uploaded PDF documents.
- **Langchain-based Retrieval**: Utilizes Langchain for splitting, embedding, and retrieving document content.
- **Groq LLM Integration**: Uses Groq's `Gemma2-9b-It` model for generating responses.

## Installation

To run this project, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/rag-with-pdf.git
   ```

2. Navigate to the project directory:

   ```bash
   cd rag-with-pdf
   ```

3. Set up a virtual environment:

   ```bash
   python3 -m venv venv
   ```

4. Activate the virtual environment:

   - On macOS/Linux:

     ```bash
     source venv/bin/activate
     ```

   - On Windows:

     ```bash
     venv\Scripts\activate
     ```

5. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Set up your environment variables by creating a `.env` file at the root of your project. For example:

   ```env
   HF_TOKEN=your_huggingface_token
   GROQ_API_KEY=your_groq_api_key
   ```

2. Run the Streamlit app:

   ```bash
   streamlit run app.py
   ```

3. In the web interface, upload your PDF files and ask questions based on the content of the PDFs.

### API Keys

- You will need an API key from HuggingFace for embeddings and another API key from Groq for their LLM model. These should be stored in the `.env` file as shown in the example.

## Project Structure

```bash
.
├── app.py               # Streamlit app that runs the RAG system
├── .env                 # Environment variables (not included in repo)
├── .gitignore           # Ignores venv and environment files
├── requirements.txt     # Python dependencies
```

- **`app.py`**: The main application file for the project, which runs the Streamlit interface and handles PDF uploads, document retrieval, and chat interactions.
- **`.gitignore`**: Excludes the virtual environment and sensitive environment variables.
- **`requirements.txt`**: Contains the list of dependencies required to run the project.

## Dependencies

- `langchain`
- `langchain-community`
- `langchain-huggingface`
- `streamlit`
- `chromadb`
- `pypdf`
- `python-dotenv`
- `sentence_transformers`
- `groq` (for `ChatGroq` model integration)
- [See the full list in `requirements.txt`](requirements.txt).

These are automatically installed when you run `pip install -r requirements.txt`.

## How It Works

1. **PDF Upload**: You can upload one or more PDFs, which are processed and split into chunks for embedding.
2. **Contextual Questioning**: The RAG system combines the content from the uploaded documents and conversation history to answer your questions contextually.
3. **Answer Generation**: The system uses Groq's LLM to generate concise answers from the retrieved context.

## Customization

- You can adjust the chunk size for document splitting or modify the embeddings used in `app.py`.
- The Groq model can be replaced with any other LLM by updating the relevant section in `app.py`.

## License

This project is licensed under the MIT License.

---

Enjoy interacting with your PDFs!
