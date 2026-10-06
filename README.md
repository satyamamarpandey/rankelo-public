# Rankelo · Public

[![License: MIT](https://img.shields.io/badge/license-MIT-2ea44f.svg)](./LICENSE.md)
[![Lint Markdown](https://github.com/satyamamarpandey/rankelo-public/actions/workflows/lint.yml/badge.svg)](./.github/workflows/lint.yml)

A small, public companion repository for [Rankelo](https://rankelo.brandsap.com/), a product by [Brandsap](https://brandsap.com/), created by [Satyam Pandey](https://pandeysatyam.com/). It exists to share one genuine coding-agent session for an [Entrepreneurs First](https://www.joinef.com/) application, along with the standard project files that make a repository easy to trust and easy to use.

**This repository does not contain Rankelo's product source code.** Rankelo itself is closed-source, commercial software. What you'll find here is a real development artifact, an unedited transcript of a coding-agent session, plus documentation that explains exactly how it was produced.

## At a glance

| File | What it is |
|---|---|
| [`rankelo_ef_coding_session.md`](./rankelo_ef_coding_session.md) | An authentic, redacted transcript of a real Claude Code session. In it, the agent builds part of Rankelo's agent-safety layer: the "Guardian" policy engine, a permission-scoped tool registry, and defenses against prompt injection from untrusted web content. Nothing in the transcript is invented or rewritten. [`USAGE.md`](./USAGE.md) explains exactly how it was produced and what, if anything, was redacted. |
| [`USAGE.md`](./USAGE.md) | How to read the session transcript, and the ground rules that were followed while preparing it for publication. |
| [`PRIVACY_POLICY.md`](./PRIVACY_POLICY.md) | A privacy notice scoped to this repository, plus a link to Rankelo's actual product privacy policy. |
| [`LICENSE.md`](./LICENSE.md) | The MIT license, covering the original written content in this repository. See the License section below for what it does and doesn't cover. |
| [`.github/workflows/lint.yml`](./.github/workflows/lint.yml) | A small CI workflow that lints every Markdown file in this repository on each push and pull request, so formatting stays clean over time. |

## Why this repository exists

Coding-agent sessions are usually private: they live in a local transcript file and are rarely seen by anyone outside the person who ran them. For an Entrepreneurs First application asking to see how I actually work with AI coding tools, the honest answer needed a real example rather than a polished summary. This repository is that example, published as-is, warts included.

## Development tools versus product runtime

Rankelo is built with the help of several AI coding agents, mainly Claude Code and Codex, chosen depending on the task at hand. These are development tools. They help write, review, test, and debug the product, but they are not part of how Rankelo runs in production.

Rankelo itself is architected to be provider-agnostic, so that no single AI vendor is a hard dependency:

- The default LLM route is [OpenRouter](https://openrouter.ai), using a free-tier model.
- OpenAI, Anthropic, and Gemini are supported only as optional adapters. Each one is gated behind an explicit provider-mode switch and a daily spend cap that defaults to zero, so a paid provider can never be called by accident.
- Razorpay is the one intentional commercial dependency in the stack, and its role is scoped strictly to billing.

Because of this design, switching or removing a development coding agent, or swapping a paid model provider for a different one, never requires rebuilding the product around it.

## License

The prose written specifically for this repository (this README, `USAGE.md`, and `PRIVACY_POLICY.md`) is released under the [MIT License](./LICENSE.md), so anyone is free to reuse the wording, structure, or approach. The session transcript is a historical record of real development work on Rankelo, shared for transparency rather than as a reusable code sample. See `USAGE.md` for the full authenticity and redaction rules that were applied to it before publication.

## Contact

Brandsap, [contact@brandsap.com](mailto:contact@brandsap.com), Nagpur, Maharashtra, India.

## Author

Built by [Satyam Pandey](https://pandeysatyam.com/), founder of [Brandsap](https://brandsap.com/). Read the [Rankelo case study](https://pandeysatyam.com/projects/rankelo.html).
