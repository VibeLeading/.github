# VibeLeading

**Small squads. Real-time telemetry. Direct intent.**

VibeLeading is the open-source home of the **Vibe Leading** methodology — the leadership
framework described in Jean Machuca's book _Vibe Leading The AI: The Corporate Race
Against Machines_. The org turns that methodology into practical, installable tooling:
agent **skills** that teach a Pilot how to lead intelligence, and **MCP servers** that give
AI agents "hands" in the corporate engine.

The race against machines is on. These repositories are the cockpit.

---

## The Methodology in One Minute

Vibe Leading replaces the analog management stack — status meetings, vertical reports,
and middle-management translators — with a telemetry-driven cockpit:

| Concept | What it means |
| --- | --- |
| **The Vibe** | The leader's high-frequency strategic intent, written as a **Mission Script** with poetic clarity a human feels and engineering precision an AI can execute. |
| **IRA** (Intent-Result Alignment) | The primary HUD metric: how closely the machine's output matches the Mission Script. 100% = the agents delivered exactly what was intended. |
| **The HUD** | A live scoreboard that replaces the status meeting. The Pilot reads telemetry — Traction, Circuit Delta, Hallucination Debt — instead of asking humans what happened yesterday. |
| **Organizational Geometry** | The 5-Person Racing Squad: 1 Pilot + 4 Specialists + 100+ NPC Agents. Small, hard, and fast — a diamond, not a pyramid. |
| **The Double Tenaza** | The two-handed grip: human intuition on one side, machine precision on the other. |
| **The Garage** | The unified environment where agents connect directly to corporate data through MCP servers — no human middleman. |

Core principle: AI is a massive amplifier. A blurry intent is amplified into a
hallucination; a sharp intent becomes a competitive advantage that scales.

---

## Agent Skills

Skills are installable instruction sets for coding agents (Claude Code, OpenCode, Cursor,
Codex, and 70+ more) that encode a specific piece of the methodology. Each skill is a
dedicated public repo with a root `SKILL.md` — the standard open agent-skills format.

| Skill | What it does | Install |
| --- | --- | --- |
| [mission-script](https://github.com/VibeLeading/mission-script) | Craft high-fidelity Mission Scripts and calibrate the Vibe. Covers High vs Low Vibe, the amplification effect, frequency setting, and the Prompt Ladder (Aspirational → Exemplar). | `npx skills add VibeLeading/mission-script` |
| [ira-prompting](https://github.com/VibeLeading/ira-prompting) | Apply the seven Intent-Result Alignment techniques — Phase Contract, Delta Prompt, Symptom Report, Constraint-First, Design by Reference, Pivot Prompt, Checklist Close — and score prompts with the IRA rubric. | `npx skills add VibeLeading/ira-prompting` |
| [hud-setup](https://github.com/VibeLeading/hud-setup) | Design and calibrate the Scoreboard HUD with IRA thresholds and Circuit Delta targets. Replaces status meetings with green telemetry. | `npx skills add VibeLeading/hud-setup` |
| [pit-stop-audit](https://github.com/VibeLeading/pit-stop-audit) | Run the monthly Vibe Audit and the Pilot's Final Checklist: check the HUD, check the Squad, check the Script. | `npx skills add VibeLeading/pit-stop-audit` |
| [org-geometry](https://github.com/VibeLeading/org-geometry) | Structure the Diamond Squad (Ops Mechanic, Logic Navigator, Creative Pilot, Risk Spotter) and configure the 100+ NPC Agents around a single Pilot. | `npx skills add VibeLeading/org-geometry` |

**Install all five for your project:**

```bash
npx skills add VibeLeading/mission-script VibeLeading/ira-prompting VibeLeading/hud-setup VibeLeading/pit-stop-audit VibeLeading/org-geometry
```

---

## MCP Servers

MCP (Model Context Protocol) servers are the universal connectors of the Garage. They
give NPC Agents "hands" to touch corporate data, documents, and the outside world
directly. The book defines the **3 Must-Have MCP Servers**; the org ships those plus the
**Privacy Shield**.

All servers are TypeScript, follow the official `@modelcontextprotocol/sdk` conventions,
run over stdio, and install with `npx`.

| MCP Server | Role in the book | Tools |
| --- | --- | --- |
| [mcp-hybrid-data-engine](https://github.com/VibeLeading/mcp-hybrid-data-engine) | **The Memory Hub** — connects The Stone (legacy SQL), The Light (vector semantic context), and The Flow (analytical columnar) that feeds the HUD in milliseconds. | `query_stone`, `stone_cdc_tick`, `index_light`, `semantic_search`, `flow_put_rows`, `flow_query` |
| [mcp-document-architect](https://github.com/VibeLeading/mcp-document-architect) | **The Ecosystem Connector** — read/write access to the corporate paper trail, drafting reports aligned with the Pilot's Mission Script. | `list_documents`, `read_document`, `write_document`, `search_documents`, `draft_report` |
| [mcp-real-time-scout](https://github.com/VibeLeading/mcp-real-time-scout) | **The Web & API Connector** — keeps the HUD updated on market shifts and competitor moves so the Pilot can correct course before the dinosaurs see the turn. | `fetch_url`, `search_web`, `monitor_feed`, `track_competitor` |
| [mcp-privacy-shield](https://github.com/VibeLeading/mcp-privacy-shield) | **The Privacy Shield** — the Sanitization Gate (PII → tokens like `[CUSTOMER_01]`), Tiered Sovereignty classification (Vault / Restricted / Internal / Public), and a Compliance Score. | `sanitize_text`, `classify_zone`, `compliance_check`, `shield_catalog` |

Example client configuration (Claude Code, Cursor, or any MCP-compatible agent):

```json
{
  "mcpServers": {
    "hybrid-data-engine": { "command": "npx", "args": ["mcp-hybrid-data-engine"] },
    "document-architect": { "command": "npx", "args": ["mcp-document-architect"] },
    "real-time-scout": { "command": "npx", "args": ["mcp-real-time-scout"] },
    "privacy-shield": { "command": "npx", "args": ["mcp-privacy-shield"] }
  }
}
```

---

## From Dinosaur to Pilot

> "I am no longer a facilitator of meetings. I am an orchestrator of intelligence.
> I do not manage by the clock; I lead by the Scoreboard. My technical authority is my
> engine; my poetic vision is my compass. I will not be a fossil. I am the Pilot."
>
> — The Pilot's Oath, _Vibe Leading The AI_

The race is on. Will you be the fossil, or will you be the Pilot?

---

## License

All repositories in this organization are licensed under the **MIT License** unless a
specific repository states otherwise.