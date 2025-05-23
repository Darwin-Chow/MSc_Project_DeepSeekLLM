## Configuration

OpenManus requires configuration for the LLM APIs it uses. Follow these steps to set up your configuration:

1. Create a `config.toml` file in the `config` directory (you can copy from the example):

```bash
cp config/config.example.toml config/config.toml
```

2. Edit `config/config.toml` to add your API keys and customize settings:

```toml
# Global LLM configuration
[llm]
model = "gpt-4o"
base_url = "https://api.openai.com/v1"
api_key = "sk-..."  # Replace with your actual API key
max_tokens = 4096
temperature = 0.0

# Optional configuration for specific LLM models
[llm.vision]
model = "gpt-4o"
base_url = "https://api.openai.com/v1"
api_key = "sk-..."  # Replace with your actual API key
```

## Quick Start

One line for run OpenManus:

```bash
python main.py --web
```

Then input your idea via terminal!

### Web Interface

You can also use OpenManus through a user-friendly web interface:

```bash
uvicorn app.web.app:app --reload
```
or
```bash
python web_run.py
```

Then open your browser and navigate to `http://localhost:8000` to access the web interface. The web UI allows you to:

- Interact with OpenManus using a chat-like interface
- Monitor AI thinking process in real-time
- View and access workspace files
- See execution progress visually

For unstable version, you also can run:

```bash
python run_flow.py
```
