# Architect Domain Vocabulary

**Version**: 1.1.0
**Status**: Active
**Owner**: template-architect-aget
**Created**: 2026-01-10
**Updated**: 2026-01-11
**Scope**: Template vocabulary (DRIVES instance behavior per L481)
**Archetype**: Architect
**Template**: VOCABULARY_TEMPLATE_v3.3

---

## Meta

```yaml
vocabulary:
  meta:
    domain: "architecture"
    version: "1.0.0"
    owner: "template-architect-aget"
    created: "2026-01-10"
    theoretical_basis:
      - "L481: Ontology-Driven Agent Creation"
      - "L482: Executable Ontology - SKOS+EARS Grounding"
    archetype: "Architect"
```

---

## Concept Scheme

```yaml
Architect_Vocabulary:
  skos:prefLabel: "Architect Vocabulary"
  skos:definition: "Vocabulary for architect domain agents"
  skos:hasTopConcept:
    - Architect_Core_Concepts
  rdf:type: skos:ConceptScheme
```

---

## Core Concepts

### Architecture

```yaml
Architecture:
  skos:prefLabel: "Architecture"
  skos:definition: "Fundamental structure of a system"
  skos:broader: Architect_Core_Concepts
  skos:inScheme: Architect_Vocabulary
```

### Component

```yaml
Component:
  skos:prefLabel: "Component"
  skos:definition: "Discrete unit within an architecture"
  skos:broader: Architect_Core_Concepts
  skos:inScheme: Architect_Vocabulary
```

### Interface

```yaml
Interface:
  skos:prefLabel: "Interface"
  skos:definition: "Boundary between components"
  skos:broader: Architect_Core_Concepts
  skos:inScheme: Architect_Vocabulary
```

### Quality_Attribute

```yaml
Quality_Attribute:
  skos:prefLabel: "Quality Attribute"
  skos:definition: "Non-functional requirement like performance or security"
  skos:broader: Architect_Core_Concepts
  skos:inScheme: Architect_Vocabulary
```

### Design_Decision

```yaml
Design_Decision:
  skos:prefLabel: "Design Decision"
  skos:definition: "Significant choice affecting system structure"
  skos:broader: Architect_Core_Concepts
  skos:inScheme: Architect_Vocabulary
```

---

## Concept Relationships

```yaml
relationships:
  hierarchical:
    - parent: Architect_Core_Concepts
      children: [Architecture, Component, Interface, Quality_Attribute, Design_Decision]

  associative:
    - subject: Architecture
      predicate: skos:related
      object: Component
    - subject: Design_Decision
      predicate: skos:related
      object: Quality_Attribute
```

---

## EKO Cross-References

Per AGET_EXECUTABLE_KNOWLEDGE_SPEC.md:

| Vocabulary Term | EKO Term | Relationship |
|-----------------|----------|--------------|
| Architecture | EKO:System_Structure | skos:exactMatch |
| Design_Decision | EKO:Decision_Record | skos:closeMatch |
| Quality_Attribute | EKO:Quality_Requirement | skos:broadMatch |

---

## Extension Points

Instances extending this template vocabulary should:
1. Add domain-specific terms under appropriate broader concepts
2. Maintain SKOS compliance (prefLabel, definition, broader/narrower)
3. Reference foundation L-docs where applicable
4. Use `research_status` for terms under investigation

---

## References

- L481: Ontology-Driven Agent Creation
- L482: Executable Ontology - SKOS+EARS Grounding
- R-REL-015: Template Ontology Conformance
- AGET_VOCABULARY_SPEC.md

---

*Architect_VOCABULARY.md v1.0.0 — SKOS-compliant template vocabulary*
*Generated: 2026-01-10*
