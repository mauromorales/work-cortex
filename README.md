# Cortex

This repository is a **cortex** — a place to externalize and evolve understanding over time.

It is not a source of truth, not a task system, and not a knowledge base.

Its purpose is to support sense-making: capturing ideas, forming understanding, observing how those understandings evolve, and tracking how they interact with the world.

---

## What this is

- A place to think deliberately
- A record of evolving understanding
- A reflection surface for ideas that return over time
- A lightweight system for learning from action and feedback

---

## What this is not

- A second brain
- A diary
- A todo list
- A documentation system
- A place to store everything

Only ideas with gravity belong here.

---

## AI collaboration

Cortex was designed to support collaboration with AI as a thinking aid. For this reason, the repository includes files such as `agents.md` and Copilot instructions that define how AI tools should behave when interacting with it. However, the use of AI is optional — the cortex can be used entirely without AI if preferred, with the same structure and intent.

---

## Structure

### `seeds/`
Raw ideas, questions, or intuitions.

Seeds are not beliefs and may never be resolved.
They exist only to capture something that feels worth revisiting.

---

### `understandings/`
Evolving understandings.

Each understanding:
- has a creation date
- represents how something is currently understood
- contains a historical record of how that understanding changed
- may include actions taken as a result of it

Understandings are allowed to change.
History should remain intact.

---

### `roles/`
Stable context about ongoing roles or activities.

These files describe **where** understanding is applied, not **what is believed**.

They should change slowly.

---

### `network/`
Context about people, communities, or organizations involved in collaboration.

This directory contains professional collaboration context only.
No private or sensitive information belongs here.

---

## How this is used

This cortex is meant to be used lightly.

- Not every thought belongs here.
- Not every idea needs to become an understanding.
- Silence and incompleteness are acceptable.

The value of this system comes from reflection over time, not completeness.

---

## Review

Periodically, understandings can be reviewed to reflect on:

- which ideas evolved
- which produced action
- which remained unchanged
- which can be archived

The goal is learning, not optimization.

---

## Agents

Rules for automated agents interacting with this repository are defined in [agents.md](./agents.md) and [copilot-instructions.md](./.github/copilot-instructions.md)

Agents must preserve meaning and history.

## Prompt

When interacting with a GPT in a conversation, you can use this prompt to generate an understanding:

```
From the content above, produce the distilled understanding that represents how I currently make sense of this topic.

The goal is to capture my post-discussion perspective — the way I would explain this to myself later, once the details of the conversation are forgotten.

Guidelines:
- Write strictly from my perspective (“I”).
- Keep the tone reflective, not authoritative.
- Preserve uncertainty, nuance, and incompleteness where they exist.
- Do not resolve open questions or smooth over ambiguity.
- Do not describe the discussion itself or how this understanding was formed.
- Do not introduce new opinions, conclusions, or interpretations.

Structure the output as:

created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: [relevant tags]

Current understanding:
(Describe how I currently think about the topic, including uncertainties or tensions if present.)

Context:
(Briefly describe what prompted or framed this understanding, without narrating the discussion.)

Actions:
(Leave empty unless explicit actions are provided.)

History:
(Leave empty unless explicit historical changes are provided.)

Notes:
(Optional reflections, implications, or directions to revisit later — not conclusions.)

Output requirements:
- Produce a single block of text suitable for pasting into a GitHub issue.
- Do not include explanations, commentary, or text outside the content itself.
```
