# rag-for-beginners

This is a step-by-step tutorial project on building a Retrieval-Augmented Generation (RAG) application.

## How to Run the Project

Follow these steps to set up your environment and run the scripts in order.

### 1. Set up a Python Virtual Environment
It's recommended to use a virtual environment to avoid dependency conflicts.
```bash
python3 -m venv venv
source venv/bin/activate
```

### 2. Install Dependencies
Install the required Python packages from the `requirements.txt` file:
```bash
pip install -r requirements.txt
```

### 3. Set Up Environment Variables
Ensure you have a `.env` file in the root directory with a valid OpenAI API key:
```env
OPENAI_API_KEY=your_openai_api_key_here
```

### 4. Run the Python Scripts
The scripts should be run sequentially, starting with document ingestion to build the database.

**Step 1: Document Ingestion** (Reads files from `docs/` and creates a local `db/chroma_db`)
```bash
python 1_ingestion_pipeline.py
```

**Step 2: Retrieval Pipeline** (Tests retrieving relevant data)
```bash
python 2_retrieval_pipeline.py
```

**Step 3: Answer Generation** (Passes retrieved documents to an LLM for answers)
```bash
python 3_answer_generation.py
```

You can continue exploring the other `.py` files individually (e.g., `4_history_aware_generation.py`, `5_recursive_character_text_spliiter.py`) to learn about different RAG concepts.

### 5. Running the Jupyter Notebooks
For interactive files like `12_hybrid_search.ipynb` and `8_multi_modal_rag.ipynb`, you can either open them in VS Code (with the Jupyter extension installed) or run a Jupyter server in your terminal:
```bash
jupyter notebook
```
