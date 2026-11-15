# KVKeep

An early systems project exploring context-cache reuse for self-hosted AI inference, written in Zig.

KVKeep is for investigating a practical question: **when does keeping reusable model context outside an inference worker help enough to justify the storage, data movement, and operational complexity?**

**Current stage:** development setup only. The executable prints `KVKeep development build`. No context cache or inference integration is implemented, and there are no performance results yet.

## The problem

An application can ask different questions about the same long document or conversation history. When requests share a matching prompt prefix, reusing compatible key/value (KV) cache state can avoid repeating some prompt processing, called prefill. The model still generates a fresh answer. This does not remove the work of generating new tokens.

This capability already exists in the ecosystem: [vLLM provides automatic prefix caching](https://docs.vllm.ai/en/latest/features/automatic_prefix_caching/), and [LMCache provides KV-cache storage and reuse infrastructure](https://docs.lmcache.ai/). Those are the starting points for understanding the problem and evaluating whether KVKeep contributes anything useful.

The intended audience is developers who control their inference deployment and want to understand where context reuse happens, what it costs, and whether it helps their workload.

## Why I am building this

I’m Ahammed Nibras, a software developer in India learning Zig. I’m building KVKeep because I want to understand these systems by implementing, inspecting, and measuring their behavior.

The questions I want to work through connect model inference to memory ownership, storage, integration boundaries, and performance measurement. Choosing Zig gives me a language to learn while doing that work. The engineering evidence will come from correct behavior, reproducible experiments, and explanations of the trade-offs.

## What I want to demonstrate

The proposed workflow is:

1. Ask a real model a question about supplied context.
2. Ask a different question with the same compatible context.
3. Trace whether the model reused context through KVKeep, through its existing engine cache, or not at all.
4. Compare the same workload against the existing serving setup, with its normal caching enabled.

These are goals, not available features. A useful result must also report overhead, misses, errors, and workloads where reuse does not help. Retention controls, storage budgets, and restart persistence remain proposed extensions.

## Run the current development executable

The setup has been verified locally with **Zig 0.16.0**.

```sh
zig version
zig build --summary all
zig build run --summary all
```

The run command writes this diagnostic to stderr:

```text
KVKeep development build
```

Check formatting with:

```sh
zig fmt --check build.zig build.zig.zon src/main.zig
```

This runs the development executable; there is no model download, cache service, or interactive AI demo.

## Evidence and feedback

[Project status](docs/STATUS.md) and [engineering evidence](docs/EVIDENCE.md) record what has been verified and what remains unproven.

**Feedback question:** if you operate self-hosted inference, in what workload does your existing context cache fall short, and how do you observe that failure?

Built by [Ahammed Nibras](https://ahammednibras.com).
