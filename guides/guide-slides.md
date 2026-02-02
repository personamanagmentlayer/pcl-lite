# Guide — PCL-Lite Slides

How to use the **PCL-Lite Slides bootstrap** (personas for presentations, pitch decks, storytelling, slide design) in any AI chat.

---

## Objective: get structure & copy, then create (same chat or external)

PCL-Lite Slides gives you **deck structure, slide-by-slide copy, speaker notes, data-viz suggestions** in the chat. What you do next depends on your AI:

- **If your AI can create slides** (e.g. ChatGPT with export to deck, Gemini with slides, or any multimodal chat that outputs a deck): use the **structure and copy in the same chat** — ask the AI to build the deck from the outline or paste the slide content into the slides feature. PCL-Lite helps you get clear structure and copy.
- **If your AI doesn’t create slides**: **copy** the outline or slide content and **paste** it into one of the tools below (Google Slides, Gamma, Canva, etc.).

---

## Workflow

1. **In your chat**: Paste the PCL-Lite Slides bootstrap → use `/persona` commands → ask for a deck outline, slide copy, or speaker notes (e.g. 10-slide pitch, investor deck).
2. **Get the output**: The chat returns **ready-to-use text** (slide titles, bullets, speaker notes, structure).
3. **Multimodal AI**: Use that **structure and copy in the slides feature of the same chat** (if it has one) and generate or export the deck.
4. **Or copy-paste**: **Copy** the output and **paste** it into one of the tools below (Google Slides, Gamma, Canva, etc.) if your chat doesn’t create slides.

---

## Where to create slides

**Multimodal AI:** If your chat can create or export slides (e.g. ChatGPT export to PPTX, Gemini slides), use the structure and copy **in the same chat**. Otherwise use one of the tools below:

| Tool | Link | Use case — what to copy-paste |
|------|------|------------------------------|
| **Google Slides** | [slides.google.com](https://slides.google.com) | Free, collaborative. **Paste slide title + bullets** into each slide; use speaker notes panel for notes. |
| **PowerPoint** | [office.com](https://www.office.com) / desktop | Classic decks. **Paste outline** or slide-by-slide copy into placeholders; use Notes pane for speaker notes. |
| **Canva** (Presentations) | [canva.com](https://www.canva.com) | Templates + design. **Paste copy** into text blocks; use structure for slide order. |
| **Gamma** | [gamma.app](https://gamma.app) | AI-assisted decks from outline. **Paste your full outline or bullet list**; Gamma generates a first draft you can edit. |
| **Beautiful.ai** | [beautiful.ai](https://www.beautiful.ai) | Auto-layout slides. **Paste bullet points** into slides; use structure for flow. |
| **Keynote** | [apple.com/keynote](https://www.apple.com/keynote) | Mac/iOS. **Paste slide content** into text boxes; use speaker notes for delivery. |
| **Pitch** | [pitch.com](https://pitch.com) | Collaborative pitch decks. **Paste copy** into slides; use narrative from chat for story flow. |

**Tip:** If the chat gave you **aspect ratio, style, slide count** (e.g. 16:9, minimal, 10 slides), set those in the tool when creating the deck.

---

## 1. Get the bootstrap

All Slides bootstraps are in the **[`bootstrap-slides/`](../bootstrap-slides/)** folder:

- **English**: [bootstrap_lite_slides_en.md](../bootstrap-slides/bootstrap_lite_slides_en.md)
- **French**: [bootstrap_lite_slides_fr.md](../bootstrap-slides/bootstrap_lite_slides_fr.md)

---

## 2. Where to use PCL-Lite

Paste the bootstrap into any AI chat (ChatGPT, Claude, Gemini, DeepSeek, Cursor). The chat gives you **structure, copy, specs, and speaker notes**. If the chat **can create or export slides** (e.g. ChatGPT export to PPTX, Gemini slides), use that output in the same chat; otherwise copy it and paste into one of the tools above.

**Test flow:** Open the bootstrap file → copy full content → paste as first message → wait for *"PCL-Lite Slides v1.0 Ready"* → send `/persona` commands and tasks.

---

## 3. First steps

```bash
# List slides personas
/persona list

# Activate personas (e.g. Slide Designer + Pitch)
/persona +SLIDE_DESIGNER +PITCH_SLIDES

# Set slides context (optional)
/persona slides aspect=16:9 style=minimal format=pdf

# Ask for a deck structure
/persona task "Outline a 10-slide pitch deck: problem, solution, market, team, ask. One message per slide."
```

---

## 4. Slides context

Set once; active personas use it for their answers:

```bash
/persona slides aspect=16:9   # or 4:3, 1:1
/persona slides style=minimal # or corporate, bold
/persona slides format=pdf    # or pptx (for specs)
/persona slides clear         # clear context
```

---

## 5. Load a team

```bash
/persona team load pitch-team
/persona slides aspect=16:9 style=corporate
/persona task "Structure a 12-slide investor deck: hook, problem, solution, traction, team, financials, ask, closing."
```

Teams: `pitch-team`, `data-presentation`, `accessibility-slides`, `education-team`, `full-deck`, `technical-deck`.

---

## 6. Workflow (sequential)

```bash
/persona +STORYTELLER_SLIDES +SLIDE_DESIGNER
/persona workflow STORYTELLER_SLIDES -> SLIDE_DESIGNER
/persona task "Narrative arc for a 15-min conference talk, then slide-by-slide layout and visual hierarchy."
```

---

## 7. Check status and reset

```bash
/persona status        # active personas, slides context
/persona slides clear   # clear slides context
/persona clear         # deactivate all personas
```

---

[← Guides index](./README.md) · [Main README](../README.md)
