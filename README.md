# ADK Currency Agent

A currency conversion agent built using the [Google Agent Development Kit (ADK)](https://github.com/google/adk-python).

## Features

- Currency conversion between multiple supported currencies using Frankfurter.
- A2A (Agent-to-Agent) protocol support.

## Prerequisites

- [uv](https://github.com/astral-sh/uv) package manager.

## Setup

1. **Switch to the agent directory:**
    ```bash
    cd adk_currency_agent
    ```

2. **Set the Google API Key:**
    ```bash
    export ENV=development
    ```

3. **Install dependencies:**
    ```bash
    uv sync
    ```

## Running the Server

You can start the A2A agent server using the following command:

```bash
uv run currency_agent
```

## API Endpoints

- **Agent Card:** `GET http://localhost:10999/.well-known/agent-card.json`
- **A2A Endpoint:** `POST http://localhost:10999/`

## Running the UI

```bash
cd src
adk web
```

## Example Prompt

```text
Find the list of supported EU currencies and show the exchange rate with USD in markdown format
```

```text
how much is 10 USD in CAD?
```

```text
how did the INR value fluctuate against USD from jan 1st, 2026 to now?
```

## Acknowledgement 

This sample is taken from the A2A Project samples' [repository](https://github.com/a2aproject/a2a-samples/tree/main/samples/python/agents/adk_currency_agent).
