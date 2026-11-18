**English** | [Русский](README.ru.md)

# mercurius-skill-creator

A built-in skill of [Mercurius](https://github.com/opencck/mercurius): how the agent creates and improves its own
skills. It captures the intent from the conversation, asks only what is missing, writes a short SKILL.md with files
for details, checks the draft on 2–3 real requests with and without the skill through `delegate_task`, tunes the
description so the skill triggers where it should, and proposes the version to the owner with `skill_propose`.
Nothing is switched on without the owner's approval.

The skill text is in Russian, the default language of the agent.

## Contents

| File | What it is |
|------|------------|
| `SKILL.md` | When to create a skill, the order of work, how to write |
| `references/anatomy.md` | Fields of `skill_propose`, limits, progressive disclosure, a skeleton |
| `references/testing.md` | Checking a draft on requests with and without the skill |
| `references/description.md` | Writing the description and checking when it triggers |

## Use

Mercurius loads it as a submodule in `skills/skill-creator`; at the start every skill in `skills/` comes into the
catalog as an active version, a changed one as a new version.

```sh
git submodule update --init --depth 1 skills/skill-creator
```

Based on the ideas of the `skill-creator` skill of Anthropic's Claude plugins (intent, interview, tests with and
without the skill, description tuning) and the skill authoring rules of hermes-agent, adapted to the tools and the
owner's approval of Mercurius.

## License

[MIT](LICENSE)
