# PCL-Lite: Persona Control Language — Embedded Runtime

**PCL-Lite** is a lightweight, portable implementation of the *Persona Control Language* (PCL) protocol. It turns any AI chat session (ChatGPT, Claude, Gemini, DeepSeek) into a **multi-agent orchestration system** with no external infrastructure.

Inject it via a single bootstrap prompt to orchestrate, configure, and coordinate specialized personas directly in your conversation.

## Why PCL-Lite?

- **Instant multi-agent workflows** — Turn a linear chat into a structured collaborative session.
- **Zero setup** — Copy and paste the bootstrap into your preferred LLM. No installation required.
- **Structured collaboration** — Activate an *Architect* and a *Critic* at once for more robust outcomes.
- **Fine-grained control** — Adjust tone, verbosity, and response merge rules.

## Available bootstrap files

Repository layout: general bootstraps at root; Image and Video in **`bootstrap-image/`** and **`bootstrap-video/`**.

**→ [guides/](./guides/)** — Usage guides for standard, image, and video (how to start, commands, platforms, workflow).

This repository provides bootstrap prompts tailored to context window size and use case:

### PCL-Lite "Lite" (recommended to get started)

A token-efficient bootstrap with everything needed to manage personas and simple workflows.

- **Best for**: Quick sessions, standard models (GPT-3.5, Haiku, Gemini Flash), prototyping.
- **Features**: Activation, CRUD, configuration (tone/verbosity), simple sequences, teams, presets.
- **Files**:
  - **English**: [bootstrap_lite_en.md](./bootstrap_lite_en.md)
  - **French**: [bootstrap_lite_fr.md](./bootstrap_lite_fr.md)

### PCL-Lite Image (image and visual workflows)

A dedicated profile for **image creation, visual design, and asset production**. Same `/persona` commands with 12 image-focused personas and optional image context (aspect ratio, style, format).

**→ Bootstraps are in the [`bootstrap-image/`](./bootstrap-image/) folder.**

- **Best for**: Image prompts, visual consistency, brand assets, accessibility (alt text, contrast), social visuals, print specs.
- **Personas**: Visual Designer, Illustrator, Photo Editor, Brand Visual Guardian, Infographic, Icon Designer, Accessibility Visual, Layout Expert, Color Expert, Technical Visual, Print Prepress, Social Visual.
- **Teams**: brand-guardians, accessibility-visual, social-content, print-ready, infographic-team, visual-critique.
- **Files**:
  - **English**: [bootstrap_lite_image_en.md](./bootstrap-image/bootstrap_lite_image_en.md)
  - **French**: [bootstrap_lite_image_fr.md](./bootstrap-image/bootstrap_lite_image_fr.md)

```bash
# Activate visual and accessibility personas
/persona +VISUAL_DESIGNER +A11Y_VISUAL

# Set image context for next generation
/persona image aspect=16:9 style=minimal format=png

# Task for image-related output
/persona task "Describe a hero banner for a fintech app, with alt text"
```

### PCL-Lite Video (video and motion workflows)

A dedicated profile for **video production, editing, motion design, and delivery**. Same `/persona` commands with 12 video-focused personas and optional video context (aspect ratio, duration, format, platform).

**→ Bootstraps are in the [`bootstrap-video/`](./bootstrap-video/) folder.**

- **Best for**: Scripts, storyboards, editing advice, captions and accessibility, social/short-form, color grading, sound design, delivery specs.
- **Personas**: Video Editor, Script & Continuity, Motion Designer, Color Grading, Sound Video, Storyboard, Narrative Video, Creative Director Video, Brand Video, Social Video, Accessibility Video, Technical Video.
- **Teams**: edit-room, accessibility-video, social-video, narrative-team, technical-delivery, full-production.
- **Files**:
  - **English**: [bootstrap_lite_video_en.md](./bootstrap-video/bootstrap_lite_video_en.md)
  - **French**: [bootstrap_lite_video_fr.md](./bootstrap-video/bootstrap_lite_video_fr.md)

```bash
# Activate editor and accessibility personas
/persona +VIDEO_EDITOR +A11Y_VIDEO

# Set video context
/persona video aspect=9:16 duration=60s format=mp4 platform=tiktok

# Task for video-related output
/persona task "Outline a 60s product launch video with captions strategy"
```

## Quick start

1. Open the bootstrap file for your language (e.g. `bootstrap_lite_en.md`).
2. Copy the entire contents.
3. Paste into a new conversation with your AI assistant.
4. Wait for confirmation (e.g. *"PCL-Lite Bootstrap v1.0 Ready"*).
5. Use `/persona` commands:

```bash
# List available personas
/persona list

# Activate an Architect and a Security Expert
/persona +ARCHI +SEC

# Assign a task
/persona task "Design a secure architecture for a banking API"

# Set the response lead
/persona primary=SEC

# Get persona recommendations for a task
/persona suggest "audit our auth flow"
```

## PCL standard

PCL-Lite is an embedded variant of the full **PCL** (Persona Control Language) standard. For the complete specification and full implementations, see the main repository:

**[https://github.com/personamanagmentlayer/pcl](https://github.com/personamanagmentlayer/pcl)**

## License

This project is licensed under **Apache-2.0**. See [LICENSE](./LICENSE) for details.

---

*PCL-Lite is part of the Persona Management Layer project.*
