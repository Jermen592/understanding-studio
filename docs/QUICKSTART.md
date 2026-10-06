# Quick start

Understanding Studio is a set of agent instructions and resources, not an application or a new model. Your host provides the tools it can use.

## Get the skill

```sh
git clone https://github.com/Jermen592/understanding-studio.git
```

Follow your agent host's documentation to place the repository folder in its supported skills directory. Keep SKILL.md at the folder root and preserve references/ and assets/. Installation paths vary by host; this project does not claim verified compatibility with every host.

If your host cannot load skills, provide SKILL.md as instructions and attach only the reference files relevant to your task. This is prompt-based use, not native installation.

## First request

> Use understanding-studio to explain this topic to a beginner. Answer the core question first. Choose the simplest useful medium. Preserve uncertainty and sources. Do not use paid tools or publish anything.

## Request an interactive lesson

> Use understanding-studio to turn [TOPIC OR SOURCE] into one offline HTML file. Include an overall diagram, one hands-on example, misconceptions, and comprehension checks with explanations. Inline all CSS, JavaScript, and SVG. No CDN, external fonts, tracking, localStorage, or network requests. Use my language. State what you actually tested.

Download the generated HTML and open it in a browser. Merely viewing HTML source on GitHub does not run the lesson. The supplied assets/explainer-template.html is a starter, not a completed subject lesson.

## Ask for a video safely

> Produce a storyboard and narration for a 90-second explanation of [TOPIC]. Label timing estimates. Do not render, synthesize speech, install dependencies, or use paid services without asking me first.

## Review the result

- Check whether the answer addresses your actual question.
- Check sources, units, dates, assumptions, and qualifiers.
- Change an input and check whether the explanation changes correctly.
- Try keyboard navigation and a narrow screen.
- Ask the agent to distinguish executed checks from checks it could not run.

## Common problems

| Problem | What to check |
|---|---|
| The skill does not trigger | Verify the host's installation instructions; explicitly mention understanding-studio. |
| No file is produced | The host may lack file tools; request complete source code instead. |
| A web page or video cannot be rendered | Request code or a storyboard, and require an honest statement of tool limits. |
| The answer is too elaborate | Set a sentence limit or explicitly request plain text only. |
| The agent claims STE compliance | Ask for evidence from the full standard; this skill does not certify compliance. |

See [a worked lesson](../examples/packet-loss-lesson.md) and the [quality checklist](../references/quality.md).
