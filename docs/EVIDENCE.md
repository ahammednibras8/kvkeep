# KVKeep evidence

## CP0 — setup and repository research, 2026-11-15

- Revision: unavailable; workspace is not a Git repository. All local work is uncommitted.
- Existing material: `temp/idea.md` (proposal), then `docs/PUBLISHING.md` from the marketing thread. Neither establishes working software. PUBLISHING's initial absence report describes its earlier inspection; new shared records supersede that snapshot.
- `pwd`, `ls -la`, `rg --files --hidden`: confirmed workspace and existing files. No product source/build/tests at inspection.
- `git status --short --branch`, branch/remote/log commands: failed because no Git repository exists. This is not a clean-tree result.
- `zig version`: 0.16.0; `zig env`: Homebrew installation, aarch64-macos target. `git --version`: 2.55.0; `codex --version`: 0.166.0.
- T3 environment/thread read: server 0.1.6, macOS ARM64; model gpt-6.1-sol/high; runtime full-access. App plist: T3 Code Beta 0.1.6. Python local clock: IST/+0530.
- T3 `list_scheduled_tasks`: empty list for this project. Read scheduler schemas; no creation, dry run, or recurrence performed. Safe execution environment and scheduler timezone are unverified.
- `zig init --help`: verified `--minimal` support in installed compiler.
- Isolated temporary-directory experiment: `zig init --minimal` exited 0, generating only `build.zig` and `build.zig.zon`. Build function is a stub; manifest reports minimum Zig 0.16.0. Generated files were inspected and temporary directory removed. This was not run in the product workspace and is not a KVKeep feature.
- Separate isolated validation: initialized the same minimal template, then `zig build --summary all` exited 0 with `Build Summary: 1/1 steps succeeded`, `install cached`; no `zig-out` directory was produced. Temporary project removed; compiler global cache may retain generated build-runner artifacts. This proves only that an empty build can succeed.

## GitHub source inspection

Selected established Zig projects for relevant practices, not an exhaustive popularity ranking. GitHub API resolved these snapshots; source files were opened at their exact revisions:

- [TigerBeetle build.zig](https://github.com/tigerbeetle/tigerbeetle/blob/a2a3c7064519e08233abe26c54a43fca2f9ad9bc/build.zig#L49): checks compiler major/minor/patch against 0.16.0 and reports unsupported versions at compile time.
- [Ghostty HACKING.md](https://github.com/ghostty-org/ghostty/blob/6d9577708a211b0e6c5e6c6886f3cfb7efc47555/HACKING.md): documents debug build, run/test steps, and platform dependencies.
- [ZML README](https://github.com/zml/zml/blob/8fcff8c462070d06056f8a85ba0c8a81f0f3a636/README.md#30-second-smoke-test): Bazel prerequisites, real-model smoke test/LLM examples, test command. Examples were read, not executed; upstream performance claims were not independently tested.
- First Python HTTPS retrieval failed certificate validation. System curl with normal TLS verification and web retrieval succeeded. No TLS checks disabled.

## Current limits

- Workspace empty build and central understanding: verified in the follow-ups below. Application tests: not run; no application source or tests exist.
- Real-model inference, cache contribution, performance, retention, persistence, restart recovery, and production readiness: unproven.
- No model downloads, GPU/cloud spending, services, commits, pushes, publication, or settings changes performed.
- Agent changes are mentoring records only. Readback checks verify file access; automatic instruction reload is not assumed.

## CP0 — user attempt review, 2026-11-15

- Current revision: none; `git status --short --branch` reports no commits yet on `main`. `git remote -v` returns no remotes; `git log -1 --oneline` fails because there are no commits. Git was initialized after the initial audit.
- `git diff --stat` and path-specific diff are empty because setup files remain untracked; reviewed their actual contents instead. This is not a clean-tree result.
- `build.zig`: valid empty build function, discards `b`; no application compilation, installation, or run step. `build.zig.zon`: kvkeep 0.0.1, minimum Zig 0.16.0, generated fingerprint, package paths includes root. No dependencies declared.
- `zig version`: 0.16.0. `zig fmt --check build.zig build.zig.zon`: exit 0. `zig build --summary all`: exit 0, `Build Summary: 1/1 steps succeeded`, `install cached`. No application executable established. No test suite exists to run.
- `.gitignore` contains only `temp/`; `.zig-cache/` is reported untracked. User correction requested: ignore `.zig-cache/` and `zig-out/` before staging. No ignore or build files edited by the agent.
- Nibras explained that `_ = b` is valid code so the build can execute. Distinction between running the build script and producing an application was explained; follow-up understanding question remains unanswered. Checkpoint not yet verified.
- Only STATUS and EVIDENCE updated by the agent. Marketing record preserved. No automatic checkpoint advancement, commits, or publishing.

## CP0 — understanding and ignore correction verified, 2026-11-15

- Nibras correctly explained that no application can be launched through `zig build run` because the build defines no named `run` step, using a missing package.json script as an analogy. Central checkpoint understanding demonstrated.
- Inspected unchanged empty `build.zig` and user-updated `.gitignore`. Ignore entries now include `temp/`, `.zig-cache/`, and `zig-out/`.
- `git check-ignore .zig-cache/ zig-out/`: exit 0, output lists both directories. `git status --short --branch`: no commits on main, setup files untracked; `.zig-cache/` no longer appears. `zig version`: 0.16.0.
- Build and format checks were not repeated: previous successful checks still apply to the unchanged build files. No product tests exist. `zig build run` was discussed, not executed.
- CP0 minimal-package experiment verified; restricted permissions and committed baseline remain unresolved setup work. No AI inference or product capability established. Agent updated records only and awaits explicit `next`.

## CP1 — assignment and GitHub preparation, 2026-11-15

- User explicitly requested the next checkpoint, basic project structure/tooling, and GitHub setup for a portfolio. Repository remains on main without commits or remotes. Build stub unchanged; source directory and README not yet present.
- `gh --version`: 2.102.0. `gh api user --jq .login`: exit 0, authenticated account `ahammednibras8`. `gh repo view ahammednibras8/kvkeep --json nameWithOwner,url,visibility,defaultBranchRef`: fails to resolve that repository; does not establish global name availability or absence of inaccessible repositories.
- Read installed `gh repo create --help`: verified source/remote/public/private options and that `--push` is a separate flag. No creation or push executed; exact destination/visibility pending user confirmation and local baseline review.
- Read installed Zig 0.16.0 init template and std.Build APIs for createModule, addExecutable, installArtifact, addRunArtifact, step, dependOn; inspected std.debug.print, which writes diagnostic output to stderr and ignores output errors. Opened official build guide sections Simple Executable and Adding a Convenience Step for Running the Application. Guide is unversioned; selected APIs checked against installed 0.16.0 sources.
- Assigned a development executable and short README; no product code or build configuration edited by the agent. User code, build/run commands, and understanding have not been verified for CP1. This remains setup, with no AI inference claim.
- Marketing follow-up's report of stale engineering records refers to its inspection snapshot; current engineering records now reflect initialized Git and verified CP0. PUBLISHING preserved.
