<div align="center">

# 🌍 Hausa Prompt Engineering

### A professional linguist's guide to crafting better AI prompts in Hausa

*By Almustafa Emanuel Joseph-Alo — 15+ years professional Hausa translator & localiser*

[![Profile](https://img.shields.io/badge/GitHub-almustafa--ai-181717?style=flat&logo=github)](https://github.com/almustafa-ai)
[![Language](https://img.shields.io/badge/Language-Hausa-green?style=flat)](https://en.wikipedia.org/wiki/Hausa_language)
[![Focus](https://img.shields.io/badge/Focus-Prompt%20Engineering-blue?style=flat)](https://github.com/almustafa-ai/hausa-prompt-engineering)

</div>

---

## Why This Repository Exists

Most AI models struggle with Hausa — not because the technology cannot handle it, but because the people designing prompts for Hausa do not speak it professionally.

Hausa is spoken by **70+ million people** across Nigeria, Niger, Ghana, Sudan, and the diaspora. It has complex morphology, tonal distinctions that change meaning entirely, strict register differences between formal and colloquial usage, and deep cultural context that no machine has yet learned on its own.

This repository documents **what works, what fails, and why** — from the perspective of someone who has spent 15 years working with Hausa professionally as a translator, localiser, and language specialist.

Every prompt example here is:
- Tested against a live AI model
- Analysed linguistically for what changed and why
- Grounded in real professional translation experience
- Useful to NLP researchers, AI developers, and prompt engineers working with Hausa

---

## How to Read Each Example

Every prompt example follows this structure:
Domain        — the real-world context (formal writing, education, health, etc.)
Goal          — what we are trying to get the AI to produce
Bad prompt    — the vague or naive version most people would write
Bad output    — what the AI actually returns (and why it fails)
Refined prompt — the improved version with linguistic reasoning applied
Refined output — the significantly better result
What changed  — the linguistic and cultural reasoning behind the improvement

---

## Prompt Examples

---

### 001 — Formal Letter Writing in Hausa

**Domain:** Administrative and government correspondence
**Goal:** Generate a formal letter in Hausa appropriate for a Northern Nigerian government context

---

**❌ Bad Prompt:**
```
Write a letter in Hausa
```

**Bad Output (summarised):**
The AI produces a generic letter using casual, everyday Hausa — mixing in English loanwords freely, using informal address forms, and ignoring the structured conventions of formal Hausa administrative writing. The result would be inappropriate and unprofessional in any real government or institutional context.

**Why it fails:**
- No register specified — AI defaults to colloquial Hausa
- No audience defined — formal and informal Hausa are structurally different
- No cultural framing — Northern Nigerian administrative writing has specific conventions
- Loanwords are used where native Hausa equivalents are expected in formal contexts

---

**✅ Refined Prompt:**
```
Write a formal letter in Hausa addressed to a local government chairman 
requesting road repairs in a residential area. 

Requirements:
- Use formal written Hausa (Hausa na hukuma), not colloquial speech
- Use the appropriate respectful address: "Malam Shugaban Majalisar Gunduma"
- Avoid English loanwords where native Hausa equivalents exist
- Follow the standard structure: greeting, purpose, supporting details, request, closing
- The tone should be respectful and deferential, as is culturally expected 
  when addressing a senior official in Northern Nigerian context
- Close with "Allah ya kiyaye ku" or equivalent formal closing
```

**Refined Output (summarised):**
The AI now produces a properly structured formal letter with correct honorifics, appropriate register, native Hausa vocabulary in place of loanwords, and the deferential tone expected in Northern Nigerian institutional correspondence. The result is usable in a real administrative context.

**What changed — linguistic reasoning:**
| Element | Bad prompt result | Refined prompt result |
|---|---|---|
| Register | Colloquial (zance na yau da kullum) | Formal (hukuma) |
| Address form | Generic / missing | Correct honorific title |
| Vocabulary | Loanword-heavy | Native Hausa prioritised |
| Structure | Freeform | Standard administrative format |
| Tone | Neutral | Appropriately deferential |
| Closing | Missing or generic | Culturally appropriate |

**Key insight:** In Hausa, register is not just about word choice — it changes sentence structure, verb forms, and the entire social framing of communication. An AI that does not know this will always produce output that feels wrong to a native speaker, even if it is technically grammatical.

---

### 002 — Health Communication for Rural Hausa Communities

**Domain:** Public health messaging
**Goal:** Generate accessible health information about malaria prevention for a rural Hausa-speaking audience

---

**❌ Bad Prompt:**
```
Explain malaria prevention in Hausa
```

**Bad Output (summarised):**
The AI produces a medically accurate but culturally disconnected explanation. It uses clinical terminology translated literally into Hausa, references behaviour patterns that do not reflect rural Northern Nigerian life, and ignores the role of community and religious framing that makes health messages trusted and adopted in this context.

**Why it fails:**
- "Rural" vs "urban" Hausa audience requires different vocabulary and references
- Clinical terms like "mosquito net" become awkward transliterations instead of the familiar local term (sauro/gidan sauro)
- No acknowledgement of the role of Islamic framing in making health messages credible
- Assumes a literate, individually-oriented audience rather than a community-oriented one
---

**✅ Refined Prompt:**
```
Write a malaria prevention message in Hausa for a rural farming community
in Kano State, Nigeria.
Requirements:

Target audience: adult farmers and mothers with low formal education
Use simple, everyday Hausa vocabulary — not clinical or technical terms
Use the local word "sauro" for mosquito, not transliterations
Reference familiar daily routines (sleeping, farming hours, market days)
Include one brief Islamic reference for credibility
(e.g. "lafiya amana ce daga Allah" — health is a trust from God)
Keep sentences short — this may be read aloud by a community health worker
Avoid bullet points in the output — write as natural spoken Hausa
Length: approximately 100 words
```


**Refined Output (summarised):**
The AI now produces a warm, accessible message using familiar vocabulary, local references, appropriate Islamic framing, and a conversational tone suited for oral delivery. A community health worker could read this aloud and it would be understood, trusted, and acted upon.

**What changed — linguistic reasoning:**
The critical shift here is audience modelling. Hausa is not one monolithic variety — the Hausa of an educated Abuja professional is significantly different from the Hausa of a Kano farmer. Prompts that ignore this distinction produce output that is technically Hausa but practically useless for the intended audience. Specifying occupation, location, education level, and delivery method transformed the output completely.

**Key insight:** Cultural credibility markers (Islamic references, community-oriented framing) are not optional decoration in Hausa health communication — they are the mechanism by which the message earns trust. An AI that does not know this will produce messages that are ignored.

---

### 003 — News Writing and Journalistic Hausa

**Domain:** Media and journalism
**Goal:** Generate a news report opening paragraph in Hausa suitable for radio broadcast

---

**❌ Bad Prompt:**
```
Write a news story in Hausa about flooding in Maiduguri
```

**Bad Output (summarised):**
The AI produces text that reads like a translated English news story — passive constructions, inverted pyramid structure borrowed from Western journalism, and vocabulary that reflects print media conventions rather than the oral, direct style of Hausa radio broadcasting (particularly the BBC Hausa Service or VOA Hausa style that listeners recognise and trust).

**Why it fails:**
- Hausa radio journalism has a distinct style — direct, active, community-centred
- The AI defaults to translating English news conventions rather than applying Hausa journalistic norms
- No specification of broadcast medium — print and radio Hausa are structurally different
- Maiduguri-specific context (Lake Chad region, displacement history) is ignored

---

**✅ Refined Prompt:**
```
Write the opening paragraph of a radio news report in Hausa about flooding
in Maiduguri, Borno State.
Requirements:

Style: BBC Hausa Service broadcast style — direct, clear, active voice
Open with the most important fact first (who was affected, how many, where)
Use active sentence construction — avoid passive voice which sounds unnatural
in spoken Hausa news
Reference "mazauna Maiduguri" (residents of Maiduguri) not abstract "victims"
Mention Borno State by full name on first reference
Tone: serious and factual, with appropriate empathy — not sensationalist
Length: 60–80 words, suitable for reading in approximately 30 seconds
This will be read aloud — prioritise rhythm and natural spoken cadence
```


**Refined Output (summarised):**
The AI now produces an opening paragraph that matches the BBC Hausa Service's recognisable style — direct, human-centred, appropriately paced for oral delivery, and grounded in the specific regional context. A Hausa radio journalist could use this as a strong draft starting point.

**What changed — linguistic reasoning:**
Hausa has a rich oral tradition and its broadcast journalism reflects this — rhythm, directness, and community framing matter enormously. The key prompt additions were: specifying the broadcast model (BBC Hausa), requiring active voice, naming the community members as people rather than abstractions, and noting that the output would be read aloud. Each of these constraints pushed the AI away from translated-English conventions and toward authentic Hausa journalistic voice.

**Key insight:** Specifying a reference style (BBC Hausa, VOA Hausa) gives the AI a concrete model to emulate. Without this anchor, it defaults to whatever English-language journalism pattern dominates its training data.

---

## Skills Demonstrated in This Repository

```text
Prompt Engineering     Systematic refinement with measurable improvement criteria
Hausa Linguistics      Register, morphology, tone, dialectal variation, oral vs written
Cultural Analysis      Community framing, religious context, regional specificity
AI Evaluation          Identifying failure modes in multilingual AI output
Technical Writing      Clear documentation of complex linguistic reasoning
NLP Research           Practical contribution to low-resource language AI improvement
```

---

## About the Author

**Almustafa Emanuel Joseph-Alo** is a professional Hausa and French translator and localiser with 15+ years of experience, now working at the intersection of African language expertise and artificial intelligence.

- 🌍 GitHub: [almustafa-ai](https://github.com/almustafa-ai)
- 📧 Contact: almustafa.josephalo@gmail.com
- 🤝 Open to: NLP research collaboration, AI technical writing, Hausa language consulting

---

## Contributing & Collaboration

Are you an NLP researcher, AI developer, or linguist working on Hausa or other African languages? I welcome collaboration — open an issue, start a discussion, or reach out directly.

*More prompt examples added regularly across domains: education, legal, agriculture, commerce, and storytelling.*
