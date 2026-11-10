# Enterprise-RAG-Based-Customer-Support-Agent

LangGraph-powered support agent with RAG knowledge base and automatic escalation routing.

**Framework**: LangGraph + FAISS  
**LLM**: GPT-4o-mini  

## Setup

```bash
pip install -r requirements.txt
cp .env.example .env
```

Set `OPENAI_API_KEY` in `.env` to your API key.

For OpenRouter, use your OpenRouter key in `OPENAI_API_KEY` and add:

```dotenv
OPENAI_BASE_URL=https://openrouter.ai/api/v1
OPENAI_MODEL=openai/gpt-4o-mini
OPENAI_EMBEDDING_MODEL=openai/text-embedding-3-small
```

The selected chat and embedding models require available OpenRouter credits.

## Run

```bash
python agent.py

# Use your own .txt/.md knowledge base files
python agent.py --kb-dir docs/
```

## Features

- RAG over product knowledge base
- Automatic escalation detection for sensitive issues (billing disputes, data loss, etc.)
- Conversation history maintained
- Easily swap in your own knowledge base docs

## License and attribution

Adapted from the Customer Support Agent in [ashishpatel26/500-AI-Agents-Projects](https://github.com/ashishpatel26/500-AI-Agents-Projects).
Licensed under the MIT License; see [LICENSE](LICENSE).
