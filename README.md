# Multi-Tool-Agent

A small Python agent example for calling multiple tools, including weather and time helper functions.

## What this folder is for

This repo defines a simple `google.adk`-based agent with:

- `agent.py`: the main agent and tool definitions
- `__init__.py`: package entrypoint exporting `root_agent`
- `.gitignore`: ignores Python build files, environments, and editor settings

The agent is designed to show how to expose multiple tools through one package.

## Features

- `get_weather(city)` — returns weather status for a city
- `get_current_time(city)` — returns the current time in a supported city
- `root_agent` — the agent object used by the ADK runtime

## Setup

1. Clone the repo:

   ```bash
   git clone https://github.com/chintanrabadiya/Multi-Tool-Agent.git
   cd Multi-Tool-Agent
   ```

2. Create a Python virtual environment:

   ```bash
   python -m venv .venv
   .venv\Scripts\Activate.ps1   # PowerShell
   .venv\Scripts\activate.bat  # cmd.exe
   ```

3. Install dependencies.

   Add any required packages for your runtime environment, for example:

   ```bash
   pip install google-adk
   ```

## .env file

This repo uses a `.env` file for local environment variables and secrets.

Create a `.env` file in the project root with the values you need. Example:

```text
# Example .env
GOOGLE_ADK_API_KEY=your_api_key_here
OTHER_SECRET=your_secret_value
```

Do not commit `.env` to Git. It is already ignored by `.gitignore`.

## Usage

Use this repo as a Python package:

```python
from multi_tool_agent import root_agent
```

The agent can then be loaded by a Google ADK runtime or any tool orchestration layer that expects an agent object.

## Git workflow

- `git status` — check changes
- `git add .` — stage files
- `git commit -m "message"` — commit
- `git push origin master` — push to GitHub

## Notes

- The repository currently uses the `master` branch locally.
- If you want to rename it to `main`, run:

  ```bash
  git branch -m main
  git push -u origin main
  ```
