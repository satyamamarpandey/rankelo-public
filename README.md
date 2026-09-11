# Rankelo — Public

This is a small, public companion repository for [Rankelo](https://rankelo.brandsap.com), a product by [Brandsap](https://brandsap.com). It exists to share a real coding-agent session for an [Entrepreneurs First](https://www.joinef.com/) application, along with a few standard project files.

**This repository does not contain Rankelo's product source code.** Rankelo is closed-source, commercial software. What's here is a genuine development artifact (an unedited coding-agent session transcript) plus documentation about how it was produced.

## What's in this repo

| File | What it is |
|---|---|
| [`rankelo_ef_coding_session.md`](./rankelo_ef_coding_session.md) | An authentic, redacted transcript of a real Claude Code session that built part of Rankelo's agent-safety layer (the "Guardian" policy engine, permission-scoped tool registry, and prompt-injection defenses). Nothing in it is invented or rewritten — see [USAGE.md](./USAGE.md) for how it was produced and what was redacted. |
| [`USAGE.md`](./USAGE.md) | How to read the session transcript, and the ground rules that were followed when producing it. |
| [`PRIVACY_POLICY.md`](./PRIVACY_POLICY.md) | Privacy notice for this repository, plus a link to Rankelo's actual product privacy policy. |
| [`LICENSE.md`](./LICENSE.md) | MIT license covering the original written content in this repository (the transcript's underlying code snippets remain part of Rankelo and are not separately licensed for reuse — see the License section below). |
| [`.github/workflows/lint.yml`](./.github/workflows/lint.yml) | A basic CI workflow that lints the Markdown in this repo on every push and pull request. |

## Development tools vs. product runtime

Rankelo is built using multiple AI coding agents — primarily Claude Code and Codex, depending on the task. These are **development tools**: they help write, review, test, and debug the product. They are not part of Rankelo's runtime.

Rankelo itself is architected to be provider-agnostic:

- The default LLM route is [OpenRouter](https://openrouter.ai), using a free-tier model.
- OpenAI, Anthropic, and Gemini are supported as optional adapters, each gated behind an explicit provider-mode switch and a daily spend cap that defaults to `$0`.
- Razorpay is the one intentional commercial dependency, scoped strictly to billing.

Switching or removing a development coding agent, or a paid model provider, does not require rebuilding the product.

## License

The prose written specifically for this repository (this README, `USAGE.md`, `PRIVACY_POLICY.md`) is released under the [MIT License](./LICENSE.md). The session transcript is a historical record of real development work on Rankelo and is shared for transparency, not as a reusable code sample — see `USAGE.md` for the authenticity and redaction rules that were applied to it.

## Contact

Brandsap · [contact@brandsap.com](mailto:contact@brandsap.com) · Nagpur, Maharashtra, India
