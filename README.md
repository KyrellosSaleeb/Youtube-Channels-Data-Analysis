# 📊 YouTube Analytics AI Platform  
### End-to-End BI + AI Agent System for YouTube Data Analysis  
*ETL • Data Warehouse • SSAS Tabular Model • Power BI • LLM-Powered Analytical Agent • RAG Engine*

---

## 🧠 Project Overview

The **YouTube Analytics AI Platform** is a complete data, analytics, and AI system designed to ingest, transform, model, and analyze YouTube trending datasets using:

- A professional **Data Warehouse architecture**
- A semantic **SSAS Tabular Model** with advanced DAX measures
- A fully interactive **Power BI dashboard**
- A modern **LLM-powered Analytical Agent** using Groq + RAG

This platform allows business users to ask natural-language questions such as:

> “Show the top categories in Brazil.”  
> “Compare trend delay between United States of America and Canada.”  
> “Explain the Trend Delay metric.”

The AI Agent automatically:  
✔ Understands the question  
✔ Normalizes country names  
✔ Classifies intent (SQL / DAX / RAG)  
✔ Generates and executes the correct query  
✔ Retrieves relevant documentation  
✔ Produces a clean, structured, streaming answer  

---

## 🏗️ System Architecture

```
Raw CSV Data
      │
      ▼
┌────────────────────┐
│   Python ETL Layer │
└─────────┬──────────┘
          ▼
┌────────────────────┐
│        ODS         │
└─────────┬──────────┘
          ▼
┌────────────────────┐
│        STG         │
└─────────┬──────────┘
          ▼
┌───────────────────────────┐
│      SQL Server DWH       │
│ Fact + Dimension Tables   │
└────────────┬──────────────┘
             ▼
┌───────────────────────────┐
│     SSAS Tabular Model    │
│ DAX Measures + Semantics  │
└────────────┬──────────────┘
             ▼
┌───────────────────────────┐
│      Power BI Dashboard   │
└────────────┬──────────────┘
             ▼
╔════════════════════════════════════════════╗
║       🔥 AI Analytical Agent (LLM)         ║
║ SQL Chain • DAX Chain • RAG Chain • Memory ║
╚════════════════════════════════════════════╝
```

---

## 🔥 Core Features

### ✔ Full BI Pipeline
- Python ETL  
- SQL Server ODS → STG → DWH  
- Star Schema modeling  
- Fact & dimension tables  

### ✔ SSAS Tabular Model
- Complete semantic model  
- Relationship modeling  
- Optimized DAX measures (TotalViewCounts, AvgTrendDelay, Top Category, etc.)

### ✔ Power BI Dashboard
- Views by country  
- Trending patterns  
- Category performance  
- Trend delay insights  
- Disabled comments & ratings analysis  

### ✔ AI Analytical Agent (rag_llm.py)
- Natural-language interface  
- Intent classification (SQL / DAX / RAG)  
- Automatic country name normalization  
- SQL query generation & execution  
- DAX execution via ADOMD  
- Strict RAG grounding (no hallucinations)  
- Streaming output  
- Memory window for last 9 messages  

---

## 🤖 AI Agent Architecture

### 1️⃣ Country Name Normalization  
Automatically expands abbreviations like "USA" → "United States of America".

### 2️⃣ Intent Detection  
Classifies questions into:
- SQL Query  
- DAX Query  
- RAG (document-based response)

### 3️⃣ Query Execution Layers  
- SQL chain → Executes SQL on Data Warehouse  
- DAX chain → Executes DAX on SSAS Tabular Model  
- RAG chain → Uses FAISS + Groq LLM to produce grounded answers  

### 4️⃣ Streaming Response Formatting  
Each answer includes:
1. Introduction  
2. Clean Data / Tables  
3. Explanation  
4. Recap  
5. Follow‑up question  

---

## 🖥️ Streamlit Chat Interface

- Real-time token streaming  
- Full conversation log  
- Sliding window memory (last 9 turns)  
- Markdown responses  
- No hallucinations for RAG answers  

---

## ⚙️ Setup Instructions

### Install Dependencies
```
pip install -r requirements.txt
```

### Add Environment Variables  
Create `.env`:
```
GROQ_KEY=your_api_key_here
```

### Run the System
```
streamlit run app.py
```

---

## 🧿 Technologies Used

### Data Engineering
Python • SQL Server • SSIS • SSAS  

### AI & NLP
Groq • LangChain • FAISS • MiniLM Embeddings • RAG  

### Visualization
Power BI • Streamlit  

---

## 🏁 Conclusion

The **YouTube Analytics AI Platform** combines:
- Enterprise BI engineering  
- Strong semantic modeling  
- Intuitive dashboarding  
- Advanced AI reasoning  
- RAG-powered correctness  

A production-ready blueprint for AI-driven analytics systems.
