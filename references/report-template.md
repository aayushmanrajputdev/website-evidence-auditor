# Report template and short example

Optional layout for the output described in `SKILL.md`. Adapt headings to the user's needs and keep it concise.

## Labels

- **Observed**: seen or tested in this session, with source and method.
- **Suggested**: an improvement idea derived from an observation.
- **Needs testing**: could not be verified with the available tools.
- **Likely usefulness** (High / Medium / Low) and **Effort** (Low / Medium / High): qualitative only, no scores or predicted results.

## Layout

```markdown
# Website Evidence Auditor: <site name or URL>

**Date checked:** <date>
**Pages reviewed:** <list of URLs>
**Goals assumed or provided:** <purpose, audience, user goals>
**Tools used:** <e.g., page fetch, browser at 390px viewport, screenshots>
**Tools not available / not used:** <e.g., no screenshots, no screen reader>

## Executive summary
<3-5 sentences: strengths, biggest opportunities, limits of this audit.>

## What's working well
- <specific strength> (Observed: <URL>)

## Observed evidence
| # | Area | Observation | Source URL | Date checked | How observed |
|---|------|-------------|------------|--------------|--------------|
| 1 | ... | ... | ... | ... | fetched HTML / screenshot / browser |

## Improvement opportunities (Suggested)
### Start here
**1. <Short title>** (Usefulness: High, Effort: Low)
- What we saw: <link to observation #>
- Why it may help: <plain-language reason; no promised outcome>
- Practical next step: <one concrete action>

### Next
...
### Later
...

## Still needs testing
- <check>: <what is needed to verify it, e.g., keyboard walkthrough, real-device test, form submission with your approval>

## Next-steps checklist
- [ ] <action 1>
- [ ] <action 2>

## Limitations
<Brief note: what this audit did not cover and which findings depend on tools you lacked.>
```

## Short example (illustrative, invented site)

> **Executive summary:** The Example Bakery site explains its offer clearly and has an easy-to-find contact page. The biggest opportunities are making the ordering path more prominent and adding descriptions to a few images. This review used fetched page text only, so visual design, mobile layout, and contrast were not assessed.

| # | Area | Observation | Source URL | Date checked | How observed |
|---|------|-------------|------------|--------------|--------------|
| 1 | Clarity | The home page headline states what the bakery sells and where | https://example.com/ | 2026-01-01 | Fetched text |
| 2 | Accessibility | Two images on the About page have no alt attribute in the HTML | https://example.com/about | 2026-01-01 | Fetched HTML |

**Start here: Add short descriptions to the two images** (Usefulness: Medium, Effort: Low)
- What we saw: Observation #2.
- Why it may help: Screen reader users would learn what the images show, and the text can help if images fail to load.
- Practical next step: Add a one-sentence `alt` description to each image in your page editor.

**Still needs testing:** mobile layout at common phone sizes (no rendered view was available); keyboard navigation through the order form (requires a browser).
