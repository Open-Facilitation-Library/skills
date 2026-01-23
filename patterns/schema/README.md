# Pattern Schema

This schema defines the structure for machine-readable facilitation patterns in OFL.

## Design Principles

The schema is based on the **Why-How-Who** framework developed through research at Cooperative AI and discussions with the OFL community:

- **Why**: Purpose and intended outcomes
- **How**: Process mechanics and facilitator techniques
- **Who**: Participant dynamics and roles

## Schema Overview

### Metadata
Basic identification and categorization:
- `id`: Unique identifier (kebab-case)
- `name`: Human-readable name
- `category`: One of `deliberative`, `generative`, or `transformative`
- `tags`: Searchable keywords

### Source & Attribution
Credit to original methodology creators and references.

### Why (Purpose)
What the pattern aims to achieve:
- `purpose`: Primary goal statement
- `outcomes`: Standardized outcome types (for comparison across patterns)
- `use_cases`: When to apply this pattern
- `contraindications`: When NOT to use it

### How (Process)
The mechanics of facilitation:
- `format`: Sync/async/hybrid
- `interaction_mode`: Group size and structure
- `duration`: Time requirements
- `phases`: Ordered steps with actions and outputs
- `intervention_style`: How the facilitator engages
- `artifacts`: Inputs, outputs, and intermediate products

### Who (Participants)
People and dynamics:
- `group_size`: Min/max/optimal participants
- `roles`: Required and optional roles
- `participant_requirements`: Preparation and skills needed
- `power_dynamics`: Hierarchy and anonymity considerations

### AI Facilitation
Guidance for AI-assisted implementation:
- `suitability`: How well this pattern works with AI
- `automatable_phases`: What AI can handle
- `human_required_phases`: What needs human facilitators
- `prompt_templates`: Links to implementation prompts

## Outcome Types

Standardized outcomes allow comparison across patterns:

| Outcome | Description |
|---------|-------------|
| `agreement_building` | Helps group reach consensus |
| `preference_elicitation` | Surfaces individual preferences |
| `error_surfacing` | Identifies gaps in thinking |
| `perspective_taking` | Exposes participants to other views |
| `synthesis` | Aggregates inputs into actionable output |
| `ideation` | Generates new ideas |
| `conflict_resolution` | Resolves disagreements |

## Example

See `../deliberative/cross-pollination.yaml` for a complete example.
