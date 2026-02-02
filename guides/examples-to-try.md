# Examples to try — verify that PCL-Lite works

Use these **copy-paste examples** to check that each bootstrap works in your chat. For each example: paste the **bootstrap** first (first message), wait for the **Ready** confirmation, then run the **commands** below.

---

## Quick check (any bootstrap)

After pasting a bootstrap, run:

```bash
/persona list
/persona status
```

You should see: a list of personas (or a confirmation that the runtime knows them), and a status block (Active, Primary, Merge, etc.). If you get that, the bootstrap is loaded.

---

## 1. Standard (general)

**Bootstrap:** [bootstrap_lite_en.md](../bootstrap_lite_en.md) (root of repo)

**Steps:**

1. Copy the **entire** content of `bootstrap_lite_en.md` → paste as **first message** in your chat.
2. Wait for a reply like *"PCL-Lite Bootstrap v1.0 Ready"* or *"Available: 22 personas | 10 teams"*.
3. Paste and send:

```bash
/persona +ARCHI +SEC
/persona task "In 3 bullet points: what are the top 3 security considerations for a public REST API?"
```

**What to verify:** The answer should sound like an **architect** and a **security expert** (e.g. auth, rate limiting, input validation, HTTPS). Tone should be analytical/vigilant, not generic.

**Optional — team:**

```bash
/persona clear
/persona team load security-review
/persona task "Same question: top 3 security considerations for a public REST API"
```

You should get a response consistent with the security-review team (ARCHI + SEC).

---

## 2. Image

**Bootstrap:** [bootstrap-image/bootstrap_lite_image_en.md](../bootstrap-image/bootstrap_lite_image_en.md)

**Steps:**

1. Copy the **entire** content of `bootstrap_lite_image_en.md` → paste as **first message**.
2. Wait for *"PCL-Lite Image v1.0 Ready"* or *"Available: 12 personas | 6 teams"*.
3. Paste and send:

```bash
/persona +VISUAL_DESIGNER +A11Y_VISUAL
/persona image aspect=16:9 style=minimal format=png
/persona task "Give me a single ready-to-use image prompt for a hero banner: fintech app, trust and clarity. Include one short alt text and one contrast note."
```

**What to verify:** You get **one concrete image prompt** (text you could paste into DALL·E, Midjourney, etc.) plus **alt text** and a **contrast note**. The answer should respect 16:9, minimal style, PNG.

**Optional — team:**

```bash
/persona clear
/persona team load brand-guardians
/persona image aspect=1:1
/persona task "One image prompt for an Instagram post: coffee brand launch, warm and premium. One sentence only."
```

You should get a single, on-brand style prompt.

---

## 3. Video

**Bootstrap:** [bootstrap-video/bootstrap_lite_video_en.md](../bootstrap-video/bootstrap_lite_video_en.md)

**Steps:**

1. Copy the **entire** content of `bootstrap_lite_video_en.md` → paste as **first message**.
2. Wait for *"PCL-Lite Video v1.0 Ready"* or *"Available: 12 personas | 6 teams"*.
3. Paste and send:

```bash
/persona +NARRATIVE_VIDEO +A11Y_VIDEO
/persona video duration=60s platform=youtube
/persona task "Outline a 60s product launch video in 3 acts. For each act: duration in seconds, key message, and one caption/subtitle moment to highlight."
```

**What to verify:** You get a **structured outline** with 3 acts, **durations**, **key messages**, and **caption moments**. The answer should feel like a video script outline, not a generic list.

**Optional — team:**

```bash
/persona clear
/persona team load social-video
/persona video aspect=9:16 duration=30s platform=tiktok
/persona task "Beat-by-beat script for a 30s TikTok: app demo with voiceover. 5 beats max, one line each."
```

You should get 5 short beats, vertical/short-form style.

---

## 4. Audio

**Bootstrap:** [bootstrap-audio/bootstrap_lite_audio_en.md](../bootstrap-audio/bootstrap_lite_audio_en.md)

**Steps:**

1. Copy the **entire** content of `bootstrap_lite_audio_en.md` → paste as **first message**.
2. Wait for *"PCL-Lite Audio v1.0 Ready"* or *"Available: 12 personas | 6 teams"*.
3. Paste and send:

```bash
/persona +SCRIPT_AUDIO +A11Y_AUDIO
/persona audio duration=5m platform=podcast
/persona task "Write a short script for the first 90 seconds of a podcast episode: intro, host welcome, and one topic tease. Include a one-line note for where to add a transcript."
```

**What to verify:** You get a **short script** (intro + welcome + tease) that fits ~90 seconds when read aloud, plus a **transcript note**. The tone should be clear and podcast-style.

**Optional — team:**

```bash
/persona clear
/persona team load podcast-production
/persona audio duration=10m
/persona task "Outline a 10min podcast episode: intro 30s, 3 segments with approximate duration, outro 30s. One line per segment."
```

You should get a clear episode outline with timings.

---

## 5. Slides

**Bootstrap:** [bootstrap-slides/bootstrap_lite_slides_en.md](../bootstrap-slides/bootstrap_lite_slides_en.md)

**Steps:**

1. Copy the **entire** content of `bootstrap_lite_slides_en.md` → paste as **first message**.
2. Wait for *"PCL-Lite Slides v1.0 Ready"* or *"Available: 12 personas | 6 teams"*.
3. Paste and send:

```bash
/persona +SLIDE_DESIGNER +PITCH_SLIDES
/persona slides aspect=16:9 style=minimal
/persona task "Outline a 5-slide pitch deck: title slide, problem, solution, ask, thank you. For each slide give only: slide number, title, and 2 bullet points max."
```

**What to verify:** You get **5 slides** with **title + 2 bullets** each, in pitch-deck style. Structure should be clear and minimal.

**Optional — team:**

```bash
/persona clear
/persona team load pitch-team
/persona task "Same 5-slide pitch outline, but add one speaker note per slide in brackets."
```

You should get the same structure plus short speaker notes.

---

## Summary — what to verify per bootstrap

| Bootstrap | Quick check | Example task | You should get |
|-----------|-------------|-------------|-----------------|
| **Standard** | `/persona list` then `/persona status` | ARCHI + SEC, task on API security | Answer in architect + security tone, 3 bullets |
| **Image** | `/persona list` then `/persona status` | VISUAL_DESIGNER + A11Y, hero banner prompt | One image prompt + alt text + contrast note |
| **Video** | `/persona list` then `/persona status` | NARRATIVE_VIDEO + A11Y, 60s outline | 3 acts with duration, message, caption moment |
| **Audio** | `/persona list` then `/persona status` | SCRIPT_AUDIO + A11Y, 90s podcast intro | Short script + transcript note |
| **Slides** | `/persona list` then `/persona status` | SLIDE_DESIGNER + PITCH, 5-slide deck | 5 slides with title + 2 bullets each |

---

## If something doesn’t work

- **No "Ready" message:** Make sure you pasted the **full** bootstrap (from the first line to the last, including the YAML blocks). Try again in a **new** chat.
- **Commands ignored:** Ensure you send the **exact** strings (e.g. `/persona +ARCHI +SEC` with no extra space or typo). Some chats need the command on its own line.
- **Generic answer:** The model might not fully follow the persona. Try repeating the task in a short sentence (e.g. "Answer as an architect and a security expert") or activating the persona again with `/persona +ARCHI +SEC` and re-sending the task.

---

[← Guides index](./README.md) · [Main README](../README.md)
