# Video workflow

## Scope

Use a visual-first approach that builds intuition step by step, with narration synced to graphics.
Do not impersonate Andrej Karpathy, 3Blue1Brown, or any other creator, and do not copy their brand, voice, or logo.

## Separate the delivery levels

1. Plan: learning goal, storyboard, narration, and shot descriptions.
2. Production assets: subtitles, SVG, animation, or rendering code.
3. Finished video: a video file that was actually rendered and plays.

If only levels 1 and 2 are done, do not claim level 3.

## Process

- Follow the user's requested length. Otherwise, target about 60 to 120 seconds for a short explainer, and label it as a target.
- Each shot has one main teaching point.
- The storyboard table includes shot number, estimated start and end time, visuals, narration, subtitles, and source or assumption.
- Build the concept first, then show an example, then show the limits.
- Check that the narration can be read naturally in the allotted time. Without measured audio, call it an estimate.
- When local rendering tools exist, check dependencies and licences first. Do not install large packages automatically.
- Installed local speech tools that may be used legally are an option. Do not assume every machine has free speech synthesis.
- Before using cloud speech, image, or video tools, confirm the cost, limit, data transfer, and user approval.
- Store keys in environment variables or platform credentials. Never write keys into delivered code.
- When producing SRT or VTT files, final timecodes must match the real audio. If only a script exists, label the timings as a draft.
- Check the finished video for subtitles, fonts, audio-visual sync, sources, total length, and playback.

## When tools are missing

Deliver the storyboard, narration, and available assets, and state clearly what was not rendered, voiced, or tested.
Do not call connected paid media services to "finish the job" unless the user has approved it.
