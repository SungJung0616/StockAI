# StockAI

> **We don't predict stocks. We decode the market.**

StockAI is an AI research platform that transforms complex financial data into objective scores, explainable insights, and actionable market intelligence.

Its purpose is not to predict individual stocks or replace investment decisions. StockAI helps investors understand the market environment before deciding where—and whether—to invest.

## Project Overview

Financial markets produce signals across indexes, interest rates, volatility, currencies, commodities, sectors, market breadth, capital flows, sentiment, macroeconomic data, and events.

These signals are related, but they are usually presented through separate tools and interpreted manually. StockAI brings them together into a measurable and explainable market intelligence system.

The platform is intended to answer questions such as:

- Is the market Risk-On, Neutral, or Risk-Off?
- Which sectors are gaining or losing strength?
- Where is capital flowing?
- Is market participation broad or concentrated?
- What is the market rewarding or avoiding?
- What is changing beneath the surface?
- Which evidence supports the conclusion?
- How confident should we be?

## Why This Project Exists

Understanding the market currently requires reviewing dozens of disconnected indicators, including:

- S&P 500, Nasdaq, Dow, and Russell 2000
- Treasury yields and macroeconomic indicators
- VIX, Dollar Index, oil, and gold
- Sector rotation and relative strength
- Market breadth and participation
- ETF, institutional, insider, and options flows
- News, earnings, and scheduled market events

Looking at these indicators independently can lead to conclusions shaped by narrative, recency, or emotion.

StockAI exists to replace that fragmented process with a repeatable research framework. It will measure market conditions, track how they change, and explain the evidence behind every conclusion.

A result should not end with:

> Today’s market score is 78.

It should explain:

> Today’s market score is 78 because Treasury yields are falling, capital is flowing into technology, market breadth is improving, and the VIX remains stable.

The score summarizes the market. The reasoning makes it useful.

## Vision

Use AI to replace assumptions with evidence.

Turn complex market data into clear and actionable insights. Understand the market through data rather than emotion, and continuously improve the quality of investment decisions through learning and validation.

## What StockAI Is Not

StockAI is not:

- A stock prediction engine
- A stock recommendation service
- An automated trading platform
- A replacement for investor judgment
- A guarantee of investment performance

AI should explain the market, identify evidence and risks, and communicate uncertainty. The final investment decision remains human.

## Current Project Status

StockAI is currently in **Phase 1 — Project Foundation**.

Completed:

- Project Goal, Vision, and Roadmap defined
- Initial architecture documented
- Core technology decisions recorded
- Public Git repository established
- Development rules created for human and AI contributors

Not yet implemented:

- Development environment
- Application structure
- Data collection pipeline
- Database schema
- Market scoring methodology
- Market intelligence engine
- AI analysis engine
- Research dashboard

No application code has been written yet.

## Market Intelligence Framework

The initial system will study the market across the following dimensions:

| Dimension | Primary question |
|---|---|
| Market direction | Is the overall market strengthening or weakening? |
| Sector rotation | Where is relative and institutional strength developing? |
| Macro conditions | What economic conditions may be driving the market? |
| Market breadth | How widely is the market participating? |
| Money flow | Where is capital moving? |
| Sentiment | What is the market rewarding or fearing? |
| Event risk | Which events may affect current conditions? |

These dimensions will contribute to an explainable market regime:

- **Risk-On**
- **Neutral**
- **Risk-Off**

The scoring methodology, weights, and confidence rules are **To be defined** through research and historical validation.

## Technology Stack

Technology supports the research process; it does not define the project.

| Area | Current decision |
|---|---|
| Data collection and analysis | Python |
| Primary database | PostgreSQL |
| Flexible data storage | PostgreSQL JSONB |
| Initial dashboard | Streamlit |
| Visualization | Plotly or native Streamlit charts |
| AI model and provider | To be defined |
| Market data providers | To be defined |
| Deployment platform | To be defined |

MongoDB is not planned for the initial version. It may be reconsidered if future requirements involve large volumes of unstructured news or document data.

A future version may use a Next.js or React frontend with a Python backend API.

## Planned System Flow

```text
Market, macro, SEC, news, and event data
                    ↓
            Python Data Collector
                    ↓
             PostgreSQL Database
                    ↓
        Market Intelligence Engine
                    ↓
             AI Analysis Engine
                    ↓
             Research Dashboard
                    ↓
           Scheduled Market Briefs
```

The AI analysis should:

- Generate and explain market scores
- Compare current conditions with historical environments
- Identify supporting and conflicting evidence
- Highlight market risks
- Estimate confidence
- Produce concise market summaries

## Development Workflow

1. Read `AGENTS.md` and the relevant Notion decisions.
2. Start from an approved market question or implementation requirement.
3. Inspect the repository before making assumptions.
4. Implement the smallest complete change.
5. Validate calculations with deterministic data and historical cases.
6. Add or update relevant tests and documentation.
7. Run applicable formatting, linting, type-checking, testing, and build checks.
8. Request approval before changing architecture, schemas, scoring methodology, or core technologies.

Notion is the source of truth for the Goal, Vision, Roadmap, and Architecture. The repository documents their implementation.

## Roadmap Summary

### Phase 1 — Project Foundation

Establish the project structure, development environment, Git workflow, and basic data pipeline.

### Phase 2 — Market Intelligence

Collect and analyze market indexes, sector rotation, macroeconomic indicators, market breadth, capital flows, sentiment, and events.

### Phase 3 — AI Analysis

Explain market conditions, generate market scores, compare historical environments, identify risks, and communicate confidence.

### Phase 4 — Decision System

Combine validated market intelligence and explainable AI analysis into a structured decision-support system.

## Repository Structure

```text
StockAI/
├── AGENTS.md        # Rules for human and AI contributors
├── ARCHITECTURE.md  # Repository-level architecture documentation
└── README.md        # Project philosophy and development entry point
```

The implementation structure will be added after the Phase 1 development environment and module boundaries are approved.

## Next Milestone

Define the first version of the market intelligence framework and establish the foundation for the basic data pipeline.

The milestone should define:

- Initial market dimensions
- Minimum data required for each dimension
- Data-source selection criteria
- Risk-On, Neutral, and Risk-Off methodology
- Scoring transparency and confidence rules
- Historical validation cases
- Python development environment
- Initial application and test structure
- PostgreSQL connectivity
- Collection validation, normalization, deduplication, and status tracking

The immediate objective is not to produce investment signals. It is to build a defensible and testable foundation for understanding the market.
