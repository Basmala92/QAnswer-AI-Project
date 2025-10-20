**I made this project inspired by my graduation project which will be a whole 
management system for our college ,developing this idea we will be a making chat bot to help students with their books and any thing related to college.**


#  Multimodal PDF Question Answering with CLIP and FAISS

This project is a **PDF Question Answering system** that allows users to upload PDF documents, ask natural-language questions, and get accurate answers **directly extracted from the PDF content** — with **visual highlights** showing exactly where the answer appears.

It uses **SentenceTransformer’s CLIP model** for text embeddings and **FAISS** for efficient similarity search, enabling **semantic understanding** of questions and answers.

---

##  Features

-   **Semantic Search** — Finds relevant text based on meaning, not just keywords.  
-   **PDF Upload & Management** — Upload multiple PDFs and choose which one to query.  
-   **Answer Extraction** — Retrieves the most relevant answer snippet from the document.  
-   **Bounding Box Highlighting** — Highlights the answer’s exact position in the PDF page.  
-   **Efficient Retrieval** — Uses **FAISS** for fast vector search across large documents.  
-  **Multimodal Embeddings** — Powered by **CLIP (ViT-B/32)** for text-image understanding.  

 

##   Tech Stack

- **Python 3**
- **Google Colab**
- **FAISS (Facebook AI Similarity Search)**
- **PyMuPDF (fitz)** for text and coordinates extraction
- **Sentence Transformers (CLIP-ViT-B-32)**
- **PIL (Pillow)** for image rendering and highlighting
- **NumPy** for numerical operations

 

##   Project Workflow

1. **Upload PDFs** — The user uploads one or more PDF files into `/pdfs`.  
2. **Extract Text & Coordinates** — Each PDF page’s text blocks and bounding boxes are extracted.  
3. **Embed Sentences** — All text blocks are converted to dense embeddings using CLIP.  
4. **Build FAISS Index** — The embeddings are stored in a FAISS vector index for fast search.  
5. **Ask Question** — User types a natural-language question.  
6. **Retrieve Answers** — FAISS finds the most similar text block to the query.  
7. **Display Results** — The answer text and its location are shown, with a **red box highlight** on the original PDF page.

---


##  How to Use

1. **Run all cells** in the notebook or script.
2. **Upload your PDF files** when prompted.
3. Select a PDF from the list.
4. Enter your **question**.
5. View the **highlighted answer** directly in the notebook output.

Example interaction:
```
✅ PDFs uploaded to /pdfs
Available PDFs:
1. data_science_book.pdf
2. ai_research_paper.pdf

Choose a PDF number: 1
Ask your question: What is reinforcement learning?

Answer (Page 12):
Reinforcement learning is a type of machine learning where agents learn by receiving rewards or penalties for their actions.
```

---

##  Future Enhancements

- Add a **Streamlit UI** with a chat-style interface.  
- Integrate **image-based search** using CLIP’s image encoder.  
- Support **multi-page answers** and summaries.  
- Enable **deployment on Hugging Face Spaces** or **Colab + pyngrok**.


 
