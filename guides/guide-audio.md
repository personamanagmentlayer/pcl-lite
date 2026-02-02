# Guide — PCL-Lite Audio

How to use the **PCL-Lite Audio bootstrap** (personas for podcast, voiceover, sound design, transcripts) in any AI chat.

---

## Objective: get script & structure, then generate (same chat or external)

PCL-Lite Audio gives you **scripts, episode structure, transcript strategy, sound-design notes** in the chat. What you do next depends on your AI:

- **If your AI can generate audio** (e.g. ChatGPT with voice read-out, Gemini with audio, or any multimodal chat with TTS/voice): use the **script in the same chat** — paste it into the voice/audio feature so the AI reads or generates from it. PCL-Lite helps you get a clear script and structure.
- **If your AI doesn’t generate audio**: **copy** the script and **paste** it into one of the tools below (ElevenLabs, Descript, Murf, etc.).

---

## Workflow

1. **In your chat**: Paste the PCL-Lite Audio bootstrap → use `/persona` commands → ask for a script, episode outline, or transcript strategy (e.g. 30min podcast, voiceover script).
2. **Get the output**: The chat returns **ready-to-use text** (script, segment list, speaker labels, transcript notes).
3. **Multimodal AI**: Use that **script in the audio/voice feature of the same chat** (e.g. “Read aloud”, TTS, or future audio gen) if it has one.
4. **Or copy-paste**: **Copy** the script and **paste** it into one of the tools below (ElevenLabs, Descript, Murf, etc.) if your chat doesn’t generate audio.

---

## Where to generate audio

**Multimodal AI:** If your chat can generate or read audio (e.g. ChatGPT “Read aloud”, TTS, or voice features), paste the script **in the same chat**. Otherwise use one of the tools below:

| Tool | Link | Use case — what to copy-paste |
|------|------|------------------------------|
| **ElevenLabs** | [elevenlabs.io](https://elevenlabs.io) | Text-to-speech / voiceover. **Paste your script** into the text box and generate voice. |
| **Descript** | [descript.com](https://descript.com) | Podcast/video edit + voice. **Paste script** for voiceover or Overdub; use episode structure for segments. |
| **Murf** | [murf.ai](https://murf.ai) | Voiceover from text. **Paste your script** and choose voice; export audio. |
| **Adobe Podcast** | [podcast.adobe.com](https://podcast.adobe.com) | Enhance speech + simple edit. **Paste or record**; use script for captions/structure. |
| **Audacity** | [audacityteam.org](https://www.audacityteam.org) | Free edit (no AI voice). Use **script** as reference for cutting and ordering; use transcript for captions. |
| **CapCut** (voice) | [capcut.com](https://www.capcut.com) | Add AI voice to video. **Paste script** into the text-to-speech / caption tool. |
| **ChatGPT** (voice read-out) | [chat.openai.com](https://chat.openai.com) | Read script aloud (mobile). Copy script into ChatGPT and use “Read aloud” if you need a quick listen. |

**Tip:** If the chat gave you **duration, format, platform** (e.g. 30m, mp3, podcast), set those in the tool when exporting.

---

## 1. Get the bootstrap

All Audio bootstraps are in the **[`bootstrap-audio/`](../bootstrap-audio/)** folder:

- **English**: [bootstrap_lite_audio_en.md](../bootstrap-audio/bootstrap_lite_audio_en.md)
- **French**: [bootstrap_lite_audio_fr.md](../bootstrap-audio/bootstrap_lite_audio_fr.md)

---

## 2. Where to use PCL-Lite

Paste the bootstrap into any AI chat (ChatGPT, Claude, Gemini, DeepSeek, Cursor). The chat gives you **scripts, specs, and recommendations**. If the chat **can generate or read audio** (e.g. ChatGPT “Read aloud”, or TTS/voice features), use that script in the same chat; otherwise copy it and paste into one of the tools above.

**Test flow:** Open the bootstrap file → copy full content → paste as first message → wait for *"PCL-Lite Audio v1.0 Ready"* → send `/persona` commands and tasks.

---

## 3. First steps

```bash
# List audio personas
/persona list

# Activate personas (e.g. Script + Accessibility)
/persona +SCRIPT_AUDIO +A11Y_AUDIO

# Set audio context (optional)
/persona audio duration=30m format=mp3 platform=podcast

# Ask for a script outline
/persona task "Outline a 30min podcast episode: intro, 3 segments, outro. Include transcript strategy."
```

---

## 4. Audio context

Set once; active personas use it for their answers:

```bash
/persona audio duration=30m   # or 5m, 1h
/persona audio format=mp3     # or wav, aac
/persona audio platform=podcast  # or youtube, spotify, web
/persona audio clear          # clear context
```

---

## 5. Load a team

```bash
/persona team load podcast-production
/persona audio duration=20m platform=podcast
/persona task "Script for a 20min interview episode: host intro, 5 questions, guest flow, outro and CTA."
```

Teams: `podcast-production`, `accessibility-audio`, `sound-design-team`, `full-audio-production`, `interview-team`, `technical-delivery-audio`.

---

## 6. Workflow (sequential)

```bash
/persona +SCRIPT_AUDIO +EDITOR_AUDIO
/persona workflow SCRIPT_AUDIO -> EDITOR_AUDIO
/persona task "Draft script for a 15min voiceover, then suggest edit structure: pacing, cuts, levels."
```

---

## 7. Check status and reset

```bash
/persona status       # active personas, audio context
/persona audio clear  # clear audio context
/persona clear        # deactivate all personas
```

---

[← Guides index](./README.md) · [Main README](../README.md)
