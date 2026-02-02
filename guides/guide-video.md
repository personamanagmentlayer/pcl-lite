# Guide — PCL-Lite Video

How to use the **PCL-Lite Video bootstrap** (personas for scripts, storyboards, editing, captions, motion, delivery) in any AI chat.

---

## Objective: get script & specs, then generate (same chat or external)

PCL-Lite Video gives you **scripts, storyboards, shot lists, caption strategy, delivery specs** in the chat. What you do next depends on your AI:

- **If your AI can generate video** (e.g. Gemini with video gen, ChatGPT with video, or any multimodal chat with video): use the **script or scene descriptions in the same chat** — paste them into the video feature so the AI generates from your structure. PCL-Lite helps you get a clear script and specs.
- **If your AI doesn’t generate video**: **copy** the script or storyboard and **paste** it into one of the tools below (Runway, Synthesia, Descript, etc.).

---

## Workflow

1. **In your chat**: Paste the PCL-Lite Video bootstrap → use `/persona` commands → ask for a script, storyboard, or specs (e.g. 60s product launch, TikTok beat sheet).
2. **Get the output**: The chat returns **ready-to-use text** (script, shot list, caption moments, technical specs).
3. **Multimodal AI**: Use that **script or scene descriptions in the video feature of the same chat** (if it has one) and generate.
4. **Or copy-paste**: **Copy** the output and **paste** it into one of the tools below (script → Synthesia/Descript, storyboard → Runway/CapCut, etc.) if your chat doesn’t generate video.

---

## Where to generate video

**Multimodal AI:** If your chat can generate video (e.g. Gemini, or future video features), paste the script or scene descriptions **in the same chat**. Otherwise use one of the tools below:

| Tool | Link | Use case — what to copy-paste |
|------|------|------------------------------|
| **Runway** | [runwayml.com](https://runwayml.com) | Gen-3 text-to-video / image-to-video. Paste **scene descriptions** or prompts; use script for structure. |
| **Synthesia** | [synthesia.io](https://synthesia.io) | Talking-head / avatars from script. **Copy-paste your script** into the script field; use your beat list for scenes. |
| **Descript** | [descript.com](https://descript.com) | Edit video + voice. **Paste script** for voiceover or captions; use storyboard for edit structure. |
| **CapCut** | [capcut.com](https://www.capcut.com) | Edit short-form. Use **script** for captions and order of clips; use storyboard for cuts. |
| **Canva** (video) | [canva.com](https://www.canva.com) | Templates + simple edit. Use **script** for text overlays and order; use specs for duration/format. |
| **Pika** | [pika.art](https://pika.art) | Text/image to video. Paste **scene or shot descriptions** from your storyboard. |
| **Luma Dream Machine** | [lumalabs.ai](https://lumalabs.ai) | Text/image to video. Paste **shot descriptions** from your PCL-Lite output. |

**Tip:** If the chat gave you **duration, aspect ratio, platform** (e.g. 60s, 9:16, TikTok), set those in the tool before generating or exporting.

---

## 1. Get the bootstrap

All Video bootstraps are in the **[`bootstrap-video/`](../bootstrap-video/)** folder:

- **English**: [bootstrap_lite_video_en.md](../bootstrap-video/bootstrap_lite_video_en.md)
- **French**: [bootstrap_lite_video_fr.md](../bootstrap-video/bootstrap_lite_video_fr.md)

---

## 2. Where to use PCL-Lite

Paste the bootstrap into any AI chat (ChatGPT, Claude, Gemini, DeepSeek, Cursor). The chat gives you **scripts, storyboards, specs**. If the chat **can generate video** (e.g. Gemini, or future multimodal video features), use that script in the same chat; otherwise copy it and paste into one of the tools above.

**Test flow:** Open the bootstrap file → copy full content → paste as first message → wait for *"PCL-Lite Video v1.0 Ready"* → send `/persona` commands and tasks.

---

## 3. First steps

```bash
# List video personas
/persona list

# Activate personas (e.g. Narrative + Accessibility)
/persona +NARRATIVE_VIDEO +A11Y_VIDEO

# Set video context (optional)
/persona video duration=60s platform=youtube

# Ask for a script outline
/persona task "Outline a 60s product launch video: 3 acts, hook in first 5 seconds, caption strategy"
```

---

## 4. Video context

Set once; active personas use it for their answers:

```bash
/persona video aspect=9:16    # or 16:9, 1:1, 4:5
/persona video duration=60s  # or 15s, 2m
/persona video format=mp4    # or mov, webm
/persona video platform=tiktok  # or youtube, instagram_reels, web
/persona video clear         # clear context
```

---

## 5. Load a team

```bash
/persona team load social-video
/persona video aspect=9:16 duration=30s platform=tiktok format=mp4
/persona task "Beat-by-beat script for a 30s TikTok: app demo with voiceover. Where captions go, thumbnail idea."
```

Teams: `edit-room`, `accessibility-video`, `social-video`, `narrative-team`, `technical-delivery`, `full-production`.

---

## 6. Storyboard then edit

```bash
/persona +STORYBOARD +VIDEO_EDITOR
/persona workflow STORYBOARD -> VIDEO_EDITOR
/persona video aspect=16:9 duration=90s
/persona task "Storyboard 6–8 shots for a 90s testimonial (talking head + B-roll). Then edit structure: pacing, cut points, continuity."
```

---

## 7. Check status and reset

```bash
/persona status       # active personas, video context
/persona video clear  # clear video context
/persona clear        # deactivate all personas
```

---

## Summary

| Goal | Use |
|------|-----|
| Test bootstrap, get scripts / storyboards / specs | ChatGPT, Claude, Gemini, DeepSeek, Cursor |
| Produce the actual video | Runway, Synthesia, Descript, CapCut, etc. (after using the bootstrap in a chat) |

---

[← Guides index](./README.md) · [Main README](../README.md)
