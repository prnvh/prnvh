# Pranav Harikumar

**Building reliability layers for AI systems - constraints, gates, and deterministic pipelines.**

18 · Bengaluru, India · [LinkedIn](https://linkedin.com/in/pranav-h2/) · pranavharikumar2008@gmail.com

---

## What I Build

AI systems break in deployment for a specific reason: generation is treated as the end point rather than a component inside a larger architecture that should constrain and verify it. I'm focused on the layer between the model and the real world — deterministic pipelines, explicit validation gates, and systems that fail predictably rather than hallucinate silently.
Both of my projects are different implementations of the same idea applied in different domains.

---

## Projects

### [SVMP – Multi-Tenant LLM Governance Layer](https://github.com/svmp-systems/SVMP-Systems)

A session-based orchestration layer for LLM-driven customer service. Instead of letting the model answer freely, SVMP routes every query through a typed pipeline.

- **Soft Debounce** - 2.5s sliding window aggregates fragmented messages into Complete Thought Units before any AI logic runs. Reduces LLM API overhead by 40–60%
- **Multi-Tenant Identity Frame** - 3-dimensional coordinate system (tenantId · clientId · userId) hard-silos every interaction at the database level. No prompt engineering — enforced at the DB layer
- **MUTEX Locking** - Atomic state lock prevents race conditions and guarantees exactly-once processing
- **Similarity Gate (≥0.75)** - If confidence is below threshold, the system freezes and escalates to a human agent rather than hallucinating
- **Intent Logic Fork** - Transactional queries (order tracking, cancellations) bypass the LLM entirely and hit verified APIs directly. Eliminates transactional hallucination
- P90 internal latency **< 5s** post-debounce · 500+ adversarial red-team tests completed

---

### [LLM Code Graph Compiler](https://github.com/prnvh/llm-code-graph-compiler)

A CLI tool that converts natural language tasks into deterministic, runnable Python programs. The LLM never generates executable logic — it only selects and wires components that already exist.

- **Typed Node Registry** - 23 nodes across data ingestion, transformation, storage, querying, and serving. Every edge is only legal if output type of node A matches input type of node B
- **Structured Planner** - LLM returns a JSON graph spec (nodes, edges, params). Plan normalizer handles format inconsistencies before validation
- **Deterministic Validator** - 5-check pipeline: node existence · type compatibility · DAG integrity via Kahn's algorithm · orphan detection · required parameter enforcement. Aborts with explicit errors before a single line emits

---

## Other Work

**Student Marketing Venture** - Scaled from $0 to $4,000 revenue in 3 months. Managed execution team, delivered 20+ client projects.

**Labor Market Research (Independent)** - 150+ structured interviews across Kerala. Identified wage asymmetry patterns between migrant and local workers. Drafting research paper.

---

## Stack

`Python` `JavaScript` `SQL` `MongoDB` `Pydantic` `Multi-tenant architectures` `Deterministic validation` `Constrained LLM planning`

---

*Graduating high school April 2026. Feel free to reach out for any enquiries.*
