# Guide — PCL-Lite Image

How to use the **PCL-Lite Image bootstrap** (personas for visual design, illustrations, brand assets, accessibility, print, social visuals) in any AI chat.

---

## Objective: get the best prompt, then generate

PCL-Lite Image gives you **ready-to-use prompts, specs, alt text, palette** in the chat. What you do next depends on your AI:

- **If your AI can generate images** (e.g. ChatGPT with DALL·E, Gemini with image gen, or any multimodal chat): use the prompt **in the same chat** — paste it into the image box or ask the AI to generate from it. PCL-Lite helps you get a better, structured prompt.
- **If your AI doesn’t generate images**: **copy** the prompt from the chat and **paste** it into one of the tools below (Midjourney, Ideogram, etc.).

---

## Workflow

1. **In your chat**: Paste the PCL-Lite Image bootstrap → use `/persona` commands → ask for a prompt or description (e.g. hero banner, Instagram visual).
2. **Get the output**: The chat returns a **ready-to-use prompt** (and optionally specs, alt text, palette).
3. **Multimodal AI**: Paste that prompt into the **image feature of the same chat** (e.g. ChatGPT image tab, Gemini image gen) and generate.
4. **Or copy-paste**: **Copy** the prompt and **paste** it into one of the tools below if your chat doesn’t generate images.

---

## Where to generate images

**Multimodal AI:** If your chat can generate images (e.g. ChatGPT with DALL·E, Gemini), paste the prompt **in the same chat** (image tab or image feature). Otherwise use one of the tools below:

| Tool | Link | Use case |
|------|------|----------|
| **DALL·E** (ChatGPT Plus) | [chat.openai.com](https://chat.openai.com) — use the image tab in ChatGPT | If you already use ChatGPT; paste the prompt in the image box. |
| **Midjourney** | [midjourney.com](https://www.midjourney.com) | High-quality art, illustrations; paste prompt in Discord. |
| **Ideogram** | [ideogram.ai](https://ideogram.ai) | Text in images, logos, posters; paste prompt in the box. |
| **Leonardo.AI** | [leonardo.ai](https://www.leonardo.ai) | Game art, assets, illustrations; paste prompt in the generator. |
| **Stable Diffusion** (e.g. ClipDrop) | [clipdrop.co](https://clipdrop.co/stable-diffusion) | Free tier; paste prompt to generate. |
| **Canva** (AI image) | [canva.com](https://www.canva.com) | Quick visuals, social; use “Apps” → “Text to image” and paste prompt. |
| **Figma** (with AI plugins) | [figma.com](https://www.figma.com) | UI/UX visuals; use plugins that accept text prompts. |

**Tip:** If the chat gave you **dimensions, style, format** (e.g. 16:9, minimal, PNG), set those in the tool before generating.

---

## 1. Get the bootstrap

All Image bootstraps are in the **[`bootstrap-image/`](../bootstrap-image/)** folder:

- **English**: [bootstrap_lite_image_en.md](../bootstrap-image/bootstrap_lite_image_en.md)
- **French**: [bootstrap_lite_image_fr.md](../bootstrap-image/bootstrap_lite_image_fr.md)

---

## 2. Where to use PCL-Lite

Paste the bootstrap into any AI chat (ChatGPT, Claude, Gemini, DeepSeek, Cursor). The chat gives you **prompts, specs, and recommendations**. If the chat **can generate images** (e.g. ChatGPT Plus with DALL·E, Gemini), use that prompt in the same chat; otherwise copy it and paste into one of the tools above.

---

## 3. First steps

```bash
# List image personas
/persona list

# Activate personas (e.g. Visual Designer + Accessibility)
/persona +VISUAL_DESIGNER +A11Y_VISUAL

# Set image context (optional; used for next prompts/specs)
/persona image aspect=16:9 style=minimal format=png

# Ask for a description or prompt
/persona task "Describe a hero banner for a fintech app, with alt text and contrast notes"
```

---

## 4. Image context

Set once; active personas use it for their answers:

```bash
/persona image aspect=16:9   # or 1:1, 4:5, 9:16
/persona image style=minimal # or editorial, flat, 3d
/persona image format=png    # or jpg, webp, svg
/persona image clear        # clear context
```

---

## 5. Load a team

```bash
/persona team load brand-guardians
/persona image aspect=1:1 style=flat
/persona task "Describe 3 Instagram visuals for a coffee launch: product, lifestyle, quote. Consistent palette and typography."
```

Teams: `brand-guardians`, `accessibility-visual`, `social-content`, `print-ready`, `infographic-team`, `visual-critique`.

---

## 6. Workflow (sequential)

```bash
/persona +LAYOUT_EXPERT +COLOR_EXPERT
/persona workflow LAYOUT_EXPERT -> COLOR_EXPERT
/persona task "Propose composition for a dashboard illustration, then a 5-color palette and usage rules"
```

---

## 7. Check status and reset

```bash
/persona status       # active personas, image context
/persona image clear  # clear image context
/persona clear       # deactivate all personas
```

---

[← Guides index](./README.md) · [Main README](../README.md)
