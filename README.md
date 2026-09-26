# agent-skills

Claude Code skills for getting a second opinion before you trust the first one — AI code review by another model, multi-agent debate, multi-agent deep research — and an effort loop that builds cheap and verifies hard.

| Skill | What it does |
| --- | --- |
| [`codex-code-review`](skills/codex-code-review) | Code review by OpenAI Codex, judged by Claude. Your diff, commit or plan reviewed by a model that didn't write it. |
| [`multi-agent-debate`](skills/multi-agent-debate) | Three agents get contradicting hypotheses and must refute each other. Exit on agreement, you get the survivor. |
| [`multi-agent-deep-research`](skills/multi-agent-deep-research) | Four researchers on one topic, one report, no blind spots. |
| [`effort-advisor`](skills/effort-advisor) | Recommends an effort level for the task in one or two lines. |
| [`build`](skills/build) | `/build`: implements a spec in one pass at low effort, lists its assumptions. |
| [`verify`](skills/verify) | `/verify`: at high effort — reproduce, adversarial review, randomized tests, reverted-fix check, large inputs. |

## Effort loop

`grill-me` → `/build` → review → `/verify`

`grill-me` turns an idea into a spec, `/build` implements it fast and lists what it assumed, you review the assumptions, `/verify` hunts the edge cases. `/build` and `/verify` set their effort level themselves, for their own reply only. Higher effort finds missed edge cases; a wrong approach is caught at review.

## Install

Any agent, via [skills.sh](https://skills.sh):

```
npx skills add mikhin/agent-skills
```

Claude Code, as a plugin:

```
/plugin marketplace add mikhin/agent-skills
/plugin install agent-skills@mikhin-agent-skills
```

Skills then show up namespaced: `agent-skills:codex-code-review`, `agent-skills:multi-agent-debate`, `agent-skills:multi-agent-deep-research`, `agent-skills:build`, `agent-skills:verify`.

## Requirements

- Claude Code with sub-agents for `multi-agent-debate` and `multi-agent-deep-research`
- [Codex CLI](https://github.com/openai/codex) signed in for `codex-code-review`, optional for the fourth voice in `multi-agent-debate`
- A `grill-me` skill for the effort loop, optional. The effort levels in `/build` and `/verify` apply in Claude Code only

## License

MIT
