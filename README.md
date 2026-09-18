# agent-skills

Three Claude Code skills for getting a second opinion before you trust the first one: AI code review by another model, multi-agent debate, multi-agent deep research.

| Skill | What it does |
| --- | --- |
| [`codex-code-review`](skills/codex-code-review) | Code review by OpenAI Codex, judged by Claude. Your diff, commit or plan reviewed by a model that didn't write it. |
| [`multi-agent-debate`](skills/multi-agent-debate) | Three agents get contradicting hypotheses and must refute each other. Exit on agreement, you get the survivor. |
| [`multi-agent-deep-research`](skills/multi-agent-deep-research) | Four researchers on one topic, one report, no blind spots. |

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

Skills then show up namespaced: `agent-skills:codex-code-review`, `agent-skills:multi-agent-debate`, `agent-skills:multi-agent-deep-research`.

## Requirements

- Claude Code with sub-agents for `multi-agent-debate` and `multi-agent-deep-research`
- [Codex CLI](https://github.com/openai/codex) signed in for `codex-code-review`, optional for the fourth voice in `multi-agent-debate`

## License

MIT
