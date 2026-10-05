# Format rules

These are design choices for this skill. They are not rules from Andrej Karpathy or from ASD-STE100.

## Text

Answer first, then break the concept down. For complex content, go deeper layer by layer. Do not replace technical terms with misleading slogans.
A full lesson may offer a "quick version" and a "deep version". A short answer does not need two versions.

## Diagrams

- Process or causation: nodes are states or actions; label arrows with the condition or effect.
- Architecture or concepts: distinguish containment, data flow, dependency, and association. Do not mix them with the same unlabeled arrow.
- Comparison: prefer tables. Do not draw data with no numeric meaning as precise proportional charts.
- One diagram answers one core question. Split dense diagrams.
- In Markdown environments, use Mermaid. In standalone offline HTML, prefer inline SVG.
- Provide a text alternative. Do not use colour as the only signal.
- In Mermaid, use short node IDs, quote labels, and check arrows and branches.

Obsidian mode: each note contains a `flowchart TD` decision or reading flow, and a `graph LR` concept map. If the topic has no decision, design a real "how to judge" or "how to read" flow. Do not invent causation.

## Interactive HTML

Goal: when the reader changes one condition, they can see how the result or the explanation changes.

- Deliver one HTML file that opens directly. By default it needs no build step, network, CDN, or account.
- Inline the CSS, JavaScript, and SVG. Avoid external fonts and libraries.
- Do not depend on localStorage, cookies, or third-party iframes. Keep page state in memory.
- Use semantic HTML, clear labels, and keyboard-operable controls.
- Support narrow screens, visible focus, sufficient contrast, and reduced-motion settings.
- Good interactions: step through a process, compare conditions, parameter sliders, clickable nodes, expandable derivations, revealable quiz answers.
- Include at least one interaction that changes the reader's understanding. If no natural interaction exists, deliver text or a static diagram instead.
- Calculations show formulas, units, assumptions, and limits. Do not present an unverified mechanism as a scientific simulation.
- Write user input or external text with safe methods such as textContent. Never execute code from input.
- Without permission, add no analytics, telemetry, network requests, or external data submission.
- Do not default to a heavy React project. Use one only when an existing project needs it or the user asks.
- An animated web page is not an MP4. A page without audio is not a narrated video.

Suggested page: direct answer, overall diagram, interactive example, misconceptions and limits, comprehension check, sources.
The template is a starting point. Do not leave placeholder content such as "Topic" or "Sources to be added" in a final lesson.
