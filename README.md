# 🔄 Loop Sentinel v2 — Microsoft Edition

**Governed Autonomous Code Agent** · Built by Mullair Jeudi, MD · Kristal Labs

> "AI can THINK autonomously but should not ACT autonomously."

## What It Does

Loop Sentinel is a self-correcting code generation agent with **bounded autonomy**. It generates code, validates it against structural and compliance checks, corrects errors autonomously, and enforces a human-controlled kill switch that limits how many iterations the agent can perform.

Unlike unbounded AI agents, Loop Sentinel enforces governance at every step:

- **Kill Switch**: Human-defined maximum loop count (1-10). When the limit fires, the agent stops and asks — not tells.
- **Risk Posture**: Strict / Balanced / Experimental presets that control validation thresholds
- **Compliance Engine**: Real-time security, accessibility, and standards checks with a 0-100 confidence score
- **Full Audit Trail**: Every iteration logged with timestamps, tokens, errors, and corrections
- **Negotiation Protocol**: When the kill switch fires, the human decides — accept current output, or consciously extend with full awareness of what's being granted

## Architecture

```
USER DESCRIBES → AGENT GENERATES → ENGINE EVALUATES → AGENT CORRECTS → REPEAT OR HALT
                                                              ↑
                                                    KILL SWITCH ENFORCED
                                                    HUMAN DECIDES, NOT AI
```

Single-file HTML application. Zero dependencies. Zero build step. Runs in any modern browser.

## Provider Support

| Provider | Status | Auth |
|----------|--------|------|
| **Azure OpenAI** ★ | Default / Recommended | Endpoint + Deployment Name + API Key |
| Anthropic Claude | Supported | API Key |

Azure OpenAI is the primary provider. The tool is designed to work natively with Azure's responsible AI infrastructure.

## Responsible AI by Design

This tool operationalizes Microsoft's Responsible AI principles:

- **Transparency**: Every loop iteration is logged and exportable (Markdown report + JSON audit trail)
- **Accountability**: Human governance enforced at every level — the agent cannot exceed defined limits without explicit human consent
- **Fairness**: Compliance checks include accessibility validation (alt tags, ARIA, semantic HTML)
- **Reliability & Safety**: Kill switch prevents runaway iteration, token waste, and unbounded cost
- **Privacy**: API keys stay in the browser session. Nothing is stored server-side. Nothing is transmitted except to the provider you choose.

## Exports

- **Markdown Governance Report**: Human-readable summary of every loop — what was generated, what failed, what was corrected, what the compliance score was at each stage
- **JSON Audit Trail**: Machine-readable compliance artifact for enterprise workflows, including full token counts, error categories, and governance decisions

## Quick Start

1. Open `index.html` in any modern browser
2. Select **Azure OpenAI** (recommended) or Claude
3. Enter your API credentials
4. Describe what you want built (e.g., "Build a Pomodoro timer with dark mode")
5. Set your risk posture and kill switch limit
6. Click **INITIATE LOOP SENTINEL**
7. Watch the agent generate, validate, and self-correct in real time
8. When the kill switch fires, decide: accept or extend
9. Export your governance report and audit trail

## Why Governance Matters

Most AI code agents optimize for one thing: completing the task. Loop Sentinel optimizes for something harder: completing the task within boundaries the human defined before the agent started running.

The kill switch isn't a safety net. It's the product. The audit trail isn't a feature. It's the proof that governance happened.

Every enterprise deploying AI agents will eventually need this. The question isn't whether to add governance — it's whether to build it in from the start or bolt it on after something goes wrong.

Loop Sentinel builds it in from the start.

## Live Demo

🔗 [Deployed on Azure Static Web Apps](https://witty-sand-0a53b9c1e6.azurestaticapps.net)

## Built With

- **Azure OpenAI** (GPT-4o) — Primary AI provider
- **Azure Static Web Apps** — Deployment
- **GitHub** — Source control
- **VS Code** — Development
- **GitHub Copilot** — Development assistance
- Vanilla HTML / CSS / JavaScript — Zero external dependencies

## The Builder

**Mullair Jeudi, MD** — Medical intern and founder of Kristal Labs.

27+ AI tools built with zero formal computer science background using a multi-AI orchestration methodology called "The Council" — a structured approach where multiple AI systems (Claude, Gemini, DeepSeek, Groq) work the same problem from different analytical angles, with a human making every final decision.

Research tools shared with faculty at Yale School of Medicine, the University of Chicago, NYU Langone Health, and the Center for Open Science. Three peer-accessible publications on Zenodo with permanent DOIs.

- 🌐 [Credentials](https://mullairjeudi.com)
- 📖 [The AI-Powered Solopreneur](https://www.amazon.com/dp/B0GQDKW7XV) — The methodology behind 27 tools with 0 CS background
- 🔬 [PrepEnfermería](https://prepenfermeria.com) — Multilingual nursing education platform
- 💻 [GitHub](https://github.com/mullairj-gif)

## License

MIT — Free to use, modify, and distribute.

---

*Loop Sentinel v2 Microsoft Edition was built specifically for the Microsoft AI Dev Days Hackathon 2026, incorporating Azure OpenAI as the default provider and enterprise governance controls aligned with Microsoft's Responsible AI framework.*
