# 1-Hour Research Agent Challenge

## The Task

Prototype a "Research Agent" from scratch. We will start with a simple question and iterate on the complexity together.

## The Stack

- **Search:** Tavily API. Tavily will return documents that are relevant to the query.
- **LLM:** Together AI. LLM that will synthesize the context and generate the final answer.

- **Coding Agent:** Your choice (Cursor, Claude, etc.)


## Expected Pipeline

```text
+--------+    +--------+    +--------------+    +--------+
| Query  | -> | Search | -> | Docs/Context | -> | Answer |
+--------+    +--------+    +--------------+    +--------+
```

## Main Functions

- Tavily search: `TavilyClient.search(query="...")`
- LiteLLM completion: `completion(model="...", messages=[...])`
- How it works: run Tavily search to fetch context, then pass that context to LiteLLM completion to generate the final answer.

## Instructions

- Think aloud as you work.
- We want to see how you approach the task, debug API responses, and iterate on your solution.

## Requirements

- **Package manager:** [uv](https://docs.astral.sh/uv/)
- **Dependencies:** `tavily-python`, `litellm`

### Docs

- Tavily Search API: https://docs.tavily.com/documentation/api-reference/endpoint/search
- Tavily Python SDK: https://docs.tavily.com/sdk/python/reference
- LiteLLM – Make a Request: https://docs.litellm.ai/docs/

## API Keys

- `TAVILY_API_KEY`: ...
- `TOGETHER_API_KEY`: ...
