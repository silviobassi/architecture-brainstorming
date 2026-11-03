# Requirements engineering

Use this guide to discover needs, analyze existing documents, write requirements, or assess their
quality. Choose techniques according to uncertainty; do not run all of them as a mandatory sequence.

## Discovery and context

Identify the problem, desired outcome, stakeholders, and decision authority. Explore affected users
and operations, system boundaries, environment, integrations, and real constraints. Separate business
objectives from mechanisms proposed to achieve them.

Choose the technique most likely to reduce the current uncertainty:

| Situation | Useful technique | Evidence sought |
| --- | --- | --- |
| Tacit knowledge or poorly described operations | Example-based interviews, observation, or walkthroughs | Actual work, exceptions, and vocabulary |
| Stakeholders with different expectations | Scenario-oriented workshop and negotiation | Conflicts, priorities, and decision authority |
| Ambiguous interactions or responsibilities | Scenarios, use cases, process or state modeling | Triggers, actors, rules, and transitions |
| Uncertain user experience | Risk-proportionate prototype or simulation | Validation with affected people |
| Existing system | Document and implementation analysis, incidents, operational data | Differences among intent, behavior, and need |

Not every statement needs to become a requirement. Preserve vocabulary, assumptions, and questions
as distinct categories. Do not infer that roles or concepts are equivalent merely because their names resemble each other.

## From need to verifiable requirement

For each item worth formalizing, seek:

- an identifiable need and source;
- a responsible actor or system, relevant conditions, and expected behavior or outcome;
- scope, important exceptions, and data or operational boundaries;
- appropriate verification criteria, with confirmed values or explicit gaps;
- status, justified priority, and dependencies when relevant.

Use stable identifiers when items will be linked. Respect local conventions; do not renumber the
entire collection or impose a management tool merely to obtain traceability.

An adaptable functional-requirement structure is:

> When [condition/trigger] occurs, [system/actor] shall [observable behavior] for [object/scope].

This is a writing aid, not a universal standard. Remove unhelpful fields and separate statements
that involve independent decisions.

For quality requirements, use scenarios and measures as described in [architecture.md](architecture.md).
Do not invent latency, load, availability, recovery, or delivery targets to fill a template.

## Quality review

Look for ambiguity, needs mixed with solutions, undefined terms, contradictions, unsupported
assumptions, and excessive scope. Assess whether each item is understandable, necessary, consistent,
feasible, and verifiable. For the set, assess coverage of relevant scenarios, interfaces, exceptions,
and conflicts; requirement count does not establish completeness.

Separate two questions:

- Is the requirement clearly expressed and verifiable?
- Does it address the actual needs of people and the business?

Textual review does not replace stakeholder validation. Acceptance criteria can guide verification
without necessarily prescribing technology or specific automated tests.

## Priority, change, and traceability

Prioritize by expected outcome, risk, dependencies, urgency, and cost of delay. If using MoSCoW,
ranking, or another technique, explain the criteria; do not assign arbitrary importance on the user's behalf.

Maintain enough links to answer:

> Which need or source supports this requirement? Which decision addresses it? How will we know it was met?

One possible chain is need → requirement → decision → verification evidence. Do not duplicate a
requirement across PRD, RFC, and story as three independent truths; reference a common identifier or source.

When changing a requirement, assess impact on related items, affected states and interfaces, and
existing operations. Establish whether this is a new decision or a clarification. Preserve contract
and historical-name provenance when vocabulary changes do not authorize interface renaming.

## Stories and use cases

Stories express someone's goal and value; they do not replace rules, constraints, or quality
requirements. Use scenarios or use cases when sequences, exceptions, and actor interactions need
clarification. Not every internal behavior needs a story attributed to a fictional user.

Formats are in [artifacts.md](artifacts.md). Engineering references and their limits are in
[sources.md](sources.md).
