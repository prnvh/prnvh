# Pranav Harikumar
### Independent AI systems researcher and builder focused on reliability.
I build AI systems focused on making LLMs usable in reliable real-world workflows. Familiar with governed memory, deterministic workflows and architectures that constrain LLM behavior through validation, typed state, and explicit execution paths.

18 · Bengaluru, India
LinkedIn pranavharikumar2008@gmail.com

## What I'm working on
I’m interested in making LLM systems more reliable in deployment — not by prompting them harder, but by placing them inside architectures that constrain writes, validate actions, and fail in explicit ways.

## Projects

### PlanCompiler
A deterministic compilation architecture for structured LLM workflows.
- Typed node registry and static validation
- LLM plans workflows; deterministic code generation handles execution
- Benchmarked on 300 tasks against direct-generation baselines

### Governed Memory Layer
A governed, event-driven shared memory architecture for LLM agents.
- Shared state is updated through a promotion pipeline rather than direct free-form writes
- Interpreter evaluates one note at a time with current context
- Writes are validated, logged to an append-only ledger, and projected into canonical state
- Includes benchmark families for lifecycle updates, identity resolution, overrides, coherence, and replay robustness

### SVMP-CS
A governance layer for session-based LLM customer support.
- Soft debounce for message consolidation
- Multi-tenant isolation
- Similarity-based escalation
- Verified non-LLM routing for transactional paths


## Areas of interest
LLM reliability, governed memory, deterministic execution, stateful systems, agent infrastructure.
