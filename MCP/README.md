# MCP Servers

## List of my preffered MCP servers (Under construction)


## List and descriptions

Below is a list of preferred MCP servers you can configure in your global `mcp.json`. For each, you'll find a short description, installation command, and any special notes:

---

- **Puppeteer MCP Server**
  - **Description:** Automates browser actions using Puppeteer. Useful for web scraping, testing, and automation tasks.
  - **Installation:**
    ```sh
    npx -y @modelcontextprotocol/server-puppeteer
    ```
  - **Notes:** No API key required.
  - **More info:** See [mcp_server_usage.mdc](../mdc/mcp_server_usage.mdc)

---

- **tavily-mcp**
  - **Description:** Provides AI-powered web search and extraction via Tavily.
  - **Installation:**
    ```sh
    npx -y tavily-mcp@0.1.3
    ```
  - **Notes:** Requires `TAVILY_API_KEY` in your environment.
  - **More info:** See [mcp_context7_usage.mdc](../mdc/mcp_context7_usage.mdc)

---

- **github**
  - **Description:** Integrates with GitHub for repository automation and management.
  - **Installation:**
    ```sh
    docker run -i --rm -e GITHUB_PERSONAL_ACCESS_TOKEN ghcr.io/github/github-mcp-server
    ```
  - **Notes:** Requires `GITHUB_PERSONAL_ACCESS_TOKEN`. Runs via Docker. [Read more](https://github.com/github/github-mcp-server?tab=readme-ov-file)
  - **More info:** See [mcp_git_usage.mdc](../mdc/mcp_git_usage.mdc)

---

- **taskmaster-ai**
  - **Description:** Advanced task and project management with AI (Anthropic, Perplexity).
  - **Installation:**
    ```sh
    npx -y --package=task-master-ai task-master-ai
    ```
  - **Notes:** Requires `ANTHROPIC_API_KEY` and `PERPLEXITY_API_KEY`. Supports model and subtask config in environment.
  - **More info:** See [mcp_task_management.mdc](../mdc/mcp_task_management.mdc)

---

- **context7**
  - **Description:** Enables code and documentation search using Context7.
  - **Installation:**
    ```sh
    npx -y @upstash/context7-mcp@latest
    ```
  - **Notes:** No API key required for basic use.
  - **More info:** See [mcp_context7_usage.mdc](../mdc/mcp_context7_usage.mdc)

---

You can add or customize these servers in your global `mcp.json` file, typically located at `/Users/YOUR_USERNAME/.cursor/mcp.json`.

### Store in your global mcp.json

The mcp.json is located somewhere like this: `/Users/YOUR_USERRNAME/.cursor/mcp.json`

```
{
  "mcpServers": {
    "Puppeteer MCP Server": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-puppeteer"
      ]
    },
    "tavily-mcp": {
      "command": "npx",
      "args": [
        "-y",
        "tavily-mcp@0.1.3"
      ],
      "env": {
        "TAVILY_API_KEY": "YOUR_API_KEY"
      }
    },
    "github": {
      "command": "docker",
      "args": [
        "run",
        "-i",
        "--rm",
        "-e",
        "GITHUB_PERSONAL_ACCESS_TOKEN",
        "ghcr.io/github/github-mcp-server"
      ],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "<YOUR_TOKEN>"
      }
    },
    "taskmaster-ai": {
      "command": "npx",
      "args": [
        "-y",
        "--package=task-master-ai",
        "task-master-ai"
      ],
      "env": {
        "ANTHROPIC_API_KEY": "YOUR_API_KEY",
        "PERPLEXITY_API_KEY": "YOUR_API_KEY",
        "MODEL": "claude-3-7-sonnet-20250219",
        "PERPLEXITY_MODEL": "sonar-pro",
        "MAX_TOKENS": "64000",
        "TEMPERATURE": "0.2",
        "DEFAULT_SUBTASKS": "5",
        "DEFAULT_PRIORITY": "medium"
      }
    },
    "context7": {
      "command": "npx",
      "args": [
        "-y",
        "@upstash/context7-mcp@latest"
      ]
    }
  }
}