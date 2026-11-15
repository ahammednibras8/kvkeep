# KVKeep publishing record

## Session inspection — 2026-11-15

- Inspected workspace: `/Users/ahammednibras/AhammedNibras/Projects/kvkeep`.
- This workspace is not a Git checkout. No supporting revision is available.
- Found `temp/idea.md`, which describes a proposed product and intended features. It is planning material, not implementation evidence.
- No `AGENTS.md`, `docs/STATUS.md`, or `docs/EVIDENCE.md` was found in this workspace; no ancestor `AGENTS.md` was found.
- No code, test results, benchmark artifacts, or runnable demo was found. Work in another checkout remains unverified.
- No public demo or website was verified. No publishing action is authorized.

## M001 — Obtain the build evidence handoff

- Candidate item: internal evidence handoff; no public draft yet.
- Intended audience: Ahammed and the build thread.
- Supporting evidence/revision: local `temp/idea.md` only; no repository revision available.
- Claim: KVKeep is proposed as a Zig-based context-cache component for self-hosted inference.
- Limitations: implementation stage, inference integration, attribution of reuse, performance, persistence, retention, and deployment are unverified. The available proposal does not establish that any of these exist.
- Status: idea.
- Public URL/date: none.
- Actual feedback: none supplied.
- Next action: request the build checkout location and commit SHA, with `AGENTS.md`, `docs/STATUS.md`, and `docs/EVIDENCE.md` if present. If the shared records do not exist yet, request a brief handoff stating what works at that SHA, one reproduction command and its result/artifact, and known limitations; explicitly state if there is no implementation yet.
- Publishing approval: none requested or granted.

## Feedback distinctions

- Assumptions: the proposed workflow may help developers reusing context in self-hosted inference; no audience evidence supplied.
- Actual comments/conversations: none supplied.
- Experiments: none selected; first establish the available engineering evidence.
- User decisions: communication and feedback work is separate from build ownership; no feature or roadmap decisions recorded here.

## Follow-up inspection — 2026-11-15

- Read the now-present `AGENTS.md`, `docs/STATUS.md`, and `docs/EVIDENCE.md`, plus the local build files. M001's missing-record handoff has been received locally; it is no longer the next action.
- Actual Git state: `main` exists as an unborn branch; `git log -3 --oneline` fails because there are no commits. `git status --short` lists untracked setup files and records. No supporting revision exists yet.
- `zig version` reports `0.16.0`. `build.zig` contains only a stub build function; the manifest names `kvkeep` and specifies minimum Zig `0.16.0`.
- The engineering records predate these workspace changes: they still say there is no Git repository and initialization is pending. Flag this discrepancy for the build thread; do not edit its records. No product behavior or learning completion is inferred from the setup files. No build or tests run in this marketing session.

## M002 — Introduce the Zig learning project

- Candidate item: one short X post about starting to learn Zig, with one concrete question for experienced Zig developers.
- Intended audience: Zig developers who can suggest an exercise about memory ownership.
- Supporting evidence/revision: Nibras explicitly says he is trying Zig; local setup files and Zig 0.16.0 corroborate setup activity. `temp/idea.md` supports the proposed product direction. All repository material is uncommitted; no SHA available.
- Claim: Nibras is starting to learn Zig with KVKeep as a project idea and remains at setup.
- Limitations: no inference integration, working cache, benchmark, deployment, or demonstrated mastery claimed.
- Format rationale: a short post fits an introduction and a specific learning question; current evidence does not support a launch or technical-results article.
- Venue check: reviewed X's current Rules and Authenticity policy on 2026-11-15: https://help.x.com/en/rules-and-policies/x-rules and https://help.x.com/en/rules-and-policies/authenticity . No prohibition on ordinary AI-assisted text drafts identified in those policies; spam, deceptive identities, and artificial engagement are prohibited. This draft proposes one manual post without automation or mass distribution.
- Status: published (Nibras published his own wording; verified in the review below).
- Public URL/date: https://x.com/Ahammed__Nibras/status/2121893012104167715 — 2026-11-15 at 09:08:11 UTC (14:38:11 IST).
- Actual feedback: no substantive replies verified; syndication metadata alone does not establish complete reply visibility.
- Next action: review actual technical replies if supplied; no follow-up post selected. Preserve the published wording separately from the earlier draft.

Earlier proposed draft (233 characters; not the published wording):

> I'm starting to learn Zig with KVKeep, a project idea for context caching in self-hosted inference.
>
> Still at setup: learning the language and build system.
>
> Zig developers: what small exercise helped you understand memory ownership?

### M002 — Published-item review, 2026-11-15

- Nibras supplied the public URL and requested a check. Direct web retrieval failed with `Cache miss`; exact-ID search returned no results. X's official syndication endpoint and official publish.twitter.com oEmbed endpoint both returned the same post ID, account, and text. Publication verified through those first-party responses, not inferred from the draft or URL alone.
- Actual published text:

> i've a project idea context caching on self hosted inference.
>
> i am building this on zig

