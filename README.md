# LangChain Update

A collection of Jupyter notebooks exploring LangChain concepts and integrations. The notebooks use providers such as Groq and Google Gemini and build up from basic model calls to tools, structured output, and agent middleware.

## Notebooks

1. [`1-langchainintro.ipynb`](updatedlangchain/1-langchainintro.ipynb) — LangChain introduction
2. [`2-ModelIntegration.ipynb`](updatedlangchain/2-ModelIntegration.ipynb) — Integrating chat models, including Google Gemini and Groq
3. [`3-Tools.ipynb`](updatedlangchain/3-Tools.ipynb) — Defining and using tools
4. [`4-Messages.ipynb`](updatedlangchain/4-Messages.ipynb) — Working with messages and conversation history
5. [`5-Structureoutput.ipynb`](updatedlangchain/5-Structureoutput.ipynb) — Producing structured model output
6. [`6-middleware.ipynb`](updatedlangchain/6-middleware.ipynb) — Agent middleware concepts

## Requirements

- Python 3.14 or newer
- API keys for the model providers used in the notebooks
- [uv](https://docs.astral.sh/uv/) (recommended) or pip

## Setup with uv

Clone the repository and enter its directory, then install the project dependencies:

```bash
git clone https://github.com/sujalbhatt1718/UpdatedLangchain.git
cd UpdatedLangchain
uv sync
```

Start Jupyter from the project environment:

```bash
uv run jupyter lab
```

Open a notebook under `updatedlangchain/` and run its cells. The project includes `ipykernel` as a development dependency.

Alternatively, install the packages listed in `requirements.txt` with pip:

```bash
python -m pip install -r requirements.txt
python -m pip install ipykernel jupyterlab
```

## API keys

Some notebooks load credentials from a local `.env` file. Create that file in the project root and add only the keys you need, for example:

```dotenv
Groq_API_Key=your_groq_api_key
GROQ_API_KEY=your_groq_api_key
GOOGLE_API_KEY=your_google_api_key
```

Use the variable names expected by the notebook you are running. Never commit `.env` or paste real API keys into notebooks; `.env` is excluded by `.gitignore`.

## Notes

- Model provider accounts and API usage may incur costs or have separate rate limits.
- The notebooks are learning examples; run cells in order and review any provider-specific model names before use.
- The `src/langchainupdate` package currently contains a minimal starter entry point and is separate from the notebook lessons.
