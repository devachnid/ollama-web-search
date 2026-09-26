# Ollama Web Search Integration for Home Assistant

This custom integration connects Home Assistant to an Ollama LLM server and adds web search capabilities using a locally hosted SearXNG instance.

## Features

- Use Ollama as a local LLM agent in Home Assistant
- Supports Home Assistant's LLM tooling/function calling
- Adds a `web_search` tool that uses SearXNG for real-time web results
- Voice and text commands can trigger web searches via the model

## Requirements

- Home Assistant (2024.7 or newer recommended)
- Ollama server running and accessible
- A SearXNG instance reachable from Home Assistant, with the `json` output format enabled (under `search.formats` in SearXNG's `settings.yml`)

## Installation

1. Copy the `custom_components/ollama_with_websearch` folder to your Home Assistant `custom_components` directory.
2. Restart Home Assistant.
3. Add the Ollama integration via Settings > Integrations.
4. Enter your Ollama server URL and your SearXNG instance URL (e.g. `https://searx.example.org`).
5. Add a conversation agent or AI task and choose a model.

To change the SearXNG URL later, open the integration and choose **Reconfigure**.

## Usage

- Use Home Assistant's conversation or AI task features to interact with Ollama.
- Ask questions that require web search (e.g., "What's the latest news about Home Assistant?").
- The integration will use the `web_search` tool to fetch results from SearXNG and return them in the response.

## Tooling

- The integration automatically registers the `web_search` tool with Home Assistant's LLM API.
- No changes are required on your Ollama server; all tooling is managed by Home Assistant.

## Troubleshooting

- Check Home Assistant logs for errors related to Ollama or tool registration.
- Ensure your SearXNG instance is reachable from Home Assistant.

## Credits

- Ollama: https://ollama.com
- SearXNG: https://searxng.github.io

## License

MIT
