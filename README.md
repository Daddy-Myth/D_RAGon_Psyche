# 🐉 D-RAGon_Psyche
> A psychologist in your pocket — evidence-grounded, not opinion-driven.
 
**D-RAGon_Psyche** is a locally-run RAG system that provides evidence-backed workplace wellbeing recommendations grounded in 17 organizational psychology books. It replaces generic chatbot advice with cited, theory-driven guidance drawn from Kahn, Maslach, Demerouti and others.
 
📖 [Full Documentation → Notion](https://www.notion.so/D-RAGon_Psyche-Organizational-Psychology-Knowledge-Retrieval-System-311ff95a70998028839ed8f591fde4fe)
 
---
 
## How It Works
 
```
4 Guided Questions → Narrative Synthesis (LLM)
    ↓
Parameter Scoring — 11 psych parameters scored 0–10
    ↓
ChromaDB Retrieval — top-4 chunks from 8,059 indexed
    ↓
Psychologist Synthesis (LLM) — 3 evidence-backed recommendations + cited sources
    ↓
Conversational Follow-up — history-aware free chat mode
```
 
---
 
## Features
 
- **Guided intake** — 4 structured questions build a psychological case narrative
- **RAG retrieval** — BGE-M3 embeddings over 17 org psych books
- **Parameter scoring** — JD-R, MBI, and Kahn's frameworks scored per session
- **Conversational mode** — follow-up questions with query rewriting and 10-turn history
- **Knowledge graph** — interactive Pyvis graph mapping questions → frameworks → parameters → literature
- **Fully local** — no API fees, no data leaves your machine
 
---
 
## Tech Stack
 
| Component | Tool |
|---|---|
| Embeddings | BAAI/bge-m3 |
| Vector Store | ChromaDB |
| LLM | Llama-3.1-8B via Ollama |
| Orchestration | LangChain |
| UI | Gradio |
| Knowledge Graph | Pyvis |
| Parameter Scoring | Matplotlib |
 
---
 
## Evaluation
 
Benchmarked on 20 scenarios across 7 topics (burnout, stress, motivation, leadership, team dynamics, psychological safety, emotional exhaustion) at 3 severity levels.
 
| Metric | Score |
|---|---|
| Recall@4 | **1.0** |
| Precision@4 | **0.463** |
| Faithfulness | **0.925 / 1.0** |
| Answer Quality | **3.825 / 5.0** |
 
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
 
# 5. Add your own org psychology PDFs to Data/Raw_Books/
#    (see Notion docs for the full book list)
 
# 6. Open D-RAGon_Psyche_Production.ipynb and run all cells
```
 
---
 
## Project Structure
 
```
D-RAGon_Psyche/
├── Data/
│   ├── Raw_Books/          # PDF knowledge base (not included, see docs)
│   └── Eval_Stuff/         # Benchmark files
├── Chroma/                 # Vector store (generated, gitignored)
├── D-RAGon_Psyche_Production.ipynb   # Production notebook
├── D-RAGon_Psyche.ipynb              # Dev notebook
└── README.md
```
 
---
 
## Knowledge Base

17 organizational psychology books across 3 layers:

**Layer 1 — Core Org Psych**
- Organizational Behavior — Robbins & Judge
- Industrial and Organizational Psychology — Paul Levy
- Work and Organizational Psychology — John Arnold
- The Oxford Handbook of Organizational Climate and Culture — Schneider & Barbera
- Leadership in Organizations — Gary Yukl

**Layer 2 — Workplace Stress & Burnout**
- Occupational Health Psychology — Leka & Houdmont
- The Burnout Epidemic — Jennifer Moss
- Why Zebras Don't Get Ulcers — Robert Sapolsky
- The Stress Management Handbook — Eva Selhub
- Full Catastrophe Living — Jon Kabat-Zinn
- The Relaxation Response — Herbert Benson
- The Stress Proof Brain — Melanie Greenberg

**Layer 3 — Behavioral & Cognitive Foundations**
- Thinking, Fast and Slow — Daniel Kahneman
- Influence — Robert Cialdini
- Pre-Suasion — Robert Cialdini
- Emotional Intelligence — Daniel Goleman
- The Fearless Organization — Amy Edmondson

---
 
## Built By
 
Archit Yadav






