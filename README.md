# Mental Peace Bot

A small, honest prototype of a compassionate mental-health assistant built as a research/learning project. Not a replacement for professional care.

## What this project is

Mental Peace Bot is a compact prototype that demonstrates how an LLM-based assistant can be combined with local document retrieval to support conversational responses grounded in source material (PDFs). The goal is to explore tools and patterns — not to ship a clinical product.

## Status & scope

- Prototype: for experimentation and learning.
- Not a medical or therapeutic service. Do not use for crisis situations.
- Minimal infrastructure: runs from a Jupyter notebook, uses local vector storage, and requires external model/API credentials when using cloud LLMs.

## Key features

- Loads PDFs and splits them into chunks.
- Builds embeddings and a small local vector database (Chroma).
- Runs a retrieval-augmented QA loop using a configured LLM.

## Tech stack

- Python 3.10+
- Libraries used (examples in the notebook): `langchain_groq`, `langchain_core`, `langchain_community`, `chromadb`, `pypdf`, `sentence_transformers`
- Vector DB: Chroma (local persistence)
- LLM: ChatGroq (example), but the code can be adapted for other providers

## Requirements

- A working Python 3.10+ environment
- Pip-installable dependencies listed above (see quick install)
- If you intend to use the example cloud LLM, add the provider API key(s) as described in the notebook.

## Quick setup

1. Create and activate a virtual environment (recommended):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install the primary dependencies:

```powershell
pip install langchain_groq langchain_core langchain_community chromadb pypdf sentence_transformers
```

3. Prepare your PDFs in a data folder. The notebook expects a `data/` directory with PDF files.

4. If using a hosted LLM (example in the notebook uses Groq), set the appropriate API key in the notebook or via environment variables.

## Running

- Open and run `MENTAL_PEACE_BOT.ipynb` in Jupyter or JupyterLab.
- Run the cells in order: they install packages, build or load the Chroma DB, initialize the LLM, then start the simple chat loop.

## Usage notes & limitations (be real)

- This project is intentionally small and opinionated — it's a learning prototype, not production-ready software.
- Responses can be incorrect or misleading; always validate important outputs against trusted sources.
- There is no authentication, rate-limiting, or safety-hardening in the example notebook.
- If you plan to extend this, add unit tests, logging, secrets management, and safety filters.

## Contributing

- Contributions are welcome but expect small, focused changes. Open an issue first to discuss major ideas.

## Files of interest

- `MENTAL_PEACE_BOT.ipynb` — the runnable notebook with the prototype implementation and installation steps.

## License

This repository is provided as-is for educational purposes. No license file included; adapt as you see fit.

---

If you want, I can also: generate a `requirements.txt`, add a short example `config.example` for API keys, or extract the notebook logic into a small runnable script. Tell me which next step you prefer.
