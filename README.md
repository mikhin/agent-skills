# agent-skills

Three skills for getting a second opinion before you trust the first one.

| Skill | What it does |
| --- | --- |
| [`cx`](skills/cx) | Cross-model review of a diff, commit or plan through the Codex CLI. Codex reads, Claude judges. |
| [`consensus`](skills/consensus) | Adversarial multi-agent debate: roles get mutually exclusive hypotheses and must refute each other, exit on agreement. |
| [`multi-agent-research`](skills/multi-agent-research) | Four parallel sub-agents research a topic from different angles, one synthesised report. |

## Install

Any agent, via [skills.sh](https://skills.sh):

```
npx skills add mikhin/agent-skills
```

Claude Code, as a plugin:

```
/plugin marketplace add mikhin/agent-skills
/plugin install agent-skills@agent-skills
```

Skills then show up namespaced: `agent-skills:cx`, `agent-skills:consensus`, `agent-skills:multi-agent-research`.

## Requirements

- Claude Code with sub-agents for `consensus` and `multi-agent-research`
- [Codex CLI](https://github.com/openai/codex) signed in for `cx`, optional for the fourth voice in `consensus`

## License

MIT
