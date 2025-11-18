# Documentation Specialist Skill - Progressive Disclosure Header

---
TOKEN_BUDGET: 250
TIER: 1
LOAD_TRIGGER: Always loaded when skill is invoked
DEPENDENCIES: None
VERSION: 2.0.0-PDA
---

## Quick Start

Transform Claude Code into an expert software documentation specialist using Progressive Disclosure Architecture for efficient token management.

**Primary Capabilities:**

1. **Greenfield**: Create documentation from templates (SRS, PRD, SDD, arc42, OpenAPI)
2. **Brownfield**: Reverse-engineer documentation from code (Spring Boot, Pulumi, FastAPI, etc.)
3. **Audit**: Review and improve existing documentation
4. **Convert**: Transform between formats (MD, DOCX, PDF)
5. **Diagram**: Generate visual documentation (Mermaid, PlantUML)

## Progressive Disclosure Architecture

**Tier 1 (This File)**: ~250 tokens - Always loaded metadata
**Tier 2 (skill.md)**: ~2,500 tokens - Core routing and execution logic
**Tier 3 (On-Demand)**: ~10,000 tokens - Workflows, reference guides, templates

**Typical Token Load**: 2,750 tokens (Tier 1 + Tier 2)
**With Workflow**: 4,250 tokens (+ single Tier 3 workflow)
**Maximum Load**: 5,000 tokens (+ workflow + reference guide)

## How It Works

1. **User makes request** → Skill classifies intent
2. **Intent routing** → Loads appropriate Tier 3 workflow guide
3. **Executes task** → Follows workflow-specific instructions
4. **Generates artifacts** → Creates documentation files
5. **Post-processing** → Offers format conversion, diagram generation

## Command Examples

**Greenfield (Create from Templates):**
```
Create an SRS for a billing system with PCI-DSS compliance
Create a PRD for a real-time collaboration feature
Generate an arc42 architecture document for microservices platform
```

**Brownfield (Code-to-Docs):**
```
Document my Spring Boot application at ~/projects/customer-api
Generate deployment documentation from Pulumi at ~/infra
Extract API documentation from FastAPI app at ~/data-service
```

**Audit & Improve:**
```
Audit my API documentation at docs/api/openapi.yaml
Review my SDD for completeness and clarity
```

**Convert Formats:**
```
Convert docs/srs.md to Word format
Generate PDF package from all markdown documentation
```

**Generate Diagrams:**
```
Create a C4 container diagram for my microservices
Generate ER diagram from my JPA entities
```

## Next Steps

For detailed implementation, Claude will automatically load the appropriate workflow guide from Tier 3 based on your request intent. You don't need to manually specify which workflow to use.

**For more information, see**: skill.md (Tier 2)
