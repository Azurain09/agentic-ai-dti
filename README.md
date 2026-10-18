# Agentic AI DTI - Credit and Collections Assistant

An intelligent agent prototype for a small Peruvian store that manages credit sales (fiados), payments, customer history, and basic collection decisions. The project was developed for the DTI Agentic AI course.

## What it demonstrates

- Tool-using LLM agent built with LangChain.
- Conversational memory for multi-step interactions.
- SQLite persistence for customers, credit sales, payments, and history.
- Data validation for identifiers, phone numbers, amounts, and dates.
- Business rules for credit categories and account status.
- Financial summaries and data visualizations generated on demand.
- Interactive notebook interface for a controlled demonstration.

## Architecture

```text
User request
    |
LangChain agent + conversation memory
    |
Business tools: customers | credit sales | payments | reports | charts
    |
SQLite database + generated demo data
```

## Tech stack

- Python
- LangChain and OpenRouter-compatible LLM API
- SQLite
- Pandas, Matplotlib, and Seaborn
- Jupyter Notebook and ipywidgets

## Run locally

1. Create and activate a virtual environment.
2. Install the dependencies.
3. Set an API key in your local environment.
4. Open the notebook in Jupyter or VS Code.

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
$env:OPENROUTER_API_KEY = "your-key-here"
```

Open [notebooks/agentic-credit-collections-assistant.ipynb](notebooks/agentic-credit-collections-assistant.ipynb) and run the cells in order. The notebook requests the key securely when it is not available in the environment.

## Security and privacy

- The published notebook has no executed outputs, API keys, personal records, or local database files.
- `.env`, SQLite databases, CSV exports, generated charts, and local session artifacts are ignored by Git.
- All data used in a public demonstration must be synthetic.
- Never paste provider keys into notebook cells or commit them to Git.

## Portfolio framing

This project is a prototype, not a production banking or credit-scoring platform. It demonstrates applied agentic AI: connecting an LLM to constrained tools, persistent data, validation rules, and practical business workflows.
