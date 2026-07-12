# lau-voice

## Intention

Voice interface for the Lau game platform — lets kids talk to their game world using natural language. Parses speech into structured commands, generates kid-friendly responses with emotional tone, and maintains conversation memory. Also translates git concepts (commits, branches, merges) into game n

## How It Works

`lau-voice` bridges the gap between a child speaking naturally ("I wanna build a castle!") and structured game commands. It:
1. **Parses speech** into typed `VoiceCommand` variants (Build, Move, Create, Teach, Explore, Save, Undo, Branch, Merge, Show)
2. **Responds** with emotionally-tagged `VoiceResponse` text — excited when building, gentle after mistakes, celebrating new creations
3. **Remembers** the conversation in a sliding window, so the assistant has context
4. **Narrates git concepts** as game stories — commits become "You built a crystal tower!", merges become "Your experiment worked!"
The entire pipeline is: `raw speech → VoiceParser::parse() → VoiceCommand → GameAssistant::respond() → VoiceResponse`, with each exchange recorded in `ConversationMemory`.

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Voice interface for the Lau game platform — lets kids talk to their game world using natural language. Parses speech into structured commands, generates kid-friendly responses with emotional tone, and

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (146 lines), mentions tests, includes examples.

- README length: 206 lines, 8300 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
