# Usage

This repository has one main artifact: [`rankelo_ef_coding_session.md`](./rankelo_ef_coding_session.md), a real Claude Code session from Rankelo's development history. This page explains how to read it and exactly what rules were followed while preparing it for publication.

## How to read it

The file is organized into two parts:

1. **A short context section at the top.** It states the project, the tools involved, the session date, why this particular session was chosen, what the underlying engineering problem was, and a plain, factual summary of what happened: the starting test count, what was built, what failed, what changed as a result of that failure, and the final test count.
2. **`# Original Coding Agent Session`.** The transcript itself, starting immediately after that heading.

Read the context section first. It tells you what to look for once you reach the transcript, in particular, two points where a failing test exposed a real design mistake and the design was changed because of it, and one point where the project's own automated secret scanner caught a mistake in the agent's own test code.

## Ground rules followed while preparing this transcript

- Every line under `# Original Coding Agent Session` is copied from a real, local Claude Code session log. Nothing was invented, reordered, or rewritten to make the session read better than it actually went.
- The original prompts are reproduced exactly as written, including their full length and any repetition in them.
- Failed attempts, test failures, and corrections are left in on purpose. Nothing was cut just to make the session look cleaner than it was.
- Two things are condensed for length, and both are clearly marked inline at the point where it happens. First, most of the sections of one very large opening brief that describe product features that were not actually built in this pass. Second, tool outputs and file contents that ran past roughly 3,500 characters. Every cut is marked with an explicit note; nothing is silently shortened.
- Secrets and credential-shaped strings, including API keys, passwords, and tokens, were replaced with `[REDACTED]` before publication. This includes at least one real, no-longer-valid development credential and one local-only database password that carried no real risk. Development credentials are redacted on the same principle as any other credential, regardless of whether they still work.
- Product decisions made by the human are attributed to the human, and decisions made by the agent are attributed to the agent. Neither is credited with the other's contribution.

## What this repository is not

- It is not a tutorial or a reusable code sample. The code shown in the transcript is real Rankelo source at one specific point in time, kept here for historical accuracy rather than maintained or supported.
- It is not evidence that Rankelo depends on Claude Code, Codex, or any single AI provider to run. See the "Development tools versus product runtime" section of the [README](./README.md) for how that separation actually works in the product.
