# Pill-Pal💊

![PillPal_Logo](images/PillPal-logo.png)

## Problem Statement

Have you ever come across the thin piece of folded paper that is part of every drug prescription box. Usually the text is in very small print and typically provides information about dosages, side effects, storage instructions and much more. They are hard to read and understand and requires some effort to get answers to common questions that you as a patient might have.

## Solution

Create a product that answers these questions and actually makes the medical information more accessible and easier to understand - enter PillPal💊

A Retrieval Augmented Generation (RAG) based chatbot that answers questions based on the PDF document.

## Environement Setup

```bash
python -V
# Output: Python 3.12.1
```

```bash
# create a environment named -> samba-ai
python -m venv rag-ai
```

```bash
# activate the environment
source rag-ai/bin/activate
```

```bash
# deactivate the virtual environment
deactivate
```

```bash
# create a Jupyter Notebook kernel
pip install jupyter ipykernel
```

```bash
# add the virtual environment as a kernel for the jupyter notebook
python -m ipykernel install --user --name=rag-ai --display-name="Py3.12-rag-ai"
```

```bash
# verify kernel installation
jupyter kernelspec list
```

```bash
# If needed
jupyter kernelspec uninstall rag-ai
```

![Jupyter_Kernel](images/create_jupyter_kernel.PNG)

## ARCHITECTURE OF THE APPLICATION

### DATA SOURCES

- [DAILY MED](https://dailymed.nlm.nih.gov/dailymed/index.cfm)

### MODEL PROVIDERS

#### SambaNova Cloud

- **Model ID:** `Meta-Llama-3.2-3B-Instruct`
- **Developed by:** `META`
- [**Model Card**](https://huggingface.co/meta-llama/Llama-3.2-3B)
- [**LlamaIndex Docs**](https://docs.llamaindex.ai/en/stable/examples/llm/sambanova/)

#### EMBEDDING MODEL

- **Model ID:** `jina-embeddings-v3`
- **Developed by:** `JINA AI`
- **Max Input Tokens:** `8192`
- **Max Output Dimensions:** `1024`
- [**Model Card**](https://huggingface.co/jinaai/jina-embeddings-v3)
- [**LlamaIndex Docs**](https://docs.llamaindex.ai/en/latest/examples/embeddings/jinaai_embeddings/)

#### RERANK MODEL

- **Model ID:** `jina-reranker-v2-base-multilingual`
- **Model Size:** `278 M`
- **Developed by:** `JINA AI`
- [**Model Card**](https://huggingface.co/jinaai/jina-reranker-v2-base-multilingual)
- [**LlamaIndex Docs**](https://docs.llamaindex.ai/en/stable/examples/node_postprocessor/JinaRerank/)

#### GROQ

- **Model ID:** `llama-guard-3-8b`
- **Developed by:** `META`
- **Context Window:** `8,192 tokens`
- [**Model Card**](https://huggingface.co/meta-llama/Llama-Guard-3-8B)
- [**Groq Docs**](https://console.groq.com/docs/content-moderation)

## Built for

![RAG 'n' ROLL Amp up Search with Snowflake & Mistral Hackathon](https://snowflake-mistral-rag.devpost.com/)

![Hackathon_Banner](images/Hackathon-Banner.png)

## Resources

[Ideal Chunk Size of a RAG System](https://www.llamaindex.ai/blog/evaluating-the-ideal-chunk-size-for-a-rag-system-using-llamaindex-6207e5d3fec5)

[Metadata Customization](https://docs.llamaindex.ai/en/stable/module_guides/loading/documents_and_nodes/usage_documents/)
