
# 🦜🔗 Langchain Experiments

This repo contains examples of using [LangChain](https://github.com/hwchase17/langchain)

## 📖 Contents

In particular, all main modules of LangChain are demonstrated in the notebooks.

1. [`1_MODEL_IO.ipynb`](1_MODEL_IO.ipynb) — Building blocks for interfacing with LLMs and Chat Models, using Prompt Templates and Output Parsers.
2. [`2_MEMORY.ipynb`](2_MEMORY.ipynb) — Using Memory buffers or summaries to store information during conversations, since LLMs are stateless.
3. [`3_CHAINS.ipynb`](3_CHAINS.ipynb) — Create more complex applications by connecting together multiple LLMs components into a Chain.
4. [`4_AGENTS.ipynb`](4_AGENTS.ipynb) — Create Agents that can leverage LLMs to interact with other Tools, from Wikipedia to Wolfram Alpha, from Google Search to Yahoo Finance.
5. [`5_RETRIEVAL.ipynb`](5_RETRIEVAL.ipynb) — Implement Retrieval systems for running Question Answering over collections of documents or graph databases like knowledge graphs.

## 🛠️ Setup

First of all you need to define some variables for the environment that will be used in the notebooks.
We do this with a `.env` file, so first copy the provided example `.env.example` to `.env` and fill in the values.

```bash
cp .env.example .env
# And now open ".env" with your favorite editor and fill in the values!
```

Then, you need to create a virtual environment and install the Python requirements.

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Finally, if you want to run the Neo4j example (this is completely optional!!) in [`5_RETRIEVAL.ipynb`](5_RETRIEVAL.ipynb), you need to have a Neo4j instance running.
To do so, you first need to [install Docker](https://docs.docker.com/get-docker/), make sure that you have the Docker daemon running, and then run the following command.

```bash
docker run \
    --name neo4j \
    -p 7474:7474 -p 7687:7687 \
    -d \
    -e NEO4J_AUTH=neo4j/pleaseletmein \
    -e NEO4J_PLUGINS=\[\"apoc\"\]  \
    neo4j:latest
```
