# event-bus

## Intention
**event-bus** is a lightweight, in-process publish/subscribe messaging system for Rust. It allows decoupled components to communicate through named topics without direct references to each other, using thread-safe handler registration and synchronous dispatch.

## How It Works
The `EventBus` maintains a `HashMap<String, Vec<HandlerFn>>` mapping topic names to handler lists. Each handler is an `Arc<dyn Fn(&str) + Send + Sync>` — a thread-safe closure that receives the message as a string.

**Subscription** (`subscribe`) acquires a mutex lock on the map, inserts the handler into the topic's vector, and releases the lock. This is O(1) amortized.

**Publication** (`publish`) acquires the mutex lock, iterates over the topic's handlers, and calls each one synchronously. Dis

## What It's For
The publish/subscribe pattern is fundamental to decoupled software architecture. When a user registers, the auth system shouldn't need to know about the email service, the analytics pipeline, or the welcome-message sender — it just publishes `"user.created"` and moves on. This library provides that pattern in 100 lines of dependency-free Rust, making it ideal for plugins, game engines, embedded sy

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (84 line README).

## Honest Assessment
Has documentation (84 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/event-bus](https://github.com/SuperInstance/event-bus)*
