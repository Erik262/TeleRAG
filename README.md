# TeleRAG

Quick answers from your family's documents, right inside Telegram.

## The Problem

Family members often need a single piece of information buried in their documents (an insurance ID, a policy number, a contract date) and have to dig through folders and PDFs to find it.

## What It Does

TeleRAG is a retrieval-augmented assistant you chat with through a Telegram bot. You ask a short question about your documents and get a short, direct answer back. It is built for quick lookups, not for long conversations about your documents.

A typical interaction:

- **User:** What's my health insurance ID?
- **TeleRAG:** Your health insurance ID is A123456789.

Behind the scenes, TeleRAG searches the family's indexed documents for the relevant passage and has an LLM extract the answer from it.

## Setup

1. Install uv if you don't have it yet: https://docs.astral.sh/uv/getting-started/installation/

2. Clone this repository (or download the zip and extract it).

3. Create a `.env` file from the template and add your API key:

       cp .env.example .env

4. Install dependencies:

       uv sync

5. Start Jupyter:

       uv run jupyter notebook

## Notebooks

- `notebooks/01-setup.ipynb` - smoke test that confirms your environment works
- `notebooks/02-rag.ipynb` - a minimal RAG baseline you can adapt to your own data
