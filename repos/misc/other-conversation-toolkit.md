# conversation-toolkit

**Cluster:** cs-implementations  
**Language:** Python  
**Source:** [SuperInstance/conversation-toolkit](https://github.com/SuperInstance/conversation-toolkit)

## Intention

Toolkit for conversational AI.

## How It Works

A Python library for managing multi-turn LLM conversations with context window optimization, message templates, and conversation history tracking.

## What It's For

Toolkit for conversational AI.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (247 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# Conversation Toolkit

A Python library for managing multi-turn LLM conversations with context window optimization, message templates, and conversation history tracking.

## Features

- **Message Management**: Create, format, and track messages with role-based organization
- **Conversation Tracking**: Full conversation lifecycle with UUID identification and timestamps
- **Context Window Management**: Token estimation and automatic context trimming strategies
- **Message Templates**: Reusable template engine for consistent prompt generation
- **History Management**: Search, summarize, and analyze conversation history
- **Multi-Format Support**: OpenAI and Anthropic API message formats

## Installation

```bash
pip install conversation-toolkit
```

## Quick Start

```python
from conversation_toolkit import Conversation, Role

# Create a conversation with a system message
conv = Conversation(system_message="You are a helpful assistant.")

# Add messages
conv.add_user("What is the capital of France?")
conv.add_assistant("The capital of France is Paris.")

# Get messages for OpenAI API
messages = conv.get_messages_for_api(format="openai")
print(messages)
# Output: [
#   {'role': 'system', 'content': 'You are a helpful assistant.'},
#   {'role': 'user', 'content': 'What is the capital of France?'},
#   {'role': 'assistant', 'content': 'The capital of France is Paris.'}
# ]

# Get conversation info
print(f"Messages: {conv.message_count}")
print(f"Estimated tokens: {conv.estimated_tokens}")
```

## Core Concepts

### Message

A `Message` represents a single message in a conversation:

```python
from conversation_toolkit import Message, Role

msg = Message(
    role=Role.USER,
    content="Explain quantum computing",
    metadata={"category": "science"}
)
```

### Conversation

A `Conversation` manages multiple messages:

```python
from conversation_toolkit import Conversation, ConversationOptions

# Create with custom options
options = ConversationOptions(
    max_messages=100,
    max_tokens=128000,
    auto_summarize=True,
    summarize_threshold=50
)

conv = Conversation(system_message="You are an expert tutor.", options=options)

# Add messages using convenience methods
conv.add_user("Teach me about recursion.")
conv.add_assistant("Recursion is when a function calls itself...")

# Filter messages
user_messages = conv.get_messages(role=Role.USER)
last_5 = conv.get_messages(last_n=5)
```

### Context Manager

Manage context window limits:

```python
from conversation_toolkit import ContextManager, ContextStrategy

manager = ContextManager(
    max_tokens=128000,
    strategy=ContextStrategy.DROP_OLDEST,
    reserve_tokens=1000
)

# Check if messages fit
info = manager.check_context(conv.messages)
print(f"Usage: {info.usage_percent:.1f}%")
print(f"Available: {info.available_tokens} tokens")

# Trim to fit if needed
trimmed = manager.trim_to_fit(conv.messages)

# Get formatted for API
api_messages = manager.get_messages_for_api(conv.messages, format="op
```
