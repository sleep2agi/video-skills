# video-skills

> AI video production toolkit — Dreamina, Remotion, ffmpeg, MiniMax TTS, powered by Claude Code.

## Overview

A collection of battle-tested skills and workflows for producing AI-generated videos using Claude Code as the orchestrator. Covers the full pipeline from script writing to final render.

## Toolchain

| Tool | Role |
|------|------|
| [Dreamina](https://www.capcut.com/ai-tool/dreamina) | AI image & video generation (text-to-video, image-to-video) |
| [Remotion](https://www.remotion.dev/) | Programmatic video composition in React/TypeScript |
| [ffmpeg](https://ffmpeg.org/) | Video encoding, concatenation, subtitle rendering |
| [MiniMax TTS](https://www.minimax.chat/) | AI voice synthesis for narration |
| Claude Code | Orchestration — script, generate, compose, render |

## Workflow

```
Script → AI Image/Video Generation → Voice Synthesis → Composition → Render → QA
         (Dreamina)                   (MiniMax TTS)    (Remotion)    (ffmpeg)
```

## Key Lessons

- **Always verify renders** — AI self-scoring is unreliable. Use `ffprobe` for frame-level validation
- **CJK font rendering** — Specify font paths explicitly in `drawtext` filters to avoid tofu (□□□)
- **Batch generation** — Submit small batches to Dreamina, verify quality before scaling
- **Credit management** — Check `dreamina user_credit` before expensive generation runs

## Related

- [claude-jimeng-skills](https://github.com/sleep2agi/claude-jimeng-skills) — Dreamina CLI skill for Claude Code
- [evoskills](https://github.com/sleep2agi/evoskills) — Self-evolving skill system

## License

MIT