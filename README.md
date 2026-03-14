# 🐉 D-RAGon_Psyche
> A psychologist in your pocket — evidence-grounded, not opinion-driven.
 
**D-RAGon_Psyche** is a locally-run RAG system that provides evidence-backed workplace wellbeing recommendations grounded in organizational psychology literature. It replaces generic chatbot advice with cited, theory-driven guidance drawn from 17 academic books.
 
---
 
## What It Does
 
1. **Guided Intake** — 4 structured questions capture the user's workplace context
2. **Narrative Synthesis** — answers are compressed into a psychological case summary
3. **RAG Retrieval** — the narrative queries a Chroma vector store of 8,059 chunks from 17 org psych books
4. **Psychologist Synthesis** — Llama-3.1-8B generates evidence-backed recommendations citing Kahn, Maslach, Demerouti and others
5. **Conversational Follow-up** — users can ask follow-up questions with full history awareness
6. **Parameter Scoring** — 11 psychological parameters (JD-R, MBI, Kahn frameworks) are scored per session
 
---
 
## Tech Stack
 
| Component | Tool |
|---|---|
| Embeddings | BGE-M3 (BAAI) |
| Vector Store | ChromaDB |
| LLM | Llama-3.1-8B via Ollama |
| RAG Orchestration | LangChain |
| UI | Gradio |
| Knowledge Graph | Pyvis |
| Visualization | Matplotlib |
 
---
 
## Knowledge Base
 
17 organizational psychology books including:
- *The Burnout Epidemic* — Jennifer Moss
- *Occupational Health Psychology* — Leka & Houdmont
- *The Fearless Organization* — Amy Edmondson
- *Organizational Behavior* — Robbins & Judge
- *Emotional Intelligence* — Daniel Goleman
- *(and 12 more)*
 
---
 
## Evaluation
 
Benchmarked on 20 workplace scenarios across 6 topics (burnout, stress, motivation, leadership, team dynamics, psychological safety) at 3 severity levels.
 
| Metric | Score |
|---|---|
| Recall@4 | 1.0 |
| Precision@4 | 0.463 |
| Faithfulness | 0.925 / 1.0 |
| Answer Quality | 3.825 / 5.0 |
 
---
 
## Setup
 
```bash
# 1. Clone the repo
git clone https://github.com/YOUR_USERNAME/D-RAGon_Psyche.git
cd D-RAGon_Psyche
 
# 2. Create environment
conda create -n dragon_v2 python=3.11
conda activate dragon_v2
 
# 3. Install dependencies
pip install -r requirements.txt
 
# 4. Pull the LLM
ollama pull llama3.1
 
# 5. Add your books to Data/Raw_Books/ and run ingestion
# Then open D-RAGon_Psyche_Production.ipynb and run all cells
```
 
---
 
## Project Structure
 
```
D-RAGon_Psyche/
├── Data/
│   ├── Raw_Books/          # PDF knowledge base
│   └── Eval_Stuff/         # Benchmark files
├── Chroma/                 # Vector store (generated)
├── D-RAGon_Psyche.ipynb           # Main dev notebook
├── D-RAGon_Psyche_Production.ipynb  # Clean production notebook
└── README.md
```
 
---
 
## Built By
 
**Team Rambo** — Archit Yadav, Sneha Kushwaha, Sahib Taj Singh, Hardik Tyagi  
*Hacked 4.0*
