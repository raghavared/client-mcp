# MCP (Model Context Protocol) Client

This repository contains a client implementation for the Model Context Protocol, which facilitates communication between LLMs (Large Language Models) and various external tools and services.

## Overview

The MCP Client orchestrates interactions between users, LLMs, and a variety of server-based tools. It allows LLMs to access external capabilities like email (Gmail), calendar, web browsing, memory storage, and search functionality.

## Structure

- `main.py`: Core implementation containing the LLMClient, Tool, and ChatSession classes
- `servers_config.json`: Configuration for connecting to various MCP servers (this file is gitignored)
- `.servers_config.json`: Template configuration file with placeholder values

## Configuration

The system uses a configuration file (`servers_config.json`) to define available MCP servers. This file contains sensitive information and is excluded from version control. A template (`.servers_config.json`) is provided with placeholder values.

### Available Servers

- **gmail**: Email access and management
- **calendar**: Calendar management
- **sequential-thinking**: Enables step-by-step reasoning
- **puppeteer**: Web automation capabilities
- **browsermcp**: Browser control and interaction
- **memory**: Persistent storage for conversations
- **brave-search**: Web search functionality

## Setup

1. Copy `.servers_config.json` to `servers_config.json`
2. Replace placeholder values with your actual API keys and credentials
3. Ensure environment variables are set properly (e.g., LLM_API_URL for the LLM service)

## Security Note

The configuration files contain sensitive information including OAuth tokens and API keys. Never commit the `servers_config.json` file to version control.

## Usage

The client manages communication with LLM providers and coordinates with various MCP servers to execute tools requested by the LLM during conversations.
