# claude-skills

[![Stars](https://img.shields.io/github/stars/techsaurabh-394/claude-skills?style=flat&logo=github&color=6ea8fe)](https://github.com/techsaurabh-394/claude-skills/stargazers) [![License: MIT](https://img.shields.io/badge/license-MIT-green?style=flat)](LICENSE) [![Last commit](https://img.shields.io/github/last-commit/techsaurabh-394/claude-skills?style=flat)](https://github.com/techsaurabh-394/claude-skills/commits/main) [![Issues](https://img.shields.io/github/issues/techsaurabh-394/claude-skills?style=flat)](https://github.com/techsaurabh-394/claude-skills/issues)

Reusable [Claude Skills](https://docs.claude.com) I use for SEO, technical writing and AI-agent engineering. Each skill is a folder with a `SKILL.md` (YAML frontmatter + instructions). Drop a folder into your Claude skills directory, or zip it and upload it in Claude's skills settings.

| Skill | Use it to |
|---|---|
| [`seo-geo-audit`](skills/seo-geo-audit/SKILL.md) | Audit a page for technical SEO and GEO (visibility in AI answer engines) and get a prioritised fix list |
| [`technical-blog-writer`](skills/technical-blog-writer/SKILL.md) | Write developer-focused posts that rank and get cited, with verified code |
| [`mcp-server-builder`](skills/mcp-server-builder/SKILL.md) | Scaffold a TypeScript MCP server with typed tools and a test checklist |

## Install
1. Copy a folder from `skills/` (or zip it so `SKILL.md` sits at the zip's folder root).
2. Add it in Claude → Settings → Skills (or place it in your skills directory for Claude Code).
3. Ask Claude for the task; it loads the skill when the description matches.

## Contribute
Issues and PRs welcome. Keep each skill focused on one job, with a clear trigger description and a defined output format.

## License
MIT

## Roadmap (contributions welcome)
- [ ] `resume-bullet-optimizer` skill
- [ ] `api-docs-writer` skill
- [ ] `code-review-checklist` skill
- [ ] Example inputs/outputs for each skill in `examples/`

If these save you time, a star helps others find them.
