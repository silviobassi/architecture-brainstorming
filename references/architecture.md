# Architectural reasoning

Use this guide to turn goals and concerns into decision criteria, evaluate alternatives, and guide
evolution. Technology-agnostic means not starting from a preferred stack; concrete technologies can
be compared when the problem and its constraints justify that choice.

## Drivers and architectural significance

Start with business goals, significant requirements, constraints, and risks. A concern warrants
architectural analysis when it influences important structural, behavioral, or evolutionary decisions
and matters to the system's success. Do not apply a filter that excludes structurally significant
functional requirements.

Characteristics may be explicit or inferred as hypotheses from context. Mark inferences as hypotheses
to validate. Do not turn every attribute in a quality catalog into a requirement.

Consider runtime, change, and operations: performance, security, reliability, recoverability,
modifiability, and other relevant qualities. Operational cost, team capabilities, dependencies, and
delivery time may also drive decisions without all being product quality attributes in the same normative sense.

## Quality attribute scenarios

When an adjective is insufficient for a decision, describe:

| Element | Question |
| --- | --- |
| Source | Who or what causes the event? |
| Stimulus | What happens? |
| Environment | Under which operational or change conditions? |
| Affected artifact | Which part of the system or operation is involved? |
| Response | What behavior or outcome is expected? |
| Measure | How will the outcome be evaluated? |

Record priority, sources, and important gaps with the scenario. If measures are missing, explain
which decision depends on them and how to obtain them; do not turn illustrative numbers into approved targets.

QAW and ATAM provide distinct methods for eliciting qualities and evaluating architecture. Use their
ideas about scenarios, prioritization, and tradeoffs proportionately to context. A conversation inspired
by these methods must not be represented as a complete QAW or ATAM assessment.

## Alternatives and recommendations

Compare real alternatives against prioritized drivers. Include maintaining the current state or
deferring when those are plausible options. Do not fabricate a fixed number of alternatives for a table.

For each relevant alternative, consider:

- satisfaction of critical scenarios and requirements;
- benefits and losses, including operations and team effort;
- risks, dependencies, assumptions, and confidence in the evidence;
- change cost, reversibility, and conditions for revisiting the choice.

Avoid unsupported scores and weights. An honest qualitative matrix is preferable to invented numerical
precision. If the outcome depends on a disputed assumption, recommend the smallest investigation or
experiment capable of discriminating among options, with an observable result and stopping condition.

State the recommendation: which option, why, what it sacrifices, and what would change your mind.
Do not equate a more restrictive or complex option with demonstrably better protection against the risk at issue.

## Boundaries and evolution

Distinguish business boundaries, domain models, bounded contexts, components, and deployment units.
Similar names do not establish ownership or dependencies. Record related capabilities without
automatically assigning them to the context currently under discussion.

When architecture needs to be described, choose views according to audience and concern: context
and boundaries, elements and relationships, interfaces, states, or execution as the decision requires.
Do not impose a notation or a complete diagram set; identify how each view addresses relevant
concerns and keep the views consistent.

For existing systems, identify observed state, desired state, and the relevant difference. Compare
gradual and direct transitions when they change risk. Consider compatibility, data, operations,
preservation evidence, and rollback without turning the conversation into migration execution.

## Security and privacy

Start with the unwanted event, its actors, assets, and consequences. Distinguish authentication,
authorization, isolation, auditing, environment restrictions, and abuse by someone with legitimate
access. A mechanism does not automatically address all these risks; explain what it reduces and what remains.

When a solution creates new data processing or limits people's activities, include that consequence
in the comparison. Verify jurisdiction and applicable sources before attributing an obligation to
law or a standard. Finding no prohibition is not universal proof of compliance.
