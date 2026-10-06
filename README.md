# Understanding Studio

An [Agent Skill](https://agentskills.io/specification) that helps AI assistants turn complex topics and AI outputs into explanations people can actually understand: plain text, diagrams, interactive single-file HTML, or video storyboards.

**New here?** Download [docs/index.html](docs/index.html) and open it in a browser for an interactive overview of what the skill does, with before-and-after examples. (Viewing the file on GitHub shows only its source code.)

Inspired by [Andrej Karpathy's post](https://x.com/karpathy/status/2105819303471976479) on spending more time understanding LLM outputs through clearer writing (such as [ASD-STE100 Simplified Technical English](https://www.asd-ste100.org/about_STE.html)), diagrams, interactive pages, and explainer videos. This project is not affiliated with or endorsed by Andrej Karpathy or ASD.

## What it does

- Picks the right medium for the question instead of always producing a big artifact.
- Verifies sources before simplifying, and keeps qualifiers like "may" and "only".
- Uses clear-writing rules inspired by STE: short sentences, active voice, one term for one thing.
- Builds offline, accessible, single-file HTML lessons with no CDN and no localStorage.
- Plans videos as storyboards first, and never claims a video was rendered when it was not.
- Asks before using paid tools, extra credits, or external services.

| Topic shape | Default output |
|---|---|
| Single concept | Plain text, plus one example if useful |
| Process or structure | Text plus a diagram |
| Comparing options | A table, plus a decision diagram if needed |
| Linked concepts or a mechanism | Interactive single-file HTML |
| Change over time, video requested | Storyboard and narration |
| Obsidian notes requested | Markdown with two Mermaid diagrams |

## Structure

```
understanding-studio/
├── SKILL.md                      # Triggers, rules, and workflow
├── README.md
├── LICENSE
├── CONTRIBUTING.md               # How to contribute and report test results
├── SECURITY.md                   # Privacy, safety boundaries, and reporting
├── references/
│   ├── formats.md                # Text, diagram, HTML, and Obsidian rules
│   ├── video.md                  # Storyboard, voice, rendering, and cost rules
│   ├── quality.md                # Checklist and regression cases
│   └── sources.md                # Inspiration and design boundaries
├── assets/
│   └── explainer-template.html   # Offline interactive lesson starter
├── docs/
│   ├── index.html                # Interactive overview of the skill
│   └── QUICKSTART.md             # First requests and common problems
└── examples/
    └── packet-loss-lesson.md     # Lesson design specification
```

## Documentation

- [Interactive overview](docs/index.html): download and open in a browser.
- [Quick start](docs/QUICKSTART.md): first requests, prompts, and troubleshooting.
- [Worked example specification](examples/packet-loss-lesson.md): how one mechanism becomes an interactive lesson.
- [Contributing](CONTRIBUTING.md): how to propose changes and report reproducible test results.
- [Security and privacy](SECURITY.md): safety boundaries and how to raise a concern.

## Install

Hosts differ, so check your tool's documentation for the exact skill folder.

1. Clone or download this repository.
2. Copy the folder (with `SKILL.md` at its root) into the skills directory your agent uses.
3. If your tool does not support Agent Skills, paste `SKILL.md` as custom instructions and attach the relevant reference files. This works as a prompt, not as a native skill.

## Example prompts

> Use Understanding Studio to explain this article. Answer the core question in two sentences, then pick the most helpful visual format.

> Use understanding-studio to turn this topic into a single-file interactive HTML lesson with an overall diagram, a hands-on example, common misconceptions, and a comprehension check. No external CDN, no localStorage.

> Storyboard a 90-second explainer video. Do not voice, render, or use paid credits.

## Status

Version 1.0.0. The package files, required metadata, relative links, and the template's basic static properties were checked. The data behind the overview page was checked for completeness with Node.js. It has not yet been tested for triggering behaviour across agent platforms, validated with the official `skills-ref` tool, or tested in a browser for visuals and keyboard use. Issues and pull requests are welcome.

This skill is a set of instructions and resources. It does not add search, speech, video, or browser capabilities to an agent.

## License

[MIT](LICENSE)
