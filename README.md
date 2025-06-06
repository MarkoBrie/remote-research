```bash
uv venv
source .venv/bin/activate

uv add arxiv mcp
uv run mcp_chatbot.py
```

# Run the inspector
```npx @modelcontextprotocol/inspector```


# Git + Render 

Render requires pip and cannot use uv so we translate uv requirements to pip ones.  
We create a new github repository ```remote-research``` that is consumed by RENDER.

```bash
git init
```

```bash 
echo ".venv" > .gitignore
```

```bash 
uv pip compile pyproject.toml > requirements.txt
```

```bash 
echo "python-3.11.11" > runtime.txt
```

```bash 
git add .
```

```bash
git commit -m "ready for deployment"
```

### push an existing repository from the command line

```bash
git remote add origin https://github.com/MarkoBrie/remote-research.git
git branch -M main
git push -u origin main
```