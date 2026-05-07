# What is AI?

AI (Artificial Intelligence) is software that can perform tasks that typically require human-level understanding, things like reading text, answering questions, writing code, and summarizing documents.

## What is an LLM?

An **LLM (Large Language Model)** is the specific type of AI that powers tools like Claude. Here's how it works at a high level:

- **Trained on text:** An LLM is trained on a massive amount of written text (books, websites, code, documentation). Through that training it learns patterns in language: grammar, facts, reasoning, and how ideas connect.
- **Predicts the next word:** When you send a message, the model generates a response one word (technically one "token") at a time, each time predicting what word should come next given everything before it.
- **Not a search engine:** An LLM doesn't look anything up. It generates responses from what it learned during training. This is why it can be wrong and produce a confident-sounding answer that isn't accurate.
- **Context window:** The model can only "see" the current conversation. It has no memory of past conversations unless you explicitly provide that context.

## What Claude is

Claude is Anthropic's LLM. It is designed to be helpful, harmless, and honest. When you use Claude.ai, Claude Code, or Claude Cowork, you are sending messages to Claude and receiving generated responses in return.

## What Claude is good at

- Writing and refactoring code based on a description of what you want
- Explaining unfamiliar code, queries, or error messages
- Drafting stored procedures, scripts, and boilerplate from a template or example
- Summarizing documents and extracting key information
- Debugging when you give it the full error message and relevant context
- Generating first drafts that you review and refine

## What Claude is not good at

- Anything that requires live data — it has no connection to your database or the internet unless a tool provides it
- Knowing your environment without being told — schema, platform, naming conventions all need to be provided
- Tasks where accuracy is critical and unverified — always review output before using it in production
- Long chains of dependent logic without checkpoints — break complex tasks into steps and verify as you go

## What to keep in mind

- Claude can make mistakes. Always review its output, especially for code and data.
- Claude does not have access to the internet or live data unless a tool explicitly provides it.
- The quality of the response depends heavily on how clearly you phrase your request.
