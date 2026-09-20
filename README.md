# Hritik Datta

Product and GTM at [Pre6.ai](https://pre6.ai). I work on enterprise AI: which customer workflow to start with, how to evaluate it, and whether the economics support deployment.

Previously, applied AI at Daimler and risk advisory at KPMG. I build prototypes to work through product decisions in code: how someone completes a task, what context an assistant needs, and how a team investigates a failure.

## Selected work

### [BolForm](https://github.com/Hritikd/Bolform) — voice to forms

Fill a form by speaking, review the answers, and download a PDF. Speaking language, screen language, and the form's language are separate choices.

One decision worth inspecting: validate a short answer directly when the current field is known; use a model for longer answers and corrections. Try an incomplete phone number and watch the form ask again.

[Live demo](https://bol-form-voice-form-assistant.replit.app) · [Build history and tradeoffs](https://github.com/Hritikd/Bolform/blob/main/docs/BUILD_STORY.md), including the work done with Replit Agent.

### [VyaparSaathi](https://github.com/Hritikd/VyaparSaathi) — merchant conversations

A Hindi/English assistant experiment using Groq-hosted Llama and Whisper. Compare onboarding a new merchant with answering an existing merchant using their account context.

[Walk through the example](https://github.com/Hritikd/VyaparSaathi#a-useful-demonstration) · [Inspect how context is assembled](https://github.com/Hritikd/VyaparSaathi/blob/main/app.py#L63). Uses fictional merchant records; no live merchant-system integration.

### [FieldKit](https://github.com/Hritikd/sarvam-fieldkit) — speech incident diagnosis

Turn one incident into a customer update and an engineering report. The example catches a missing order number that an aggregate transcription error rate does not explain on its own.

[Run the offline example](https://github.com/Hritikd/sarvam-fieldkit#try-it-in-a-minute) · [Read the diagnostic rules](https://github.com/Hritikd/sarvam-fieldkit/blob/main/src/fieldkit/diagnostics.py). The live adapter uses Sarvam; the example needs no API key.

[Website](https://hritikd.github.io) · [LinkedIn](https://www.linkedin.com/in/hritikdatta/) · [Email](mailto:hritikdatta2403@gmail.com)