- Claim audit: this presents a project idea and work in Zig without claiming a working cache, inference integration, measured speedup, deployment, or users. Current engineering records describe verified minimal-package learning and CP1 executable setup assigned but not verified. Git still has no commits; no supporting product revision exists.
- Editorial findings: “context caching for self-hosted inference” and “building it in Zig” are clearer phrasing. The post does not name KVKeep, explicitly describe the learning/setup stage, or ask a specific feedback question. These are communication limitations, not grounds to invent product progress or require another post.
- Evidence freshness: the build records now reflect initialized Git and verified CP0, superseding the earlier stale-record finding. No STATUS/EVIDENCE edits or engineering verification performed here.
- Outcomes: no verified technical replies, independent trials, reproductions, issues, collaborations, or job conversations. Do not treat engagement counters as demand evidence.
- Boundary: only PUBLISHING updated. No X edit, reply, repost, or other external write performed. The agent's earlier draft was not published by the agent.

## M003 — Explain KVKeep's problem and learning purpose in the README

- Candidate item: repository README rewrite, explicitly requested by Nibras, informed by research into engineering contract requirements accessible from India.
- Intended audience: engineers evaluating the project, potential collaborators, and potential engineering clients. The README addresses self-hosted inference operators; the market research below is editorial context, not customer feedback.
- Supporting revision: `5c01d573dc53cb6e64927cf2bf1455ea5fa1cc52` on `main`, tracking `origin/main`. Inspected committed README, build configuration, and diagnostic-only source. Current STATUS/EVIDENCE contain newer, uncommitted build-thread review notes; these were read and preserved.
- Verified stage: CP1 executable behavior is recorded as verified by the build thread; README completion and CP1 understanding remain pending in its records. No cache, inference integration, performance result, or deployed service established.
- Personal motivation: Nibras explicitly says he is building this because he needs to really understand it. The README explains that learning purpose without inventing experiences or expertise.
- Claim and limitations: early systems project exploring compatible context reuse; demonstration workflow and retention/persistence remain goals. Credits existing vLLM/LMCache capabilities. Makes no speed, safety, adoption, production, or employment promises.
- Status: awaiting approval of local README wording for inclusion in Nibras's next commit. Local editing was authorized; commit/push/publication was not.
- Public URL/date: revised README not published by this agent; no public verification of the rewritten version.
- Actual feedback: no customer conversations or independent trials supplied. Job advertisements are buyer-requirement evidence, not product validation.
- Recommended positioning: investigate and explain inference reuse with correct integration and reproducible measurements. Trade-off: tightly relevant to this project, but requires inference-stack skills beyond Zig. Credible alternative: broader platform/reliability positioning has adjacent contracts but less direct connection to a context-cache experiment. This is an editorial recommendation, not an accepted roadmap change or a claim of Nibras's current readiness.
- Next action: Nibras reviews the README's what/why and current-stage wording; build thread retains ownership of implementation, checkpoint understanding, and engineering records. No additional public item selected.

### Market research snapshot — inspected 2026-11-15

Method: purposive sample of public client listings, an employer-posted India role, and first-party contractor/platform pages. Searches covered inference deployment, performance, platform/distributed systems, and specialist evaluation, not Zig-only vacancies. This is not a representative salary survey, verified hiring count, or earnings forecast. Posted budgets are neither accepted contract rates nor take-home income; hours and continuity are unproven. USD figures are retained without speculative INR conversion or annualization.

1. **NVIDIA GPU Engineer for AI Deployment — Upwork client listing.** Advertised $18–$50/hour, worldwide, under 30 hours/week, 1–3 months. Requests Linux/NVIDIA runtime setup, model-serving API, memory/concurrency tuning, measured performance, and maintenance/recovery documentation. The indexed first-party page returned these details; direct retrieval returned HTTP 403, so live vacancy availability is unverified. Worldwide is an advertised location label, not confirmation that a particular client will engage Nibras.
   Source: https://www.upwork.com/freelance-jobs/apply/NVIDIA-GPU-Engineer-for-Deployment_~022117570887953437591/

2. **Senior ML Inference & Performance Engineer — Upwork client listing.** Advertised $30–$200/hour, worldwide, expert level, under one month. Requests measured before/after results, profiling, PyTorch/CUDA/runtime optimization, batching, load testing, observability, and operating documentation. The very broad budget is not evidence that $200/hour is paid. Indexed first-party text read; live page retrieval blocked with 403. No application or completed hire verified.
   Source: https://www.upwork.com/freelance-jobs/apply/Senior-Inference-Performance-Engineer-Model-Optimization-High-Throughput-Production-Serving_~022108461099127410044/

3. **Founding AI Platform Engineering Lead — Upwork client listing.** Advertised $100–$175/hour, worldwide, contract-to-hire, over 30 hours/week and six months. Requires eight-plus years, production ownership, incident experience, secure multi-tenancy, observability, acceptance tests, and US Eastern overlap. Indexed first-party text read; direct requests returned 403. An example of senior requirements, not a realistic beginner rate claim or verified live opening.
   Source: https://www.upwork.com/freelance-jobs/apply/Founding-Platform-Engineering-Lead-Contract-Hire_~022093064880045977246/

