# Copilot Instructions for Cortex

This repository is a **cortex** used for sense-making.

Follow these instructions when assisting in this repository.

---

## General behavior

- Be conservative.
- Prefer preserving existing content over rewriting.
- Do not introduce new beliefs, opinions, or conclusions.
- Do not infer intent that is not explicitly written.
- Ask for clarification when unsure.

---

## File creation

When asked to create files:

- Place files only in these directories:
  - `seeds/`
  - `understandings/`
  - `roles/`
  - `network/`

- Do not create new top-level directories unless explicitly instructed.

---

## Understandings

When creating or updating files under `understandings/`:

- Always include frontmatter.
- Set `created` and `updated` dates to today unless provided.
- Do not invent tags or actions.
- Use empty arrays when none are provided.

Structure must follow this order:
1. Current understanding
2. Historical record
3. Notes (optional)

Historical record rules:
- Append only.
- Never rewrite or delete past entries.
- Do not collapse history into a single narrative.

---

## Issues → files

When asked to convert an issue into a file:

- Extract content from the issue only.
- Do not add new reasoning.
- Do not improve arguments.
- Preserve the author’s wording as much as possible.
- Rephrase only for clarity, not strength.

---

## Seeds

When creating seed files:

- Treat seeds as raw ideas.
- Do not resolve or conclude.
- Do not promote seeds to understandings unless explicitly requested.

---

## Roles and Network

When creating files under `roles/` or `network/`:

- Capture context only.
- Avoid opinions or interpretations.
- Do not speculate.
- Do not include private or sensitive information.

---

## Default rule

If a request would require guessing, inventing, or completing missing meaning:

- Stop.
- Ask for clarification.
