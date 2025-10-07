# 🧠 Hybrid Search with RAG (Retrieval-Augmented Generation)


> 🚀 A project demonstrating **Hybrid Search** — combining **semantic embeddings** and **keyword-based BM25 retrieval** using **LangChain**, **Pinecone**, and **Hugging Face**.  
> This serves as the **retrieval backbone** for modern **RAG (Retrieval-Augmented Generation)** systems.

---

## 📘 Overview

This project showcases how to implement a **hybrid search mechanism** that merges the best of both retrieval methods:

- **Dense retrieval** for semantic understanding using embeddings  
- **Sparse retrieval** for exact keyword matching using BM25  

By combining them, the system delivers **more accurate and context-aware results**, forming the foundation for **RAG-powered AI applications** such as chatbots, knowledge assistants, and Q&A systems.

---

## 🧩 Project Workflow

1. **Environment Setup**
   - Install and import all required dependencies.
   - Initialize Pinecone client using your API key.
   - Create a vector index for hybrid search.

2. **Embedding Models**
   - Dense Embeddings → `HuggingFaceEmbeddings(all-MiniLM-L6-v2)`
   - Sparse Embeddings → `BM25Encoder()` from `pinecone-text`

3. **Hybrid Retriever Creation**
   - Combine both embedding types using `PineconeHybridSearchRetriever` from LangChain.

4. **Data Ingestion**
   ```python
   sentences = [
       "In 2023, I watched Attack on Titan: The Final Season",
       "In 2022, I watched Demon Slayer: Entertainment District Arc",
       "In 2021, I watched Jujutsu Kaisen"
   ]
   retriever.add_texts(sentences)




5.  **Hybrid Search Query**

retriever.invoke("Which anime did I watch in 2022?")


✅ Output:
In 2022, I watched Demon Slayer: Entertainment District Arc




⚙️ **Tech Stack**

Technology	               Purpose
Python	                   Programming Language
LangChain                  Framework for retrievers & chaining LLM components
Pinecone                 	 Vector database for dense & sparse retrieval
Hugging Face               Transformers	Generate semantic embeddings
BM25 Encoder               (Pinecone Text)	Perform keyword-based retrieval
dotenv	                   Manage environment variables securely




**🧠 What is RAG?**

Retrieval-Augmented Generation (RAG) combines:

Retriever → fetches relevant documents using hybrid search

Generator → an LLM (like GPT, LLaMA, or Gemini) that uses retrieved data to generate accurate, grounded answers

This project focuses on building the retrieval layer — the most critical part of any RAG pipeline.





**🔍 Key Features**

✅ Combines semantic and keyword-based retrieval

⚡ Uses Pinecone for scalable, low-latency vector search

🧠 Integrates Hugging Face embeddings (all-MiniLM-L6-v2)

🔧 Implements BM25 sparse retrieval for keyword precision

💬 Forms the foundation of a RAG-based AI system




**🧱 Setup Instructions**




1️⃣ Clone the Repository
git clone https://github.com/your-username/hybrid-search-with-rag.git
cd hybrid-search-with-rag



2️⃣ Install Dependencies
pip install --upgrade pinecone-client pinecone-text langchain_community langchain_huggingface



3️⃣ Add Environment Variables

Create a .env file and add your Pinecone API key:
PINECONE_API_KEY=your_api_key_here



4️⃣ Run the Script
python hybrid_search_with_rag_.py



🧾 Example Output
Query: Which anime did I watch in 2022?
Result: In 2022, I watched Demon Slayer: Entertainment District Arc



💡 Use Cases

🤖 Chatbots with contextual memory

🧾 Document Question Answering

🧠 AI-powered search systems

📚 Knowledge base augmentation for LLMs

🔎 Semantic + keyword search applications

🚀 Future Enhancements

Integrate with LLMs (GPT, Gemini, LLaMA) for full RAG pipeline

Add document chunking and metadata filtering

Implement hybrid reranking using cross-encoders

Extend retrieval to multi-modal (text + image) data




📚 Learning Outcomes

Through this project, you’ll gain hands-on understanding of:

Vector databases and hybrid search

Dense vs. sparse retrieval methods

Embedding models and BM25 encoding

RAG architecture fundamentals

Real-world AI search pipelines





🤝 Contributing

Contributions are welcome!
If you’d like to improve this project or extend it into a full RAG pipeline, feel free to fork and submit a pull request.




📄 License

This project is licensed under the MIT License – free to use and modify.




🧑‍💻 Author

AI Engineer | Building Intelligent Systems with LLMs, RAG, and Hybrid Retrieval




🌐 Connect With Me

💼 LinkedIn - www.linkedin.com/in/siddhant-uke

🐙 GitHub - https://github.com/SiddhantUke

