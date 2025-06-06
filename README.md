uv venv
source .venv/bin/activate
export ANTHROPIC_API_KEY='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'
uv add arxiv mcp
uv run mcp_chatbot.py


# run the inspector
npx @modelcontextprotocol/inspector


# Git + Render

```git init````

```echo ".venv" > .gitignore```

```uv pip compile pyproject.toml > requirements.txt```