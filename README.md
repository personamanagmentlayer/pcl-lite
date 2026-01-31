# PCL-Lite: Persona Control Language — Embedded Runtime

**PCL-Lite** is a lightweight, portable implementation of the *Persona Control Language* (PCL) protocol. It turns any AI chat session (ChatGPT, Claude, Gemini, DeepSeek) into a **multi-agent orchestration system** with no external infrastructure.

Inject it via a single bootstrap prompt to orchestrate, configure, and coordinate specialized personas directly in your conversation.

## Why PCL-Lite?

- **Instant multi-agent workflows** — Turn a linear chat into a structured collaborative session.
- **Zero setup** — Copy and paste the bootstrap into your preferred LLM. No installation required.
- **Structured collaboration** — Activate an *Architect* and a *Critic* at once for more robust outcomes.
- **Fine-grained control** — Adjust tone, verbosity, and response merge rules.

## Available bootstrap files

This repository provides bootstrap prompts tailored to context window size and use case:

### PCL-Lite "Lite" (recommended to get started)

A token-efficient bootstrap with everything needed to manage personas and simple workflows.

- **Best for**: Quick sessions, standard models (GPT-3.5, Haiku, Gemini Flash), prototyping.
- **Features**: Activation, CRUD, configuration (tone/verbosity), simple sequences, teams, presets.
- **Files**:
  - **English**: [bootstrap_lite_en.md](./bootstrap_lite_en.md)
  - **French**: [bootstrap_lite_fr.md](./bootstrap_lite_fr.md)

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
