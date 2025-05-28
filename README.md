
# LangGraph Agentic AI with Tavily API, Arxiv, and Wikipedia

## Overview

This project sets up an agentic AI system using LangGraph, a framework built on LangChain for sophisticated, controllable agent workflows. The agent integrates three key tools:

- Tavily API for real-time web search,

- Arxiv for scientific paper retrieval,

- Wikipedia for general knowledge lookup.

The agent leverages LangGraph’s graph-based orchestration, memory integration, and human-in-the-loop capabilities to deliver robust, multi-step information retrieval and synthesis.

Architecture
Component	Description
LLM Agent	Core reasoning engine; orchestrates tool calls and synthesizes responses.
Tavily Tool	Integrates Tavily API for up-to-date web search results.
Arxiv Tool	Fetches and summarizes academic papers from Arxiv.
Wikipedia Tool	Retrieves and summarizes Wikipedia articles.
Memory	Stores session and long-term context for continuity and personalization.


## Workflow
User Query: The agent receives a user question.

Tool Selection: The LLM agent evaluates which tool(s) are best suited for the query (e.g., Tavily for news, Arxiv for research, Wikipedia for general facts).

Tool Invocation: The agent calls the selected tool(s), gathers results, and updates its internal state.

Reasoning Loop: The agent may iterate, calling additional tools or refining queries based on previous observations.

Response Generation: Synthesizes a comprehensive answer, optionally citing sources.

Human-in-the-Loop (Optional): Pauses for human review or intervention if required.

Delivery: Returns the final answer to the user.

## Setup Steps

Install Dependencies

* pip install langgraph langchain langchain-tavily wikipedia arxiv

## Configure API Keys

Obtain and set your Tavily API key and Groq API key.

## Tools
Tavily: Use the langchain-tavily integration to create a search tool.

Arxiv: Use the arxiv Python package or LangChain’s Arxiv tool.

Wikipedia: Use the wikipedia Python package or LangChain’s Wikipedia tool.

## Example Use Cases
- Research Assistant: Answers technical or academic questions by pulling from Arxiv and Wikipedia, supplementing with Tavily for the latest news.

- Conversational Agent: Engages in multi-turn dialogue, leveraging memory and multi-source retrieval for context-rich responses.

- Web-Powered Q&A: Handles real-time, complex queries requiring synthesis from multiple sources.

## References
- LangGraph documentation and tutorials

- Tavily API integration guides

- Example agentic RAG workflows

- Wikipedia agent walkthroughs

## Notes
LangGraph enables flexible, production-ready agentic systems with robust state management and human-agent collaboration.

The agent can be extended with additional tools or custom logic as needed.

For detailed code examples and advanced customization, refer to the official LangGraph and LangChain documentation.
