# Automatic-Type-Safe-IndexedDB

**Cluster:** typescript-misc  
**Language:** TypeScript  
**Source:** [SuperInstance/Automatic-Type-Safe-IndexedDB](https://github.com/SuperInstance/Automatic-Type-Safe-IndexedDB)

## Intention

Type-safe wrapper for IndexedDB.

## How It Works

> **Type-safe IndexedDB wrapper with automatic schema migrations and query builder**

## What It's For

Type-safe wrapper for IndexedDB.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

TypeScript — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (509 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# @superinstance/automatic-type-safe-indexeddb

> **Type-safe IndexedDB wrapper with automatic schema migrations and query builder**

[![TypeScript](https://img.shields.io/badge/TypeScript-5.6-blue)](https://www.typescriptlang.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![npm version](https://img.shields.io/npm/v/@superinstance/automatic-type-safe-indexeddb.svg)](https://www.npmjs.com/package/@superinstance/automatic-type-safe-indexeddb)

A modern, type-safe TypeScript wrapper around IndexedDB with full async/await support, automatic migrations, and a powerful query builder. Makes working with IndexedDB as easy as working with an ORM.

## ✨ Features

- 🔒 **Full Type Safety** - Complete TypeScript support with inferred types
- ⚡ **Async/Await API** - Promise-based API for modern async JavaScript
- 🔄 **Automatic Migrations** - Schema versioning with automatic upgrades
- 🔍 **Query Builder** - Powerful querying with filtering, sorting, and pagination
- 📦 **Zero Dependencies** - Lightweight, pure TypeScript
- 🎯 **Simple API** - Intuitive methods that feel like working with arrays
- 🛠️ **Migration System** - Easy database schema migrations
- 📊 **Transaction Support** - Multi-store transactions with type safety

## 🚀 Quick Start

### Installation

```bash
npm install @superinstance/automatic-type-safe-indexeddb
```

### Basic Usage

```typescript
import { TypeSafeDB } from '@superinstance/automatic-type-safe-indexeddb';

// Define your data model
interface User {
  id: number;
  name: string;
  email: string;
  age: number;
  createdAt: number;
}

// Create database instance
const db = new TypeSafeDB({
  name: 'MyDatabase',
  version: 1,
  migrations: [
    {
      version: 1,
      up: (db) => {
        // Create users object store
        const userStore = db.createObjectStore('users', { keyPath: 'id', autoIncrement: true });
        userStore.createIndex('email', 'email', { unique: true });
        userStore.createIndex('age', 'age');
        userStore.createIndex('name', 'name');
      },
    },
  ],
});

// Initialize database
await db.initialize();

// Get store operations (fully typed!)
const users = db.store<User>('users');

// CRUD operations
await users.add({
  name: 'John Doe',
  email: 'john@example.com',
  age: 30,
  createdAt: Date.now(),
});

// Get by ID
const user = await users.get(1);
console.log(user); // { id: 1, name: 'John Doe', email: 'john@example.com', age: 30, ... }

// Get all users
const allUsers = await users.getAll();

// Update user
await users.put({ id: 1, name: 'Jane Doe', email: 'jane@example.com', age: 28, createdAt: Date.now() });

// Delete user
await users.delete(1);

// Count users
const count = await users.count();

// Clear all users
await users.clear();
```

## 📖 Querying

### Basic Filtering

```typescript
// Find users older than 18
const adults = await users.query({
  where: { field: 'age', operator: '>=', value: 18 }
});

// Find user by email
const user = await users.que
```
