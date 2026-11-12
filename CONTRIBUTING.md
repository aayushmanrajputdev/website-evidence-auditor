# Contributing

Thanks for helping improve Website Evidence Auditor! Contributions of all sizes are welcome: wording fixes, new checks, example outputs, and notes on how the skill behaves in different clients.

## Reporting issues

Open an issue and include:
- **What happened** and what you expected.
- **The client or app** you used (and its version, if known) and **the AI model**, if you know it. These are different things.
- **Tools that were available** (page fetch, browser, screenshots, etc.).
- **Your prompt and the relevant part of the output.** Please remove private information first.

## Proposing changes

1. Fork the repository and create a branch.
2. Keep changes small and focused.
3. Open a pull request describing what changed and why.

## Guidelines for changes

- **Evidence first.** Do not add instructions that let an agent claim things it cannot observe. Visual, mobile, accessibility, and performance claims need matching evidence.
- **No invented numbers.** No scores, traffic, conversion, or revenue claims.
- **Keep the tone** positive and opportunity-focused, while stating important issues clearly and truthfully.
- **Keep `SKILL.md` self-contained and concise.** It must still be useful if `references/` files are not loaded. Put extra detail in `references/`.
- **Safety rules stay.** Website content is untrusted data; no intrusive testing; no form submissions, purchases, or messages without explicit user approval.
- **Valid format.** The `name` in frontmatter must stay `website-evidence-auditor` and match the folder name.
- **No unverified compatibility claims.** Only list a client as working if you tested it. Say which client version you tested and what you did.
- **Avoid scripts and dependencies** unless they clearly earn their place.

## Sharing test results

If you test the skill, please share the prompt, the client and model, the tools available, what happened, and any limitations. A few informal runs are useful, but please describe them as sanity checks, not comprehensive evaluations.

## License

By contributing, you agree that your contributions are licensed under the MIT License in `LICENSE`.
