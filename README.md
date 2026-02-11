# 1-Hour Research Agent Challenge

**Note**: the objective of this challenge is not to come up with the best possible solution. Not even to finish the challenge itself. 

It is fine if you don't know some tools mentioned below, this is part of the activity, we will go step by step and see how we can use them to solve the problem.

For the first 10/15 minutes, feel free to just ask questions (you can also ask questions later, but the first 10/15 minutes is a good time to get started).

## The Task

Prototype a simple web search agent from scratch. 

Let's assume we have a user who is asking a question and we need to find the answer to that question.

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

- Think aloud as you work. Think about the design of what you are building and how you will implement it.
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
