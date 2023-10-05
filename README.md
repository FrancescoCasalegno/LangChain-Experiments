
# 🦜🔗 Langchain Experiments

This repo contains examples of using [LangChain](https://github.com/hwchase17/langchain)

## 📖 Contents

In particular, all main modules of LangChain are demonstrated in the notebooks.

1. [`1_MODEL_IO.ipynb`](1_MODEL_IO.ipynb) — Building blocks for interfacing with LLMs and Chat Models, using Prompt Templates and Output Parsers.
2. [`2_MEMORY.ipynb`](2_MEMORY.ipynb) — Using Memory buffers or summaries to store information during conversations, since LLMs are stateless.
3. [`3_CHAINS.ipynb`](3_CHAINS.ipynb) — Create more complex applications by connecting together multiple LLMs components into a Chain.
4. [`4_AGENTS.ipynb`](4_AGENTS.ipynb) — Create Agents that can leverage LLMs to interact with other Tools, from Wikipedia to Wolfram Alpha, from Google Search to Yahoo Finance.

## 🛠️ Setup

First of all you need to define some variables for the environment that will be used in the notebooks.
We do this with a `.env` file, so first copy the provided example `.env.example` to `.env` and fill in the values.

```bash
cp .env.example .env
# And now open ".env" with your favorite editor and fill in the values!
```

Then, all you need is to create a virtual environment and install the requirements.

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Then, simply open one of the notebooks and run the cells to see the results.
