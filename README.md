# Product Management Skills

Agent Skills for thinking through product problems, making decisions, and preparing work a team can act on.

Product work often starts with something incomplete: a feature request that assumes the solution, research notes that point in different directions, or a proposal that leaves ownership unclear. These skills give an AI agent a structured way to examine that material, expose the decisions underneath it, and produce a useful next step.

Each skill contains instructions and worked examples. Use one on its own or install the collection. There’s no router, required sequence, or personal profile to configure.

## Install

Copy this prompt into a coding agent that can access GitHub and load local skills:

```text
Install all eight product management skills from:
https://github.com/dineshdm-dev/product-management-skills

Read each selected skill’s SKILL.md and load its folder with the supporting
files in `references/`. Use the host’s supported skills location and preserve
existing skills. Do not overwrite an existing installation.

Verify which skills were installed and explain how to invoke them.
If this environment cannot install skills, explain the limitation and how
to load an individual SKILL.md with its supporting references instead.
```

To install one skill, replace “all eight product management skills” with its name, such as `product-architecture`.

This prompt delegates installation to your agent; it is not a universal installer. Exact installation and invocation depend on the host.

## The skills

| Skill | When to use it | What it helps produce |
| --- | --- | --- |
| [Problem Framing](problem-framing/SKILL.md) | A request jumps to a solution, or people disagree about what needs fixing. | A clear problem and decision, with the relevant actors, constraints, evidence, assumptions, and non-goals. |
| [Product Strategy](product-strategy/SKILL.md) | You need to choose an opportunity, customer segment, position, priority, or sequence. | A recommendation that explains alternatives, opportunity cost, tradeoffs, and what would change the choice. |
| [Product Architecture](product-architecture/SKILL.md) | Objects, ownership, states, permissions, or integration boundaries are unclear. | A product model covering relationships, lifecycle, sources of truth, and the consequences for users. |
| [Product Specification](product-specification/SKILL.md) | A defined problem needs to become work a team can build and verify. | Scoped behavior, flows, edge cases, permissions, recovery, acceptance criteria, and unresolved decisions. |
| [Product Experience](product-experience/SKILL.md) | A workflow, onboarding experience, navigation structure, or interaction needs attention. | Proposed flows, terminology, defaults, feedback, accessibility considerations, and error recovery. |
| [Research Synthesis](research-synthesis/SKILL.md) | Interviews, support feedback, surveys, or research notes need to inform a decision. | Findings connected to their evidence, including contradictions, limitations, and implications. |
| [Product Red Team](product-red-team/SKILL.md) | You want to challenge a proposal before committing to it. | Consequential weaknesses, hidden assumptions, failure modes, and concrete mitigations or tests. |
| [Technical Program](technical-program/SKILL.md) | Delivery crosses teams, systems, dependencies, or rollout stages. | Milestones, dependencies, owner roles, decision gates, validation, rollout, recovery, and readiness criteria. |

## Try one

Start with material you already have: a proposal, a draft spec, research notes, or a description of a workflow. Name the skill and the decision you need help with.

```text
Use product-architecture to review the proposal below.

We’re adding shared project templates. Anyone can create a template from
a project, workspace admins can edit it, and teams can use it to start
new projects. Changes should sync automatically.

Identify the objects, ownership, lifecycle, and permission rules we need
to settle before writing the spec. Explain the consequences of the
different choices and recommend a sensible starting model.
```

In this fictional example, “changes should sync automatically” leaves an important decision unresolved. Does an existing project inherit future template changes, or does it become independent when created? The answer affects whether an admin’s edit can change work another team already relies on, and what happens when that team has made its own edits.

That is the kind of ambiguity Product Architecture is intended to surface before it turns into conflicting implementation assumptions.

Other starting points:

```text
Use problem-framing to examine this feature request. What problem are
we trying to solve, and which assumptions need checking?

Use research-synthesis on these interview notes. Separate supported
findings from interpretation and explain what we can decide from them.

Use product-red-team on this launch proposal. Find the most consequential
failure modes and suggest the smallest useful checks before launch.
```

Exact invocation syntax depends on the host. If automatic discovery is unavailable, ask the agent to read the selected skill’s `SKILL.md` and follow its linked runtime references.

## How they work

The skills instruct the agent to use the available evidence, distinguish assumptions from facts, and ask questions when the missing answer materially changes the result. A short question should receive a short answer; a complex proposal may need a fuller model or review.

They also give each task a different focus. Framing examines the problem. Architecture examines the product model. Specification defines behavior a team can build. Red Team challenges the proposal. You can move between them when that helps, without following a prescribed process.

The instructions are readable Markdown, so you can inspect the reasoning they request and adapt it to your own work.

## Compatibility

The skills are plain Markdown directories intended to be loaded individually. Exact installation and invocation depends on the host.

## Limits

A skill can guide how an agent examines a problem. It cannot supply missing customer evidence, prove a causal claim, or make an uncertain commercial decision certain. Review recommendations against your context, especially where the consequences are difficult to reverse.

Results depend on the model, the host, and the material supplied. Worked examples are authored illustrations.

## Author and license

Created by [Dinesh DM](https://github.com/dineshdm-dev).

Available under the [MIT License](LICENSE).
