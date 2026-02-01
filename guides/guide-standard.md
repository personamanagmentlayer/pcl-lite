# Guide — PCL-Lite Standard

How to use the **standard PCL-Lite bootstrap** (general personas: architecture, development, DevOps, security, etc.) in any AI chat.

---

## 1. Get the bootstrap

- **English**: [bootstrap_lite_en.md](../bootstrap_lite_en.md)
- **French**: [bootstrap_lite_fr.md](../bootstrap_lite_fr.md)

Files are at the **root** of the repository.

---

## 2. Where to use it

Paste the bootstrap into any text-based AI chat:

- ChatGPT ([chat.openai.com](https://chat.openai.com))
- Claude ([claude.ai](https://claude.ai) or in Cursor)
- Gemini ([gemini.google.com](https://gemini.google.com))
- DeepSeek ([chat.deepseek.com](https://chat.deepseek.com))
- Cursor / IDE assistant

No installation. Copy the full bootstrap → paste as first message → wait for *"PCL-Lite Bootstrap v1.0 Ready"*.

---

## 3. First steps

```bash
# List available personas
/persona list

# Activate one or more personas (e.g. Architect + Security)
/persona +ARCHI +SEC

# Assign a task
/persona task "Design a secure API for a banking app"

# Set who leads the response (optional)
/persona primary=SEC

# Get persona suggestions for a task
/persona suggest "audit our authentication flow"
```

---

## 4. Load a team

Instead of activating personas one by one, load a predefined team:

```bash
/persona team load security-review
/persona task "Review our auth design"
```

Other teams: `code-review`, `cloud-architects`, `infrastructure-team`, `observability-team`, `incident-response`, `data-team`, `documentation`, `architecture-review`, `leadership`.

---

## 5. Configure behavior

```bash
/persona depth=4 verbosity=2 risk=low
/persona merge=dissent    # show disagreements when multiple personas are active
/persona lang=fr          # response language
```

---

## 6. Presets

```bash
/persona preset startup    # MVP focus, less strict
/persona preset enterprise # Compliance, governance
```

---

## 7. Check status and reset

```bash
/persona status   # active personas, primary, merge mode, etc.
/persona clear    # deactivate all personas
/persona reset    # reset full state
```

---

[← Guides index](./README.md) · [Main README](../README.md)
