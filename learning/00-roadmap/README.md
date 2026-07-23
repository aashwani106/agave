# Course Roadmap

This is an ordering map, not an architecture lesson. Topic names beyond the current lesson are deliberately short so they do not front-load concepts.

This roadmap is dependency-aware but not a fixed release schedule. The external-learning gate in [../COURSE-RULES.md](../COURSE-RULES.md) controls what can be studied next.

## Current position

```text
Agave validator
├── Process entry and command dispatch ✅ ← YOU ARE HERE (STOPPED)
├── Validator initialization
├── Networking
├── TPU
│   ├── Fetch
│   ├── SigVerify
│   └── Banking
│       ├── Scheduler          external study: current
│       ├── Account Locks      external study: current
│       ├── Sealevel           external study: current
│       └── SVM                external study: next
├── Broadcast                  external study: next
├── TVU                        external study: next
└── Consensus                  external study: next
```

## Phase A — Learn to read the process

1. **Introduction:** the validator executable and its process boundary
2. **Rust while reading:** syntax is embedded just in time in whichever approved implementation lesson comes next
3. **Validator startup:** configuration, ledger locking, bootstrap, and service construction

## Phase B — Follow data into and through a validator

4. Network foundations and packet representation
5. Gossip and cluster membership
6. TPU overview, followed by separate lessons for Fetch and SigVerify
7. Banking Stage and scheduling
8. SVM execution and the account-locking model
9. Accounts, Bank, AccountsDB, and persistence

## Phase C — Follow replicated history

10. PoH and entries
11. Shreds, Turbine, and TVU ingress
12. Blockstore and repair
13. Replay Stage and fork choice
14. Voting, Tower BFT, commitment, and finality

## Phase D — Operate and contribute

15. RPC, subscriptions, snapshots, and restart
16. Cost model, fees, QoS, and local fee markets
17. Tests, benchmarks, metrics, failure diagnosis, and contributor workflow
18. Advanced/evolving designs: Jito integration boundaries, Alpenglow/Votor, Rotor, and Firedancer comparisons

Each numbered subject may become several lessons. We will split a subject whenever one lesson would require holding too many new ideas at once.
