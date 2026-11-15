# KVKeep status

Updated: 2026-11-15. Repository files and verified commands take precedence over thread memory.

## Environment

- Workspace: `/Users/ahammednibras/AhammedNibras/Projects/kvkeep`.
- Current branch `main`, tracking `origin/main`; user-created commit `5c01d573dc53cb6e64927cf2bf1455ea5fa1cc52` (`setup: project first stepup to github`). Tree was clean before this review's record updates. Origin: https://github.com/ahammednibras8/kvkeep.git.
- macOS 26.5.1 ARM64; local clock IST (+05:30), consistent with Asia/Kolkata.
- Zig 0.16.0 (`/opt/homebrew/bin/zig`); Git 2.55.0; Codex CLI 0.166.0; T3 Code Beta and server 0.1.6.
- Last verified runtime: gpt-6.1-sol, high reasoning effort, full-access; harness sandbox disabled, approvals `never`, network enabled. No permission settings changed. Recommend restricted access with supervised approvals; installed T3 UI controls remain unverified.
- No scheduled tasks in this project at initial audit. Scheduler tools support thread binding but expose no explicit timezone/model/permission controls. Recurrence unapproved and not enabled; manual `review` available.

## Current checkpoint: CP2 — run a prefix-matching learning experiment through Zig tests

- Status: CP2 assigned after explicit `next`; implementation and understanding pending. CP0 and CP1 remain verified within their scope. No inference capability established.
- User approved starting setup after the initial audit and requested GitHub project research before implementation guidance.
- Agent created only AGENTS.md, STATUS.md, and EVIDENCE.md; marketing owns existing PUBLISHING.md. Product proposal remains `temp/idea.md`.
- User attempt inspected: build defines kvkeep executable from `src/main.zig`, native target, install action, run action, named run step, and dependency connecting them. `main` prints the expected development diagnostic. Format, build, direct execution, and named run all exit 0.
- Understanding demonstrated: Nibras explained that `zig build run` cannot launch an application because no named `run` step is defined, comparing it to a missing package.json script. An empty default build can succeed without defining an application.
- `.gitignore` now ignores `temp/`, `.zig-cache/`, and `zig-out/`; `git check-ignore .zig-cache/ zig-out/` confirmed both generated directories are ignored.
- CP1 understanding demonstrated after explanation: Nibras correctly identified exe as describing compilation and run_exe as describing execution; previously identified run_step as the named command. Explained that dependOn connects the named command to the execution action. Isolated disconnected-step experiment remains supporting evidence; independent transfer of this concept to a new build task has not yet been tested.
- CP2 task: Nibras writes two meaningful tests in proposed `tests/prefix_experiment.zig`, using std.mem.startsWith on byte strings: matching document prefix succeeds, changing the document makes the match false. Wire a native test compilation with b.addTest, its execution with b.addRunArtifact, and a named test step depending on the execution action. This is a test-runner and exact-byte-prefix learning experiment, not a cache implementation or an inference compatibility contract.
- CP2 acceptance: direct `zig test tests/prefix_experiment.zig` and `zig build test --summary all` run both tests; temporarily invert one assertion to observe nonzero failure, then restore correct expectations and pass both commands. Format check passes. Nibras writes the tests; agent may extend repetitive tests only after review.
- README reviewed and accepted in its current form at Nibras's direction: describes setup-only status, explicitly unimplemented cache/inference behavior, Zig 0.16.0, diagnostic stderr output, and previously verified build/run/format commands. No further documentation expansion requested. README changes are uncommitted; agent did not edit it.
- Remaining setup issues: restricted permission configuration not verified. No inference integration, cache feature, benchmark, or production-readiness evidence exists.
- GitHub setup verified through `gh repo view`: user-created https://github.com/ahammednibras8/kvkeep is PUBLIC, default branch main. Agent performed read-only inspection; no creation, commit, push, or visibility change. Commits remain Nibras's responsibility.

## Decisions and assumptions

- Accepted: Nibras writes the product; agent teaches, reviews, and maintains evidence. One checkpoint at a time. Preserve marketing records.
- User proceeded with installed Zig 0.16.0 and the minimal native Zig build setup. No exact compiler-version enforcement exists; generated minimum-version metadata is not an exact compiler pin.
- Research references: TigerBeetle for explicit compiler compatibility; Ghostty for clear build/test commands; ZML for runnable AI examples. These are references, not adopted dependencies or a ranking of every Zig project.
- AI learning targets: KV cache versus answers; prefill versus decoding; compatible reuse; Zig memory ownership and cleanup; integration boundaries; measured attribution against a useful baseline. None certified as learned yet.
- LMCache/vLLM remains a candidate, not a decision; no integration versions or connector contracts verified. Real inference must eventually traverse our component.
- Next action: Nibras attempts CP2 and replies `done` with the prediction answer and observed failure/pass results. No automatic advancement. Restricted permission setup remains unresolved.
