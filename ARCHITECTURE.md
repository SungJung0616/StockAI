# StockAI Architecture

Notion is the source of truth for architectural decisions. This document maps the approved
StockAI Version 0.1 architecture to repository boundaries.

## System Flow

```text
Data Sources
    ↓
Collection
    ↓
Storage
    ↓
Market Intelligence
    ↓
AI Analysis
    ↓
Presentation
```

Scheduled jobs coordinate this flow without owning its business logic.

## Repository Boundaries

| Package | Responsibility |
|---|---|
| `stockai.collection` | Retrieve, validate, normalize, and deduplicate external data |
| `stockai.storage` | Persist approved structured and flexible data |
| `stockai.intelligence` | Calculate deterministic market intelligence |
| `stockai.analysis` | Explain evidence, risks, comparisons, and confidence |
| `stockai.presentation` | Present research through human-facing interfaces |
| `stockai.jobs` | Orchestrate scheduled workflows |

Dependencies should flow from orchestration toward explicit interfaces. Data-provider,
persistence, intelligence, AI, and presentation concerns must remain separable and testable.

## Testing Boundaries

- `tests/unit/` isolates external systems and validates deterministic behavior.
- `tests/integration/` validates controlled system boundaries.
- `tests/fixtures/` contains small, deterministic, non-proprietary inputs.

## Data Boundaries

`data/raw/` and `data/processed/` are local working directories. Their generated contents are
excluded from Git. PostgreSQL remains the approved primary database, with JSONB available for
flexible raw responses and AI analysis output.

## Change Control

Changes to these boundaries, data schemas, scoring methodology, security controls, public
interfaces, or core technologies require explicit approval and an updated Notion decision.
