# Template: Architect Agent

> Design systems and analyze trade-offs with architectural reasoning

**Version**: v3.29.0 | **Archetype**: Architect | **Skills**: 2 specialized + 15 universal

---

## Why Architect?

The Architect archetype brings **systematic design thinking** to system planning. Unlike ad-hoc design discussions, architect agents provide:

- **Structured design** — Decompose systems into components with clear responsibilities
- **Trade-off analysis** — Evaluate competing quality attributes with explicit reasoning
- **Decision documentation** — Record architectural decisions with context and rationale

**For evaluators**: If you need an AI that can reason about system design, evaluate architectural options, and document decisions for posterity, the Architect archetype provides structured design support.

**Domain knowledge that compounds**: Architect agents build persistent understanding of your system landscape — past decisions, quality attribute priorities, and architectural patterns that work in your context. Unlike tools that start fresh each session, your agent accumulates design context that makes each architecture more informed and each trade-off analysis more grounded.

---

## Skills

Architect agents come with **2 archetype-specific skills** plus the universal AGET skills.

### Archetype Skills

| Skill | Description |
|-------|-------------|
| **aget-design-architecture** | Design system architecture including components, relationships, and patterns. Addresses quality attributes and produces architectural artifacts. |
| **aget-assess-tradeoffs** | Analyze trade-offs between competing concerns. Classifies decisions as one-way/two-way doors and provides structured recommendations. |

### Universal Skills

All AGET agents include session management, knowledge capture, and health monitoring:

- `aget-wake-up` / `aget-wind-down` — Session lifecycle
- `aget-create-project` / `aget-review-project` — Project management
- `aget-record-lesson` / `aget-record-observation` — Learning capture
- `aget-check-health` / `aget-check-kb` / `aget-check-evolution` — Health monitoring
- `aget-propose-skill` / `aget-create-skill` — Skill development
- `aget-save-state` / `aget-file-issue` — State and issue management

---

## Ontology

Architect agents use a **formal vocabulary** of 7 concepts organized into 3 clusters:

| Cluster | Concepts |
|---------|----------|
| **System Design** | Architecture, Component, Pattern |
| **Decision Making** | Decision, ADR (Architecture Decision Record) |
| **Trade-off Analysis** | Trade_off, Quality_Attribute |

This vocabulary enables precise communication about architectural decisions.

See: [`ontology/ONTOLOGY_architect.yaml`](ontology/ONTOLOGY_architect.yaml)

---

## Quick Start

```bash
# 1. Clone the template
git clone https://github.com/aget-framework/template-architect-aget.git my-architect-agent
cd my-architect-agent

# 2. Configure identity
# Edit .aget/version.json:
#   "agent_name": "my-architect-agent"
#   "domain": "your-domain"

# 3. Verify setup
python3 -m pytest tests/ -v
# Expected: All tests passing
```

### Try the Skills

```bash
# In Claude Code CLI
/aget-design-architecture  # Create system design
/aget-assess-tradeoffs     # Analyze competing options
```

---

## What Makes Architect Different

| Aspect | Ad-hoc Design | Architect Agent |
|--------|---------------|-----------------|
| **System decomposition** | Informal discussion | Structured component analysis |
| **Trade-offs** | Implicit preferences | Explicit quality attribute evaluation |
| **Decisions** | Lost in chat | ADRs with context and rationale |
| **Reversibility** | Assumed | One-way vs. two-way door classification |
| **Domain memory** | Starts fresh each session | Accumulates architectural expertise over time |

---

## .claude/ Directory

| Directory | Purpose | Owner |
|-----------|---------|-------|
| `.claude/skills/` | Slash command definitions | Framework + Agent |
| `.claude/agents/` | Subagent definitions | Agent |
| `.claude/rules/` | Path-scoped context rules | Agent |

Skills are provided by the template. Agents and rules directories are scaffolded for your customization.

---

## Framework Specification

| Attribute | Value |
|-----------|-------|
| **Framework** | [AGET v3.12.0](https://github.com/aget-framework/aget) |
| **Archetype** | Architect |
| **Skills** | 17 total (2 archetype + 15 universal) |
| **Ontology** | 7 concepts, 3 clusters |
| **License** | Apache 2.0 |

---

## Learn More

- **[AGET Framework](https://github.com/aget-framework/aget)** — Core framework documentation
- **[Archetype Guide](https://github.com/aget-framework/aget/blob/main/docs/GETTING_STARTED.md)** — All 12 archetypes explained
- **[Getting Started](https://github.com/aget-framework/aget/blob/main/docs/GETTING_STARTED.md)** — Full onboarding guide

---

## Related Archetypes

| Archetype | Best For |
|-----------|----------|
| **[Developer](https://github.com/aget-framework/template-developer-aget)** | Implementation and code quality |
| **[Spec-Engineer](https://github.com/aget-framework/template-spec-engineer-aget)** | Requirements and specifications |
| **[Reviewer](https://github.com/aget-framework/template-reviewer-aget)** | Quality assurance and feedback |

---

**AGET Framework** | Apache 2.0 | [Issues](https://github.com/aget-framework/aget/issues)
