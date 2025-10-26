# Simple AI Agent

A simple CLI-based AI agent built with LangChain, LangGraph, and OpenAI, integrated with Firecrawl tools for web scraping, crawling, and data extraction.

## Overview

This script creates an interactive agent that processes user queries by leveraging Firecrawl's capabilities through MCP (Message-based Client Protocol). It uses GPT-4o-mini for reasoning and tool selection, allowing step-by-step handling of web-related tasks.

## Requirements

- Python 3.10+
- Dependencies: `langchain`, `langgraph`, `langchain-openai`, `langchain-mcp-adapters`, `mcp`, `python-dotenv`, `asyncio`
- API Keys: OpenAI (`OPENAI_API_KEY`) and Firecrawl (`FIRECRAWL_API_KEY`) stored in a `.env` file
- Node.js and npm (for running Firecrawl via npx)

Install dependencies with:
```
pip install langchain langgraph langchain-openai langchain-mcp-adapters mcp python-dotenv
```

## Usage

1. Create a `.env` file with your API keys:
   ```
   OPENAI_API_KEY=your_openai_key
   FIRECRAWL_API_KEY=your_firecrawl_key
   ```

2. Run the script:
   ```
   python main.py
   ```

3. Interact in the CLI:
   - Enter queries (e.g., "Scrape the latest news from example.com").
   - Type "quit" to exit.

The agent starts a local Firecrawl server and loads tools dynamically. It thinks step-by-step to select and use tools for tasks like scraping or crawling.

## Notes

- This is a basic implementation for demonstration purposes.
- Ensure Firecrawl is accessible via npx; install globally if needed: `npm install -g firecrawl-mcp`.
- Error handling is minimal; expand as needed for production use.
