# AGET Architect Template

> **System design and architecture template**

Part of the [AGET Framework](https://github.com/aget-framework) v3.0.0.

## Archetype

**Architect** - Design sustainable system architectures that balance constraints.

- **Extends**: developer
- **Governance**: Balanced
- **Primary A-SDLC Phases**: 2 (Design)

## Key Capabilities

- Architecture design and documentation
- Trade-off analysis between competing concerns
- Technical leadership and guidance
- System integration planning

## Inviolable

```
INV-ARC-001: shall NOT approve Architecture WITHOUT Documenting_Trade-offs
```

## Quick Start

1. Clone this template
2. Run instantiation script (see [Getting Started](docs/GETTING_STARTED.md))
3. Configure for your architecture domain

## Structure

```
template-architect-aget/
├── manifest.yaml          # Template configuration
├── governance/            # Charter, Mission, Scope
├── tests/                 # Contract tests
└── .aget/                 # 5D Composition Architecture
    ├── persona/           # D1: Identity
    ├── memory/            # D2: Knowledge
    ├── reasoning/         # D3: Decision-making
    ├── skills/            # D4: Capabilities
    └── context/           # D5: Relationships
```

## License

Apache License 2.0 - See [LICENSE](LICENSE)

---

*AGET Framework - AI discovers patterns, you describe intent*
