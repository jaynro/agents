# Agents Project

This project contains AI agents built with Google's Agent Development Kit (ADK).

## Requirements

- Python 3.11 or higher
- Google API Key

## Setup

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd agents
   ```

2. **Create and activate virtual environment**
   ```bash
   python3.11 -m venv .venv
   source .venv/bin/activate  # On macOS/Linux
   # or
   .venv\Scripts\activate     # On Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**
   
   Create a `.env` file in the agent folder (e.g., `my_agent/.env`):
   ```
   GOOGLE_GENAI_USE_VERTEXAI=0
   GOOGLE_API_KEY=your_api_key_here
   ```

   Get your API key from [Google AI Studio](https://aistudio.google.com/app/apikey)

## Running the Agent

### CLI Mode

Run from the project root directory:

```bash
adk run my_agent
```

This will start an interactive CLI session where you can chat with the agent. Type `exit` to quit.

### UI Mode (Optional)

For a web-based interface:

```bash
adk ui my_agent
```

Then open your browser to the URL displayed (typically http://localhost:8000)

## Project Structure

```
agents/
├── my_agent/
│   ├── __init__.py
│   ├── agent.py          # Agent implementation
│   └── .env              # Environment variables (not in git)
├── .venv/                # Virtual environment (not in git)
├── .gitignore
├── requirements.txt
└── README.md
```

## Troubleshooting

- **API Key Error**: Make sure your `GOOGLE_API_KEY` in `.env` is valid
- **Import Error**: Ensure you're in the activated virtual environment
- **Wrong Directory**: Always run `adk` commands from the project root directory (`agents/`)
