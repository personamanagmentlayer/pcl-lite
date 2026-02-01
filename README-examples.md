# PCL-Lite Image & Video — Usage Examples

This document gives **concrete usage examples** for [PCL-Lite Image](./image/bootstrap_lite_image_en.md) and [PCL-Lite Video](./video/bootstrap_lite_video_en.md). Copy the bootstrap of your choice into your chat first, then use the commands below.

---

## PCL-Lite Image — Examples

### 1. Single persona: hero banner with accessibility

Activate the Visual Designer and the Accessibility expert, set image context, then ask for a hero banner with alt text.

```bash
/persona +VISUAL_DESIGNER +A11Y_VISUAL
/persona image aspect=16:9 style=minimal format=png
/persona task "Write a detailed image prompt for a hero banner: fintech app, trust and clarity. Include exact alt text and contrast notes."
```

---

### 2. Team: brand-consistent social assets

Load the brand-guardians team so all output stays on-brand.

```bash
/persona team load brand-guardians
/persona image aspect=1:1 style=flat format=png
/persona task "Describe 3 Instagram post visuals for a coffee brand launch: product shot, lifestyle, quote. Keep palette and typography consistent."
```

---

### 3. Sequential workflow: layout then color

Use a two-step workflow: first layout and composition, then color and palette.

```bash
/persona +LAYOUT_EXPERT +COLOR_EXPERT
/persona workflow LAYOUT_EXPERT -> COLOR_EXPERT
/persona task "Propose composition and focal points for a dashboard illustration (data charts + illustration). Then suggest a 5-color palette and usage rules."
```

---

### 4. Infographic with data accuracy

Combine Infographic and Technical Visual for a data-driven graphic.

```bash
/persona +INFOGRAPHIC +TECHNICAL_VISUAL
/persona image aspect=16:9 format=svg
/persona task "Outline an infographic: 'How our API reduces latency by 40%'. Include structure, labels, one main message, and source line. Suggest SVG-safe elements."
```

---

### 5. Icons and accessibility

Get icon specs and accessibility checks in one pass.

```bash
/persona +ICON_DESIGNER +A11Y_VISUAL
/persona task "Define a set of 5 icons for a settings panel (theme, notifications, privacy, language, help). Grid size, stroke weight, and contrast requirements for WCAG AA."
```

---

### 6. Print-ready specs

Use the print specialist and visual designer for print specs.

```bash
/persona +PRINT_PREPRESS +VISUAL_DESIGNER
/persona image format=png
/persona task "Specs for a A4 flyer: safe zone, bleed, resolution, color mode. List do's and don'ts for text and logos."
```

---

### 7. Ask for persona recommendations

When you're not sure which personas to use, ask for suggestions.

```bash
/persona suggest "I need a series of thumbnails for a YouTube channel about DevOps, consistent style and readable on mobile"
```

Then activate the suggested personas and set context before your next task.

---

### 8. Check status and clear context

```bash
/persona status
/persona image clear
/persona clear
```

---

## PCL-Lite Video — Examples

### 1. Single persona: short script outline

Get a tight script structure from the narrative specialist.

```bash
/persona +NARRATIVE_VIDEO
/persona video duration=60s platform=youtube
/persona task "Outline a 60s product launch video: 3 acts, key beats, and one CTA. Include hook in first 5 seconds."
```

---

### 2. Team: social short-form with captions

Load the social-video team and set vertical format for TikTok/Reels.

```bash
/persona team load social-video
/persona video aspect=9:16 duration=30s platform=tiktok format=mp4
/persona task "Beat-by-beat script for a 30s TikTok: app demo with voiceover. Specify where captions go and thumbnail idea."
```

---

### 3. Storyboard then edit

Plan shots first, then get editing guidance.

```bash
/persona +STORYBOARD +VIDEO_EDITOR
/persona workflow STORYBOARD -> VIDEO_EDITOR
/persona video aspect=16:9 duration=90s
/persona task "Storyboard 6–8 shots for a 90s testimonial (talking head + B-roll). Then suggest edit structure: pacing, cut points, and continuity notes."
```

---

### 4. Full production with accessibility

Use the full-production team and keep accessibility in the loop.

```bash
/persona team load full-production
/persona video aspect=16:9 duration=2m format=mp4 platform=web
/persona task "End-to-end plan for a 2min explainer video: script structure, visual style, caption strategy, and audio-description moments. Include delivery checklist."
```

---

### 5. Motion and color for a title sequence

Combine motion design and color grading for a branded intro.

```bash
/persona +MOTION_DESIGNER +COLOR_GRADING_VIDEO +BRAND_VIDEO
/persona video duration=10s aspect=16:9
/persona task "Describe a 10s title sequence: logo reveal + tagline. Motion style, keyframes, color look (LUT direction), and brand constraints (logo safe area, colors)."
```

---

### 6. Sound design and sync

Get sound and sync specs for a short clip.

```bash
/persona +SOUND_VIDEO +VIDEO_EDITOR
/persona video duration=15s
/persona task "Sound design for a 15s product teaser: music style, SFX moments, dialogue level, and sync points. Broadcast-safe levels."
```

---

### 7. Technical delivery specs

Clarify codecs and platform specs before export.

```bash
/persona +TECHNICAL_VIDEO
/persona video platform=youtube format=mp4
/persona task "Delivery specs for YouTube: resolution, frame rate, codec, bitrate, caption format. Include safe zones for captions and end card."
```

---

### 8. Ask for video persona recommendations

```bash
/persona suggest "I need to plan a documentary-style interview, 5 min, with subtitles and a clear narrative arc"
```

Then activate the suggested personas and set video context.

---

### 9. Check status and clear context

```bash
/persona status
/persona video clear
/persona clear
```

---

## Quick reference

| Goal                     | Image                                      | Video                                       |
| ------------------------ | ------------------------------------------ | ------------------------------------------- |
| **Bootstrap**            | [bootstrap_lite_image_en.md](./image/bootstrap_lite_image_en.md) | [bootstrap_lite_video_en.md](./video/bootstrap_lite_video_en.md) |
| **Context**              | `aspect`, `style`, `format`                 | `aspect`, `duration`, `format`, `platform`  |
| **List personas**        | `/persona list`                             | `/persona list`                             |
| **Load team**            | `/persona team load <team-id>`              | `/persona team load <team-id>`              |
| **Suggest personas**     | `/persona suggest "image task"`             | `/persona suggest "video task"`             |
| **Clear context**        | `/persona image clear`                      | `/persona video clear`                      |

---

_For the main PCL-Lite profile (code, architecture, DevOps), see [README.md](./README.md)._
