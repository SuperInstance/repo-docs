# consensus-protocol

**Cluster:** fleet-agent-infra  
**Language:** Rust  
**Source:** [SuperInstance/consensus-protocol](https://github.com/SuperInstance/consensus-protocol)

## Intention

See README.

## How It Works

### Vote

A `Vote` represents a single vote cast during a leader election round. Each vote records:
- `voter_id` — which node cast the vote
- `candidate_id` — who they voted for
- `term` — the election round (monotonically increasing)

In Raft, each node votes at most once per term, ensuring election safety (at most one leader per term).

### ConsensusState

`ConsensusState` holds the persistent state that must survive node restarts:
- `current_term` — the latest term the node has seen
- `voted_for` — who this node voted for in the current term (None if no vote)
- `log` — the complete replicat

## What It's For

See README.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (157 lines, 6362 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# Consensus Protocol

A Rust library implementing distributed consensus algorithms for fault-tolerant distributed systems. Provides Raft-style leader election, log replication, and commit index tracking.

## Why This Matters

In distributed systems, multiple nodes must agree on shared state despite network partitions, node failures, and message delays. Without consensus, distributed databases, coordination services (like etcd/Consul), and replicated state machines would be impossible to build correctly.

The **Raft consensus algorithm** (Ongaro & Ousterhout, 2014) decomposes consensus into three subproblems:

1. **Leader Election** — Select a leader when the current leader fails
2. **Log Replication** — The leader replicates its log to all followers
3. **Safety** — If any log entry is committed, no other entry with the same index will ever be committed

This crate provides clean, testable implementations of all three components.

## Architecture

### Vote

A `Vote` represents a single vote cast during a leader election round. Each vote records:
- `voter_id` — which node cast the vote
- `candidate_id` — who they voted for
- `term` — the election round (monotonically increasing)

In Raft, each node votes at most once per term, ensuring election safety (at most one leader per term).

### ConsensusState

`ConsensusState` holds the persistent state that must survive node restarts:
- `current_term` — the latest term the node has seen
- `voted_for` — who this node voted for in the current term (None if no vote)
- `log` — the complete replicated log

### RaftLeaderElection

`RaftLeaderElection` manages timeout-based leader election with randomized timeouts to prevent split votes. When a follower doesn't hear from a leader within the election timeout, it:

1. Increments its term
2. Transitions to candidate
3. Votes for itself
4. Requests votes from all peers

A candidate wins when it receives votes from a strict majority of the cluster.

### LogReplication

`LogReplication` manages the append-only log that is replicated from leader to followers. The leader tracks:
- `next_index` — the next log index to send to each follower
- `match_index` — the highest index known to be replicated on each follower

Followers validate log consistency by checking that the term at `prev_log_index` matches `prev_log_term`.

### CommitIndex

`CommitIndex` tracks which entries are safely committed (replicated on a majority). An entry is committed when the leader determines that a majority of nodes have stored it. Committed entries are never lost and can be safely applied to the state machine.

## Usage

```rust
use consensus_protocol::{Vote, ConsensusState, RaftLeaderElection, LogReplication, CommitIndex};

// Set up a 3-node cluster
let mut state = ConsensusState::new("node-1");
let mut election = RaftLeaderElection::new("node-1", 150); // 150ms timeout
election.add_peer("node-2");
election.add_peer("node-3");

// Start an election
let vote_request = election.start_election(&
```
