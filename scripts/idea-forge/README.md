# Idea Forge

A lightweight thinking skill for **Brainstorm → Grill → Crystallize**.

It is intentionally smaller and less ceremonial than a full engineering workflow. Its purpose is to help a strong model do three things well:

1. **Expand** — propose non-obvious directions before prematurely converging.
2. **Grill** — resolve one high-impact decision at a time, always with the model's own recommendation.
3. **Crystallize** — turn the conversation into a concise brief/spec another agent can execute.

## Why this version exists

`grill-me` is excellent at exposing unresolved decisions, but it is primarily convergent: it stress-tests a plan that already exists.

Superpowers brainstorming is excellent at structured requirement discovery, but its broader workflow can be more process than you need when the real goal is simply to think clearly before building.

Idea Forge combines the parts that matter most for early-stage thinking:

- The model contributes ideas instead of making you answer blank questions.
- It asks only one question at a time.
- Every important question comes with a recommendation.
- It tracks decisions and contradictions.
- It stops when further questioning has low value.
- It produces a handoff that can go directly to a coding/research/design agent.

## Install

### Claude Code — personal skill

```bash
mkdir -p ~/.claude/skills/idea-forge
cp SKILL.md ~/.claude/skills/idea-forge/SKILL.md
```

Invoke with:

```text
/idea-forge
```

For a project-only install, place the folder at:

```text
<repo>/.claude/skills/idea-forge/
```

### Codex — personal skill

```bash
mkdir -p ~/.agents/skills/idea-forge
cp SKILL.md ~/.agents/skills/idea-forge/SKILL.md
```

Then select it from `/skills` or mention it explicitly:

```text
$idea-forge
```

For a project-only install, place the folder at:

```text
<repo>/.agents/skills/idea-forge/
```

## Good prompts

```text
/idea-forge
I have an idea for using WiFi sensing + an LLM to make a home feel emotionally aware.
```

```text
/idea-forge grill me
I think the product should infer whether my dog is anxious when nobody is home.
```

```text
$idea-forge
Brainstorm this first. Don't let me lock onto my first idea too early:
<idea>
```

```text
/idea-forge crystallize
Turn what we decided into a brief I can hand to Codex.
```

## Suggested workflow

```text
messy thought
   ↓
idea-forge
   ↓
3 strong directions
   ↓
one-decision-at-a-time grilling
   ↓
decision-ready brief/spec
   ↓
Codex / Claude Code / research / design agent
```

## Tuning

The default is deliberately opinionated and compact. If you want to tune it later, the highest-leverage knobs are:

- **More creative:** increase the number of Expand rounds, not the number of ideas per round.
- **More aggressive:** tell Grill to challenge every unstated assumption that could invalidate the idea.
- **Faster:** skip Expand when the plan is already concrete.
- **More product-oriented:** add distribution, willingness-to-pay, and habit formation to the Grill branches.
- **More technical:** add architecture constraints, failure budgets, observability, and migration/rollback decisions.
