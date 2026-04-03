# YouTube Chatbot with RAG using LangChain

This project implements a Retrieval-Augmented Generation (RAG) system for answering questions based on YouTube video transcripts. It uses LangChain, Google Generative AI (Gemini), FAISS for vector storage, and the YouTube Transcript API to fetch and process video transcripts.

## Features

- Fetches transcripts from YouTube videos
- Splits transcripts into chunks for better retrieval
- Embeds chunks using Google Generative AI embeddings
- Stores embeddings in a FAISS vector database
- Retrieves relevant context using similarity search
- Generates answers using Gemini 3 Flash model
- Built as a LangChain chain for easy invocation

## Prerequisites

- Python 3.11 or higher
- Google Cloud API key with Generative AI enabled
- YouTube video with available transcripts

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Rahul-Chotaliya/Youtube-Chatbot.git
   cd youtube-chatbot-rag
   ```

2. Create a virtual environment:
   ```bash
   python -m venv myenv
   source myenv/bin/activate  # On Windows: myenv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up environment variables:
   - Copy `.env.example` to `.env`
   - Add your Google API key: `GOOGLE_API_KEY=your_api_key_here`

## Usage

1. Open the Jupyter notebook `rag-using-langchain.ipynb`
2. Run the cells in order to set up the environment and process a YouTube video
3. Modify the `video_id` variable to point to your desired YouTube video
4. Use the `main_chain.invoke("Your question here")` to ask questions about the video

### Example

```python
# After running the setup cells
answer = main_chain.invoke("What is the main topic of this video?")
print(answer)
```

## Project Structure

- `rag-using-langchain.ipynb`: Main Jupyter notebook with the RAG implementation
- `requirements.txt`: Python dependencies
- `.env.example`: Example environment variables file
- `README.md`: This file

## Dependencies

- youtube-transcript-api: For fetching YouTube transcripts
- langchain: Core LangChain library
- langchain-google-genai: Google Generative AI integration
- faiss-cpu: Vector database
- python-dotenv: Environment variable management

## License

This project is open source. Please check the license file for details.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.