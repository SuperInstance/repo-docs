# commodore-protocol

**Cluster:** maritime  
**Language:** Python  
**Source:** [SuperInstance/commodore-protocol](https://github.com/SuperInstance/commodore-protocol)

## Intention

Multi-DeckBoss coordination — auto-discovery, election, work distribution, failover

## How It Works

[code]

**Communication flow:**

[code]

## What It's For

Multi-DeckBoss coordination — auto-discovery, election, work distribution, failover

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (464 lines, 17231 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# Commodore Protocol

> Decentralized coordination for Multi-DeckBoss instances.

[![Build Status](https://img.shields.io/github/actions/workflow/status/SuperInstance/commodore-protocol/build.yml?branch=main)](https://github.com/SuperInstance/commodore-protocol/actions)
[![License](https://img.shields.io/github/license/SuperInstance/commodore-protocol)](https://github.com/SuperInstance/commodore-protocol/blob/main/LICENSE)
[![Fleet Status](https://img.shields.io/badge/fleet-status-online-green)](https://github.com/SuperInstance/commodore-protocol)
[![Cocapn Fleet](https://img.shields.io/badge/cocapn-fleet-member-blue)](https://github.com/cocapn)

The Commodore Protocol is the brain that keeps multiple DeckBoss units working together on a single vessel. It handles **auto-discovery**, **leader election**, **deference**, **work distribution**, and **automatic failover** — so whether you're running one unit or a dozen, the fleet always has exactly one commodore calling the shots.

---

## Overview

When multiple DeckBoss instances operate on the same vessel, they need a way to agree on who is in charge, distribute computational work, and recover if the leader goes down. The Commodore Protocol solves this as a fully decentralized, peer-to-peer coordination layer:

- **Auto-discovery** — DeckBoss units find each other on the local network via mDNS
- **Election** — A priority-based algorithm selects the most qualified unit as Commodore
- **Deference** — All other units defer compute and decisions to the Commodore
- **Work distribution** — The Commodore assigns tasks based on each unit's capabilities and current load
- **Failover** — If the Commodore dies, the next-best unit promotes automatically

The human only ever talks to one unit. The rest work silently in the background.

---

## Problem Statement

Running multiple autonomous DeckBoss units on the same vessel without a coordination layer creates a set of hard, cascading failures:

| Problem | Without Coordination | With Commodore Protocol |
|---|---|---|
| **Split brain** | Multiple units try to make conflicting decisions | Exactly one Commodore at all times |
| **Wasted resources** | All units duplicate the same compute work | Tasks distributed by capability and load |
| **No failover** | Leader crash = total system failure | Automatic promotion within heartbeat timeout |
| **Discovery** | Manual configuration of every unit's peers | mDNS auto-discovery on the local network |
| **Scaling** | No visibility into when to add hardware | Load monitoring triggers scale-up suggestions |
| **Capability gaps** | No way to know which unit handles what | Central capability registry with routing |

Without coordination, adding a second DeckBoss unit can actually make things *worse* — not better. The Commodore Protocol turns additional units into genuine force multipliers.

---

## Architecture

```
                          ┌──────────────────────────────────┐
                          │          Cocapn Flee
```
