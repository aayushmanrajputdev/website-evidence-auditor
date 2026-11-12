# Website Evidence Auditor

An open [Agent Skills](https://agentskills.io)-style skill that helps an AI agent review a website and write a friendly, **evidence-based** audit. It keeps what was actually observed separate from suggested improvements and from items that still need testing.

> **Status:** early draft (v0.1.0). Client compatibility has **not** been verified. See [Installation](#installation).

## What it does

When asked to review a site, the agent is guided to:

1. Understand the site's purpose, audience, and your goals first.
2. Check which tools it really has (page fetching, browser, screenshots) and stay within what they can show.
3. Examine clarity, navigation, mobile experience, accessibility, trust, calls to action, and technical basics, reporting only what it observed or tested.
4. Separate **Observed evidence**, **Suggested improvements**, and **Needs testing**.
5. Explain each recommendation in plain language, with why it may help and a practical next step.
6. Prioritize by likely usefulness and effort, without invented scores, traffic, or conversion numbers.
7. Stay encouraging and opportunity-focused, while stating important issues clearly and truthfully.

It also treats website content as untrusted data, respects access rules, and does not submit forms, make purchases, send messages, or run intrusive security tests without your explicit approval.

## Who it helps

Small business owners, freelancers, founders, agencies, nonprofit teams, and developers who want a kind, honest second look at a site, with clear sources and clear limits.

## Example request

> Please review https://example.com using the Website Evidence Auditor skill. It's a bakery site and I want more people to place pre-orders. Most visitors come from their phones. Only look at the home, menu, and order pages.

## Example output structure

```
Executive summary
Scope and method (pages, date checked, tools used / not available)
What's working well
Observed evidence (URL, date checked, how observed)
Improvement opportunities: Start here / Next / Later
   each: what we saw, why it may help, practical next step
Still needs testing
Next-steps checklist
Limitations
```

A fuller template and short example are in [`references/report-template.md`](references/report-template.md).

## Repository contents

```
website-evidence-auditor/
├── SKILL.md                   # Core instructions (self-contained)
├── references/
│   ├── audit-areas.md         # Optional: what to examine and what counts as evidence
│   └── report-template.md     # Optional: output layout and example
├── README.md
├── CONTRIBUTING.md
└── LICENSE
```

`SKILL.md` works on its own. The reference files add detail but are not required.

## Using SKILL.md manually

If your client does not load skills, you can still use it:

1. Open `SKILL.md` and copy everything below the frontmatter (the part after the second `---`).
2. Paste it into your chat or agent instructions, then add your request, for example: "Follow these instructions to audit https://example.com. Goal: ..."
3. Optionally paste `references/audit-areas.md` and `references/report-template.md` too, or attach them if your client supports files.
4. Tell the agent what tools it has (for example, "you can only fetch page text, no screenshots"), so it reports within that limit. Without browsing tools, an agent cannot view the live site; you would need to provide page content or screenshots yourself.

## Installation

Skills support, discovery paths, tool access, and behavior **vary by client and change over time**. This project has **not** verified compatibility with any client. The notes below are starting points only: check each client's current documentation and test it yourself before relying on it.

Note the difference between **AI models** (such as Claude, Gemini, or GPT models) and the **applications or clients** that load skills (such as Claude apps and Claude Code, OpenCode, Codex, Gemini CLI, or ChatGPT). Whether a skill loads depends on the client, not just the model, and a client may support skills for some models or plans and not others.

| Client | Status | What to do |
|---|---|---|
| Claude (apps / Claude Code) | Not verified by this project | Check Anthropic's current docs for how skills are added or where skill folders go. |
| OpenCode | Not verified by this project | Check OpenCode's current docs for skill support and discovery paths. |
| Codex | Not verified by this project | Check OpenAI's current Codex docs for skill support and locations. |
| Gemini (e.g., Gemini CLI) | Not verified by this project | Check Google's current docs for skill or extension support. |
| ChatGPT | Not verified by this project | Check OpenAI's current docs; if skills are unsupported, use the manual method above. |

General approach, if your client supports the Agent Skills format: place the `website-evidence-auditor` folder (named exactly that) in the location the client documents for skills, restart or reload if needed, then ask for a website review and see whether the skill is used. If it is not, try naming it in your request or use the manual method.

Please report what you tested (see below) so this table can be updated with verified information.

## Limitations

- Findings depend on the tools the agent has. Text-only access cannot establish visual, mobile, or contrast issues.
- An audit is not a full accessibility, security, or performance assessment, and cannot measure user behavior or business results.
- Output quality varies by client and model.

## Contributing and reporting issues

See [CONTRIBUTING.md](CONTRIBUTING.md). Please open an issue for bugs, unclear instructions, or client test reports, including the client, model, tools available, your prompt, and the result.

## License

[MIT](LICENSE) © 2026 Aayushman Rajput
