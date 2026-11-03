# Artifacts and adaptable structures

Read this guide when producing or reviewing documentation. First choose the purpose and audience.
Use an existing project template when appropriate; the structures below are adaptable syntheses,
not normative reproductions or universal industry formats.

## Choose the artifact

| Need | Useful artifact |
| --- | --- |
| Preserve learning and questions during exploration | Discussion summary, glossary, or decision and open-question log |
| Record a significant decision and its rationale | ADR |
| Submit a proposal for discussion and convergence | RFC |
| Align product problem, audience, outcomes, and scope | Product/user PRD |
| Detail capabilities, constraints, and verification for engineering | Requirements specification or technical PRD view |
| Plan and discuss user goals | Stories with acceptance criteria |
| Clarify interactions, sequence, and exceptions | Scenario or use case |

Do not generate every artifact for the same decision. Share requirements and sources across views.
A technical PRD should not become a second, contradictory inventory of the product PRD's requirements.

## ADR

A lightweight decision structure inspired by ADRs and MADR:

```markdown
# [ID] — [Decision]
Status: [proposed / accepted / rejected / superseded]
Date and responsible people: [when relevant]

## Context and drivers
[Problem, scope, constraints, and relevant requirements or scenarios.]

## Considered alternatives
[Plausible options and reasons to select or reject them.]

## Decision
[Choice and rationale; identify who approved it.]

## Consequences and verification
[Benefits, losses, risks, and how the outcome will be assessed.]

## Review and references
[What would trigger reconsideration; sources and linked artifacts.]
```

An ADR can be drafted before approval but remains proposed. When superseding a decision, link the
records and update affected documents; do not erase historical rationale to make the record appear consistent.

## RFC

A proposal structure adapted from practices such as Rust RFCs:

```markdown
# [ID] — [Proposal title]
Status, authorship, and decision authority: [according to the project]

## Problem, motivation, and scope
[Who is affected, why now, expected outcome, and boundaries.]

## Proposal
[Behavior and examples understandable to the audience.]

## Necessary detail
[Relevant rules, interfaces, data, states, and qualities.]

## Alternatives and drawbacks
[Include not proceeding when plausible; costs and losses of the proposal.]

## Verification and evolution
[How to validate; impacts and transition when relevant.]

## Open questions and decision
[What remains unresolved, evidence, and discussion outcome.]
```

Do not transfer governance or language-specific requirements into every project. Record an open
question as open; do not invent a decision to give the document an appearance of completeness.

## Product or user PRD

```markdown
# [Product or capability]
Status, owner, and audience: [context]

## Problem and affected people
[Needs, evidence, scenarios, and vocabulary.]

## Expected outcomes
[Goals, confirmed success measures, and hypotheses.]

## Scope and behavior
[Capabilities, journeys, and linked requirements; relevant exclusions.]

## Acceptance and validation
[How to verify behavior and validate usefulness with stakeholders.]

## Dependencies, risks, and open questions
[What conditions the outcome and which decisions remain necessary.]
```

## Technical PRD view or requirements specification

```markdown
# [Technical scope]
Status and connection to product needs: [sources or identifiers]

## Context and boundaries
[System, actors, environments, interfaces, and known responsibilities.]

## Requirements and rules
[Identifier, statement, origin, status, and verification criterion.]

## Architectural characteristics
[Prioritized scenarios, measures, and constraints.]

## Decisions and alternatives
[References to ADRs/RFCs; do not invent architecture to fill the document.]

## Verification, impacts, and open questions
[Required evidence, effects on the existing system, and gaps.]
```

Expand only when risk requires it, such as data transition or identified regulatory requirements.
A technically detailed document is not automatically compliant with ISO/IEC/IEEE 29148.

## User story

```markdown
ID and status: [identifier]
As a [real actor], I want [goal] so that [benefit].
Related rules and requirements: [references]
Acceptance criteria: [observable examples and relevant exceptions]
Open questions: [what still prevents understanding or validation]
```

When useful, express a criterion as given a context, when an action occurs, then an outcome is expected.
Do not impose that syntax on every criterion or confuse an example with a complete requirement.

## Use case

Record the goal, actors, trigger, necessary conditions, main flow, alternatives, and outcome.
Include exceptions that materially affect behavior; do not invent authentication, notification, or
persistence flows absent from the sources merely to complete a sequence.

## Review before delivery

Check audience, purpose, decision status, and local links. Remove unhelpful empty fields and duplication.
Record material gaps and missing evidence. Keep numerical examples explicitly illustrative.
