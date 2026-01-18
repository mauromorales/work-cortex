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
Turn this conversation into an understanding for my cortex.

Requirements:
- Create frontmatter with created and updated dates (today).
- Write a clear “Current understanding”.
- Add a “Context” section with an initial entry summarizing how this understanding emerged.
- Do not add new opinions beyond what appears in the conversation.
- Keep tone reflective, not authoritative.
- Use my voice
```
