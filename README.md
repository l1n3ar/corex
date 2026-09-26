# corex

Self-hosted AI and cloud platform, built from scratch.

## Structure

- **[attnx](./attnx)**: AI platform. GPU kernels, pretraining, distributed training, post-training/RL, serving, RAG, agents, evals, MLOps, interpretability, multimodal.
- **[basisx](./basisx)**: Cloud platform. Storage, messaging, compute, networking, observability, dev tooling, control plane.
- **[agentx](./agentx)**: Planned agent framework, to be built natively on attnx/basisx primitives.
- **[agentz](./agentz)**: Agent framework in progress, built with LangChain, LangGraph, and LangSmith. Will be benchmarked against agentx once both exist.

## Stack

Monorepo, one folder per service. Language split by layer:

- Rust for storage and performance-critical services
- Go for concurrency, networking, and orchestration
- Python for ML glue
- TypeScript for tooling

## Deployment

Runs on a repurposed MacBook running Linux as a persistent VM, reachable via Cloudflare Tunnel or Tailscale Funnel.
