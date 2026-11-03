# architecture-brainstorming

A skill for using an agent as the chief engineer's critical teammate in **architecture and requirements
engineering brainstorming**, during inception, evolution, or maintenance of any software project.

The method alternates idea exploration with convergence based on evidence, scenarios, and priorities.
A conversation may yield a decision, experiment, open question, or useful document. It does not
require resolving an entire architecture before delivering a useful first result.

## Installation

Node.js/npm is needed to run the existing `skills` CLI through `npx`. The skill itself consists of
Markdown files and metadata; it has no runtime or custom installer.

### Codex: global installation, by copy

```bash
npx skills add silviobassi/architecture-brainstorming \
  --skill architecture-brainstorming \
  --agent codex --global --copy
```

In the CLI documentation consulted, Codex uses `~/.agents/skills/` for global installation and
`.agents/skills/` for project installation. These commands therefore also cover the shared
`.agents` directory. This repository does not need its own `.codex` directory.

### Codex / .agents: installation in a chosen project

Run from the root of the project where you want to install the skill:

```bash
npx skills add silviobassi/architecture-brainstorming \
  --skill architecture-brainstorming \
  --agent codex --copy
```

### Installation from a local checkout

```bash
git clone https://github.com/silviobassi/architecture-brainstorming.git
npx skills add ./architecture-brainstorming \
  --skill architecture-brainstorming \
  --agent codex --global --copy
```

The path must point to the local checkout. For project installation, run in the destination project,
use the appropriate path to the checkout, and omit `--global`.

For other agents or interactive selection, use `npx skills add silviobassi/architecture-brainstorming`.
See the [official CLI documentation](https://github.com/vercel-labs/skills/blob/main/docs/commands.md)
and [supported agents](https://github.com/vercel-labs/skills/blob/main/docs/agents.md).
Installer options and paths may evolve independently of this skill.

## Usage

In Codex, invoke `$architecture-brainstorming` and describe the question or documents to discuss.
Automatic discovery remains enabled; invocation syntax in other agents depends on the host.

Examples:

> Use $architecture-brainstorming to explore requirements and architectural characteristics for a
> new scheduling system. Start with the problem and stakeholder needs.

> Use $architecture-brainstorming to compare evolution alternatives for this existing system and
> draft a proposed RFC. Distinguish facts, hypotheses, and previously approved decisions.

> Use $architecture-brainstorming to review these requirements and record the decision we just
> approved in an ADR, preserving the questions that remain open.

The agent may recommend investigations and documentation before the chief engineer suggests them.
Drafting a document does not approve its proposals. The skill does not imply authorization to
implement, publish, or change systems.

## Contents

- [SKILL.md](SKILL.md): collaboration, brainstorming, knowledge states, and action boundaries.
- [Requirements](references/requirements.md): elicitation, quality, validation, and traceability.
- [Architecture](references/architecture.md): drivers, scenarios, tradeoffs, views, and evolution.
- [Artifacts](references/artifacts.md): adaptable structures for ADRs, RFCs, product/user PRDs,
  technical views, requirements, stories, and use cases.
- [Sources](references/sources.md): primary references and their limitations.
- [AGENTS.md](AGENTS.md): repository maintenance guidance.

Details are read on demand. The skill imposes no stack, modeling tool, or mandatory documentation
package. Its source is written in English; responses follow the user's language.

## References and license

Sources include ISO, IREB, INCOSE, SEI, and practices for MADR, RFCs, and PRDs. Standards, guidance,
and templates have different purposes. This skill does not incorporate full standards or certify
compliance based on public abstracts.

Original content is under the [MIT license](LICENSE). External references retain their own terms.
