# corex

Self-hosted AI + cloud platform, built from scratch. Merger of two previously separate projects, kept as top-level folders:

- **[attnx](./attnx)** — AI platform: GPU kernels, pretraining, distributed training, post-training/RL, serving, RAG, agents, evals, MLOps, interpretability, multimodal.
- **[basisx](./basisx)** — Cloud platform: storage, messaging, compute, networking, observability, dev tooling, control plane.
- **[agentx](./agentx)** — Agent framework built by hand with LangChain/LangGraph/LangSmith (livestreamed). Follow-up **agentz** will rebuild it on attnx/basisx primitives to benchmark against.

Monorepo, one folder per service, language split by layer (Rust for storage/perf, Go for concurrency/networking/orchestration, Python for ML glue, TypeScript for tooling). Deploys to a repurposed MacBook running Linux as a persistent VM, reachable via Cloudflare Tunnel or Tailscale Funnel. Built to production quality, not a learning exercise.
