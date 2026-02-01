# Guide — PCL-Lite Video

How to use the **PCL-Lite Video bootstrap** (personas for scripts, storyboards, editing, captions, motion, delivery) in any AI chat.

---

## 1. Get the bootstrap

All Video bootstraps are in the **[`bootstrap-video/`](../bootstrap-video/)** folder:

- **English**: [bootstrap_lite_video_en.md](../bootstrap-video/bootstrap_lite_video_en.md)
- **French**: [bootstrap_lite_video_fr.md](../bootstrap-video/bootstrap_lite_video_fr.md)

---

## 2. Where to use it

### Chats (recommended to start)

The bootstrap is **text only**: you get **scripts, storyboards, specs, and recommendations**, not generated video. Paste the bootstrap into:

- **ChatGPT** — [chat.openai.com](https://chat.openai.com)
- **Claude** — [claude.ai](https://claude.ai) or in Cursor
- **Gemini** — [gemini.google.com](https://gemini.google.com)
- **DeepSeek** — [chat.deepseek.com](https://chat.deepseek.com)
- **Cursor** — assistant chat

**Test flow:** Open the bootstrap file → copy full content → paste as first message → wait for *"PCL-Lite Video v1.0 Ready"* → send `/persona` commands and tasks.

### Video tools (after the bootstrap)

Use the chat to get **script + specs**, then produce video in your usual tools:

- **Runway** ([runwayml.com](https://runwayml.com)) — Gen-3, editing
- **Synthesia** ([synthesia.io](https://synthesia.io)) — talking-head / avatars
- **Descript** ([descript.com](https://descript.com)) — editing, voice
- **CapCut / Canva** — editing, templates

**Workflow:** Chat (bootstrap video) → script & specs → Runway / CapCut / etc. → final video.

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
