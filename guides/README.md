# PCL-Lite — Usage Guides

This folder contains **short guides** to help you use PCL-Lite effectively: standard (general), image, video, audio, and slides bootstraps.

---

## Two ways to use PCL-Lite (text-only vs multimodal AI)

**PCL-Lite always gives you text** in the chat: prompts, scripts, specs, structure. What you do next depends on your AI:

- **If your AI doesn’t generate** image / video / audio / slides: **copy** the output from the chat and **paste** it into a dedicated tool (DALL·E, Runway, ElevenLabs, Google Slides, etc.). Each guide lists **where to paste** with direct links.
- **If your AI is multimodal** (e.g. ChatGPT with DALL·E, Gemini with image/video, or any chat that can generate image/video/audio/slides in the same session): you can **use the PCL-Lite output in the same chat**. Ask for a prompt or script with `/persona`, then paste that prompt or script into the image/video/audio/slides feature of the same AI. PCL-Lite helps you get better, structured prompts and specs even when the AI can generate directly.

**Workflow (text-only AI):** Chat (PCL-Lite) → get text → **copy** → **paste** into external tool → get asset.  
**Workflow (multimodal AI):** Chat (PCL-Lite) → get prompt/script/specs → use it **in the same chat** (e.g. image tab, video feature) or copy-paste to an external tool — your choice.

---

| Guide | Bootstrap | Use case | Where to paste output |
|-------|-----------|----------|------------------------|
| [**Standard**](./guide-standard.md) | [bootstrap_lite_en.md](../bootstrap_lite_en.md) / [bootstrap_lite_fr.md](../bootstrap_lite_fr.md) | Architecture, dev, DevOps, teams | No paste step (text only) |
| [**Image**](./guide-image.md) | [bootstrap-image/](../bootstrap-image/) | Visual design, illustrations, brand, a11y | DALL·E, Midjourney, Ideogram, etc. — see guide |
| [**Video**](./guide-video.md) | [bootstrap-video/](../bootstrap-video/) | Scripts, storyboards, captions, delivery | Runway, Synthesia, Descript, CapCut, etc. — see guide |
| [**Audio**](./guide-audio.md) | [bootstrap-audio/](../bootstrap-audio/) | Podcast, voiceover, sound design, transcripts | ElevenLabs, Descript, Murf, etc. — see guide |
| [**Slides**](./guide-slides.md) | [bootstrap-slides/](../bootstrap-slides/) | Presentations, pitch decks, speaker notes | Google Slides, Gamma, Canva, etc. — see guide |

---

## How to use a guide

1. Choose the bootstrap that matches your task (standard, image, video, audio, or slides).
2. Open the corresponding guide and the bootstrap file (same language: EN or FR).
3. Copy the **entire bootstrap** into your AI chat (first message).
4. Wait for confirmation (e.g. *"PCL-Lite … Ready"*).
5. Use `/persona` commands and ask for what you need (prompt, script, deck structure, etc.).
6. **If your AI can generate** (image/video/audio/slides): use that output **in the same chat** (e.g. paste the prompt into the image or video feature). **If not:** copy the output and paste it into the tool linked in the guide.

---

## Where to run PCL-Lite (chat)

**Chats:** ChatGPT, Claude, Gemini, DeepSeek, Cursor — paste the bootstrap, then use `/persona` commands. The chat gives you **text** (prompts, scripts, specs). If your chat is **multimodal** (e.g. generates image/video/audio/slides), use that text in the same chat; otherwise each guide lists **where to generate** (with links) so you can copy-paste into an external tool.

---

## One bootstrap per conversation (recommended)

**Recommended:** Use **one bootstrap per conversation**. This keeps the model focused on one domain (Standard, Image, Video, Audio, or Slides), so personas and constraints stay coherent and results are easier to optimize.

**Why it helps:** One conversation = one set of personas and one context (e.g. image or video). No mixing of registries, no conflicting constraints, and the model can follow one clear set of instructions. A single bootstrap also uses context and tokens efficiently. When you need another domain, start a **new conversation** and paste the bootstrap that matches (e.g. Video for a script, then Image for a thumbnail in another chat).

---

## Examples to try (verify that it works)

**[examples-to-try.md](./examples-to-try.md)** — Copy-paste examples for each bootstrap (Standard, Image, Video, Audio, Slides) to check that personas and commands work. Each example includes: paste bootstrap → wait for Ready → run commands → what you should get.

---

[← Back to main README](../README.md)
