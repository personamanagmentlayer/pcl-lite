# Guide — PCL-Lite Image

How to use the **PCL-Lite Image bootstrap** (personas for visual design, illustrations, brand assets, accessibility, print, social visuals) in any AI chat.

---

## 1. Get the bootstrap

All Image bootstraps are in the **[`bootstrap-image/`](../bootstrap-image/)** folder:

- **English**: [bootstrap_lite_image_en.md](../bootstrap-image/bootstrap_lite_image_en.md)
- **French**: [bootstrap_lite_image_fr.md](../bootstrap-image/bootstrap_lite_image_fr.md)

---

## 2. Where to use it

Paste the bootstrap into any AI chat (ChatGPT, Claude, Gemini, DeepSeek, Cursor). The bootstrap is **text only**: you get **prompts, specs, and recommendations**, not generated images. Use the output in your usual image tools (DALL·E, Midjourney, Figma, etc.).

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
