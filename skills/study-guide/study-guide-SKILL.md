---
name: Study-Notes
description: Expand a basic study guide into an intensive, exam-ready reference document meant to be used live during a fully open-note/open-book exam. Trigger when the user uploads or pastes a study guide and asks to level it up, expand it, or make it more intensive for an exam.
---

# Exam Guide Intensifier

Takes a basic study guide and expands it into an intensive reference document built for one specific use case: sitting open on the desk (or laptop) during a fully open-note/open-book exam, where the user needs to find the right fact or worked example in seconds under time pressure.

This is not a study-practice tool — no quizzes, no flashcards, no timed drills. It is a reference-document upgrade. Think: "if I could only bring one document into this exam, what would make it as useful as possible?"

## When to Use This Skill

- The user uploads or pastes a basic study guide and asks to "level it up," "expand it," "make it more intensive," or "beef it up" for an exam
- The user mentions a fully open-note or open-book exam coming up and wants their existing notes turned into something more usable during the test
- The user wants a thin guide turned into a comprehensive reference they can rely on mid-exam

Do NOT use this skill for building quizzes, flashcards, or timed practice drills — that's a different kind of tool than what this produces.

## Instructions

**Step 1 — Read the source material.**
Read the user's uploaded/pasted basic study guide in full before doing anything else. If a file was mentioned but isn't actually in context, check `/mnt/user-data/uploads` for it (see the file-reading skill if needed for the format).

Identify:

- The subject and general class level (intro vs. advanced) from context clues in the guide itself
- Whether it skews **STEM** (formulas, derivations, code, problem sets) or **humanities/conceptual** (definitions, arguments, comparisons, case studies) — or a mix. This determines the shape of the expansion.
- The existing topic list/structure, since the expanded guide should track the same topics unless something is clearly missing and worth adding.

If the user hasn't said what the exam covers or how it's structured, don't stop to ask — infer from the guide and proceed. Only ask a clarifying question if the guide is too sparse to infer subject or scope at all.



**Step 2 — Supplement freely.**
The user wants outside knowledge pulled in, not just elaboration of what's already on the page. Freely add relevant course-level knowledge to fill gaps: standard definitions, related formulas, typical edge cases, context the original guide assumes but doesn't spell out. The goal is completeness — the expanded guide should stand on its own as the single best resource for the exam, not just a longer version of the original notes.

That said, stay grounded in what a real course at this level would actually cover — don't wander into material clearly outside the guide's scope or level.



**Step 3 — Structure the guide topic by topic.**
Organize by topic, mirroring the original guide's topic breakdown (adding topics only if something essential is clearly missing). For each topic, include, in this order:

1. **Definition** — tight, precise, quotable-under-pressure statement of what the thing is
2. **Explanation** — the deeper "why/how" a basic guide skips: mechanism, reasoning, derivation, or context that makes the definition make sense
3. **Example** — at least one worked example or concrete illustration
   - STEM topics: a fully worked problem showing each step
   - Humanities/conceptual topics: an applied example, case, or illustrative scenario
4. **Quick-reference summary** — a tightly compressed callout (bolded key terms, a short bullet list, or a mini-table) that's the thing the eye actually lands on when scanning mid-exam

Adapt the mix automatically based on what Step 1 determined:

- **STEM-heavy**: lean on formulas, step-by-step derivations, worked problems, unit/variable tables
- **Humanities-heavy**: lean on precise definitions, compare/contrast framing, key names/dates/arguments, illustrative examples
- **Mixed**: apply whichever pattern fits each individual topic rather than forcing one mode across the whole guide

Depth default: exhaustive, not concise. Go as deep as the material warrants — don't trim explanations or examples for the sake of brevity. Length is not a concern here; findability and completeness are.

**Step 4 — Add front matter.**
Before the topic sections, include:

1. **Table of contents / index** — every topic and subtopic listed with anchor-style headers, so the user can Ctrl+F or jump straight to what they need
2. **Formula / key-facts cheat sheet** — a single condensed block gathering every formula, key definition, date, name, or fact worth having in one glance, pulled from across all topics. This is the "first thing your eyes hit" summary — it should let the user answer easy/medium questions without ever leaving this section.

Do not include a "common mistakes" or pitfalls section — that's explicitly out of scope.



**Step 5 — Deliver as Markdown.**
Output as a `.md` file, not `.docx` or `.pdf` — the user wants something to Ctrl+F through on a laptop during the exam:

- Use clear, consistent heading levels (`#`, `##`, `###`) so document outline/navigation works in most editors
- Bold key terms so they pop on a scan
- Use tables for anything comparative or formula-heavy
- Keep topic headers exactly matching what's in the table of contents

Save the file to `/mnt/user-data/outputs/` and present it with `present_files`. Don't create it as `.docx` unless the user explicitly asks for Word instead — Markdown is the default.



**Step 6 — Sanity check before delivering.**
Before presenting the final file, confirm:

- Every topic from the original guide is represented and has all four sub-elements (definition, explanation, example, quick-reference)
- The front-matter cheat sheet actually contains high-value facts from every section, not just the first few topics
- Nothing from the original guide's content was silently dropped — expansion should never mean loss of information

## Examples

**Example 1 — STEM guide (intro physics)**
User uploads a one-page guide with bullet points like "F = ma", "Newton's 3 laws", "friction basics." The expanded guide would include: full definitions of each law, the reasoning behind why F=ma holds, worked example problems (e.g., calculating force given mass and acceleration, static vs. kinetic friction problems), a formula cheat sheet up top with F=ma, friction equations, and unit conventions, and a TOC linking to "Newton's Laws," "Force & Mass," "Friction."



**Example 2 — Humanities guide (intro sociology)**
User uploads a guide listing terms like "anomie," "structural functionalism," "Durkheim." The expanded guide would include: precise definitions of each theory/term, explanation of the historical/theoretical context (e.g., why Durkheim developed the concept of anomie), an applied example (a case study showing anomie in a real social context), a quick-reference summary contrasting functionalism vs. conflict theory, and a front-matter cheat sheet listing key theorists, terms, and one-line definitions.



**Example 3 — Mixed guide (intro economics)**
User uploads a guide covering both supply/demand graphs (STEM-leaning) and economic history/policy debates (humanities-leaning). The skill applies the formula/graph-heavy pattern to the supply/demand sections and the definition/comparison pattern to the policy sections, within the same document.