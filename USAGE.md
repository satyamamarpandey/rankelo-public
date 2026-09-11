# Usage

This repository has one main artifact: [`rankelo_ef_coding_session.md`](./rankelo_ef_coding_session.md).

## How to read it

The file has two parts:

1. **A short context section at the top** — project, tools, session date, why this session was picked, what the underlying problem was, and a factual (non-exaggerated) summary of what happened: starting test count, what was built, what failed, what changed as a result, and the final test count.
2. **`# Original Coding Agent Session`** — the transcript itself.

Read the context section first; it tells you what to look for in the transcript (in particular, the two points where a test failure exposed a real design mistake and the design was changed because of it, and the point where the project's own secret scanner caught a mistake in the agent's own test code).

## Ground rules that were followed producing this transcript

- Every line under `# Original Coding Agent Session` is copied from a real, local Claude Code session log. Nothing was invented, reordered, or rewritten to make it read better.
- The original prompts are reproduced exactly as written, including their length and repetition.
- Failed attempts, test failures, and corrections are left in. Nothing was cut just to make the session look cleaner.
- Two things are condensed for length, and both are marked inline where it happens: (1) most of the sections of one very large opening brief that describe product features that were *not* built in this pass, and (2) tool outputs and file contents that ran past roughly 3,500 characters. Both cuts are marked with an explicit note — nothing is silently shortened.
- Secrets and credential-shaped strings (API keys, passwords, tokens) were replaced with `[REDACTED]` before publishing, including at least one that was a real, no-longer-valid development credential and one that was a local-only database password with no real risk. Development credentials are redacted the same as any other credential, on principle, not based on whether they still work.
- The agent's own product decisions are shown as the agent's, and the product direction/constraints set by the human are shown as the human's. Neither is attributed to the other.

## What this is not

- It is not a tutorial or a reusable code sample. The code shown is real Rankelo source at a specific point in time, kept for historical accuracy, not maintained or supported here.
- It is not evidence that Rankelo depends on Claude Code, Codex, or any single AI provider to run. See the "Development tools vs. product runtime" section of the [README](./README.md).
