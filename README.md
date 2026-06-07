# thinking

A Claude Code plugin marketplace of thinking and reasoning skills, built on the open Agent Skills standard - so the same skills work in Claude Code, GitHub Copilot CLI, and other compatible agents.

## Skills

- **consciousness-council** - multi-perspective "Mind Council" deliberation on decisions and creative challenges.
- **scientific-brainstorming** - creative research ideation, interdisciplinary connections, and gap-finding.
- **context-degradation** - recognize and mitigate context failures (poisoning, clash, lost-in-middle).
- **context-fundamentals** - foundational context engineering for AI agent systems.

## Install in Claude Code (plugin)

```
/plugin marketplace add corticalstack/thinking
/plugin install thinking@thinking
```

Restart Claude Code. The skills then appear in autocomplete as `/thinking:<name>` (e.g. `/thinking:consciousness-council`).

## Install in GitHub Copilot CLI (and other agents)

The skills live in `.claude/skills/`, which Copilot CLI reads. Install them with the `gh skill` command (GitHub CLI **v2.90.0+**):

```
# all skills from this repo, available everywhere (user scope):
gh skill install corticalstack/thinking --agent github-copilot --scope user

# or just one skill:
gh skill install corticalstack/thinking consciousness-council --agent github-copilot --scope user
```

In a Copilot CLI session: reload with `/skills reload`, confirm with `/skills info consciousness-council`, then invoke by name, e.g. *"Use the /scientific-brainstorming skill on this research question."*

`gh skill` also accepts `--agent claude-code`, `cursor`, `gemini-cli`, `codex`, and many others, so the same repo serves any Agent-Skills-compatible tool. (Alternatively, copy a skill's folder into your project `.claude/skills/` or personal `~/.copilot/skills/` and run `/skills reload`.)

## Licensing

Repository scaffolding (manifests, README) is MIT. Individual skills retain their own licenses where present: `consciousness-council` and `scientific-brainstorming` are MIT; `context-degradation` and `context-fundamentals` carry no explicit license - treat them as the maintainer's own.
