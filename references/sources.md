# Sources and design boundaries

## Main inspiration

[Andrej Karpathy's post on X](https://x.com/karpathy/status/2105819303471976479)

The post suggests asking LLMs to explain things in ASD-STE100 style, or a looser "80%" version, to improve readability. It then suggests going further with diagrams, interactive HTML, and custom explainer videos, to help people understand and supervise the growing volume of AI output.

This skill turns those ideas into steps for choosing a medium, verifying facts, designing the explanation, producing the artifact, and checking quality.
The post is not a specification for this skill, and it does not guarantee that every model can follow STE correctly or produce usable video.

## Standard background

[ASD-STE100 official site: About STE](https://www.asd-ste100.org/about_STE.html)

The official standard contains writing rules, a controlled dictionary, and rules for technical nouns and technical verbs.
This package does not reproduce the full dictionary or the full standard, and it cannot certify compliance.
For non-English output, the skill borrows clear-writing principles only. It is not an official STE version for any other language.

## Package format

[Agent Skills specification](https://agentskills.io/specification)

The package uses the required `name` and `description` fields and the `SKILL.md`, `references/`, and `assets/` structure.
Platform support, install location, and tool permissions depend on the host product.

## Additional design choices

Offline HTML, no storage dependence, Obsidian two-diagram notes, cost confirmation, source verification, safety boundaries, and the quality rules were added for this package. They should not be attributed to Andrej Karpathy.
