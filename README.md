# Claude Skills

A collection of reusable [Claude skills](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview).
Each skill lives in its own folder under `skills/` and has a `SKILL.md` plus any
templates or files it needs.

## Skills

| Skill | What it does |
|---|---|
| [log-defect](skills/log-defect) | Writes structured defect reports from a standard template and enforces mandatory fields |

## Using a skill

**In Claude Code**, copy the skill folder into your personal or project skills directory:

```bash
git clone https://github.com/Charanjit55588/claude-skills.git
cp -r claude-skills/skills/log-defect ~/.claude/skills/
```

Use `<your-project>/.claude/skills/` instead of `~/.claude/skills/` to share it with a project's team.
Then ask Claude something like "log a defect: the checkout button does nothing after applying a promo code".

**In Claude.ai**, zip the skill folder and upload it under Settings → Capabilities → Skills.

**Template only**: every template is a plain Markdown file, e.g.
[skills/log-defect/templates/defect-template.md](skills/log-defect/templates/defect-template.md).
Copy it into Jira, GitHub Issues, Azure DevOps, or any tracker that accepts Markdown.
