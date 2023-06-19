# PDF GPT

This project uses streamlit and Large language model to interact with your pdf you upload and give you insights on it and answer questions around it.

requirements : pip install streamlit pypdf2 langchain python-dotenv faiss-cpu openai huggingface_hub tiktoken

The pdf's are converted to string , then that string is converted into chunks of texts.
then we create embeddings of those chunks using an algorithm
And store it into a vector database.

When we ask a question, that question is converted as embeddings by the same algorithm and a semantic search is conducted in the vector database.

Then the ranked results are passed to a LLM, and then the answer is provided.