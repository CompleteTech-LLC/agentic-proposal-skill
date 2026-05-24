# Agentic Proposal Skill

A CompleteTech LLC Codex skill for creating proposal and SOW-style documents for agentic development opportunities.

## Workflow Diagram

```mermaid
flowchart LR
  A[Discovery facts] --> B[Buyer decision need]
  B --> C[Proposal type]
  C --> D[Scope, assumptions, risks, and acceptance criteria]
  D --> E{Approval-ready?}
  E -->|No| F[Clarify gaps]
  E -->|Yes| G[Proposal, SOW, or approval summary]
  classDef source fill:#eef6ff,stroke:#3778c2,color:#102a43;
  classDef gate fill:#fff7e6,stroke:#c97a12,color:#3d2600;
  classDef output fill:#eefaf0,stroke:#2f8f46,color:#12351d;
  class A,B,C,D source;
  class E gate;
  class F,G output;
```

## What It Does

- Selects the right proposal document by buyer stage and decision need.
- Drafts discovery recaps, one-page pilots, full proposals, SOWs, roadmaps, evaluation plans, risk/control plans, change orders, retainer proposals, and buyer approval summaries.
- Bridges the gap between outreach emails and signed contracts/invoices.
- Keeps the offer focused on practical, bounded agentic workflow implementation with human approval gates, evaluation, monitoring, documentation, support, and handoff.

## Contents

- `SKILL.md` - operating instructions and proposal-selection guide.
- `references/proposal-catalog.md` - reusable proposal and SOW templates.
- `references/use-case-decision-table.md` - quick guide for choosing the right document.
- `references/proposal-lifecycle.md` - end-to-end proposal flow and handoff points.
- `references/proposal-positioning.md` - CompleteTech LLC proposal language and guardrails.
- `scripts/render_proposal.py` - deterministic template listing and rendering helper.

## Quick Start

```bash
python3 scripts/render_proposal.py --list
python3 scripts/render_proposal.py \
  --template one-page-pilot-proposal \
  --var client_name=Acme \
  --var workflow="support triage" \
  --var pain="manual queue review is slowing response times"
```

Rendered templates are drafts. Replace placeholders with verified client, scope, timeline, pricing, risk, and approval details before use.

## Brand Notes

Use a direct, concrete, low-hype tone. Present agentic development as bounded workflow implementation: workflow discovery, tool routing, retrieval, approval gates, evaluation examples, logs, monitoring, documentation, and handoff. Do not invent proof, regulated-use assurances, legal claims, savings metrics, or client facts.
