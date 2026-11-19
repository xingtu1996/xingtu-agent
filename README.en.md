# xingtu-agent · Agent Deployment Case Notes

> Under local construction, not published yet. This repo records how Agents land in real tasks and the trade-offs involved; it is not Agent framework source code.

[![License: MIT](https://img.shields.io/badge/License-MIT-orange.svg)](./LICENSE) ![Status](https://img.shields.io/badge/status-local-lightgrey)

## In one line

A collection of real Agent deployment cases: how tasks are decomposed, how authorization boundaries are set, how memory and receipts are kept, and how failures recover. It captures decision chains and boundaries, not explanations of what an Agent is.

## Why this repo exists

There are many articles about Agents, but few explain "why we chose this at the time, what happened later, and where it stops working." The value here is not a feature list but the decision chain: under which constraints an Agent approach holds, and why it fails in a different scenario.

## Boundaries with neighboring repos

| Repo | Covers | Does not cover |
|---|---|---|
| `xingtu-super-agent` | Methodology and minimal implementation of the cross-Agent system (XSA) | Does not collect third-party Agent cases |
| `xingtu-agent-skills` | Reusable installable Agent skills | Does not do scenario decision retrospectives |
| **xingtu-agent** (this repo) | Agent deployment cases and decision trade-offs | Not a skill library or framework source |

## Core content

- **Scenario case cards**: a uniform template recording background constraints, option choice, verification result, and boundaries.
- **Decision chains**: why A over B, the evidence at the time, and whether it held up.
- **Failure archive**: real patterns of Agent drift, authorization overreach, and missing receipts, with guardrail practices.

## On knowledge-QA-style cases

A team knowledge-QA assistant (including the spec-driven requirements to design to tasks to acceptance chain) is a reusable methodology-layer case. This repo records only the de-identified mechanisms and decision chains — how to split specs, run acceptance, and keep evidence. It does not record project entities, code, internal paths, or client information. Placeholders live in `cases/_pending/`; nothing enters the repo until a de-identified draft is ready.

## Quick start

```bash
git clone <repo-url> xingtu-agent
cd xingtu-agent
# Template: cases/_TEMPLATE.md
```

Before adding a case, read `cases/_TEMPLATE.md`. Every case needs a status label and evidence source. Inference without evidence is `design`; only locally verified and recorded work is `verified`.

## Case status labels

| Label | Meaning |
|---|---|
| `design` | Design or idea only, not verified |
| `public-source` | Compiled from public material, not tested here; needs link and check date |
| `verified` | Run locally with reproducible evidence |
| `production` | In production use |

## Contribution rules

- De-identification is a hard gate: no client names, personal names, internal domains, internal platform paths, or business data.
- Cases keep decision chains and timelines; de-identification must not erase the sense of the scene. Mechanisms only, no entities.
- Label the source and verification level of every number; second-hand data is not a criterion.

## License

[MIT](./LICENSE) · 行途 XingTu

## Author

行途 XingTu (engineering byline) · WeChat: 行途技术手记