4. **Mercor software engineering expert network — first-party page.** The former CUDA Kernel Optimizer URL explicitly says that role is closed and displays a standing software-engineering talent network. It describes historical project rates of $70–$150/hour, expert task creation/review, production judgment, and written reasoning. It explicitly says the network is not a specific opening and matching can take months. India eligibility for a particular matching project is unverified. Do not present this as an available CUDA engineering contract.
   Source: https://work.mercor.com/jobs/list_AAABml1rkhAqAyktBB5MB4RF/cuda-kernel-optimizer-ml-engineer

5. **Flex.ai AI Inference Engineer — employer-posted Wellfound listing.** Advertises ₹40L–₹80L for a full-time, in-office Bangalore role, not contract pay. Describes runtime integration, latency/throughput profiling, KV-cache techniques, repeatable benchmarks, and serving reliability. Useful evidence of relevant skills in India, not a freelance earnings benchmark or proof of an offer.
   Source: https://wellfound.com/jobs/4901361-ai-inference-engineer

6. **India access — Upwork first-party help.** Direct-to-local-bank documentation explicitly includes India (INR). This verifies an India payment route on that platform, not eligibility for every role, current client demand, or a specific person's successful onboarding.
   Source: https://support.upwork.com/hc/en-us/articles/211063888-How-to-withdraw-earnings-with-Direct-to-Local-Bank

### Excluded or qualified leads

- A Tekvo search result described a remote-India LLM contract, but its URL now returns the generic company homepage: not counted as a verified vacancy.
- An ODS/XOR low-level optimization ad quotes $90–$125/hour but is explicitly archived; India eligibility was not established. Do not treat it as a live lead.
- AfterQuery $125/hour inference/evaluation claims appeared on third-party listings; the opened first-party careers page did not corroborate that specific contract or India access. Excluded from the rate chart and actionable opportunities.
- A principal distributed-systems listing carried a worldwide label but explicitly required US work authorization in its body. Excluded as an India-accessible lead absent separate qualifying authorization.
- The micro1 CUDA job URL returned 404 in direct retrieval. No open role or compensation claim retained from it.
- These checks reinforce that remote labels, search snippets, talent networks, and engineering-delivery contracts cannot be treated as interchangeable evidence.

### Skills and evidence implications

This is a qualitative synthesis of the sampled requirements, not a frequency ranking or accepted learning plan:

- **Measure a performance problem:** defined workload, useful baseline, repeated runs, latency distributions/TTFT, throughput, memory, errors, and quality limits. Portfolio evidence: scripts, raw results, and an explanation of where an attempted optimization failed or helped.
- **Integrate with a real system:** Python/PyTorch and a serving runtime, versioned contracts, correct KV-state compatibility, fallbacks, and attribution of reuse. A byte store or small Zig executable does not establish these capabilities.
- **Understand resource behavior:** memory lifetime, concurrency, CPU/GPU transfers, profiling, Linux debugging, and failure handling. C/C++ and CUDA/Triton appear in specialized requirements; learning Zig does not substitute for them.
- **Make work operable:** reproducible installation, load tests, logging/metrics/traces, containerization and recovery documentation. Cluster-scale roles additionally request Kubernetes/cloud/distributed-systems ownership.
- **Deliver to a client:** scoped acceptance criteria, a sanitized artifact they can inspect, clear trade-off explanations, and reliable timezone overlap. Specialist evaluation work additionally requires defensible grading and test design.
- Suggested future contract shape, not a current service offer: a scoped inference performance assessment with workload reproduction, bottleneck evidence, one evaluated change, and an operating handoff. Readiness and pricing have not been established.

### README technical sources and review

- vLLM Automatic Prefix Caching, sections Introduction and Limits: matching-prefix KV reuse reduces prefill work; it does not remove decoding work. https://docs.vllm.ai/en/latest/features/automatic_prefix_caching/
- LMCache documentation, introduction and key features: existing KV-cache storage/offloading/reuse infrastructure. No upstream performance figures copied or independently verified. https://docs.lmcache.ai/
- README uses the build thread's recorded successful commands for the unchanged source at the inspected revision. No new product test or understanding certification was performed in this marketing session.
- Only README and PUBLISHING edited by this agent. Existing STATUS/EVIDENCE changes preserved. No product code, roadmap, commits, pushes, website, accounts, or external messages changed.
- Verification: README read back; its two relative documentation links exist; code fences balanced; `git diff --check` passes. Build/source files have no diff against the inspected HEAD. Website link returned HTTP 200 via normal-TLS curl after the web tool could not access it; homepage repository/framework/deployment was not investigated or changed.
- Research visualization: four individual advertised USD/hour ranges (three indexed Upwork budgets and Mercor's historical project-rate range), explicitly qualified by source access, seniority, and eligibility limits; desktop/mobile previews checked. This is not a market-rate distribution or offered pricing.
