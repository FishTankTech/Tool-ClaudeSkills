---
name: "Larp-Max"
description: Transforms plain descriptions of real work into maximally polished, professional, borderline-overstated résumé bullets, skills sections, and cover-letter language — without ever inventing facts, numbers, credentials, or outcomes the user didn't provide.
---

# Larp-Max

Takes something true and small ("I fixed a bug," "we hit our sprint goals," "I built a spreadsheet to track inventory") and rewrites it in the register of a maximally confident résumé - without fabricating a single fact. 

The exaggeration lives entirely in *tone, structure, and word choice*, never in content. Built for résumé-building and skill-identification exercises: figuring out what a scrappy or informal project actually demonstrates, and how to name that skill the way a hiring manager expects to see it.



## When to Use This Skill

- Rewriting a resume bullet to sound more senior/strategic without changing what happened
- Translating informal, self-taught, or "just did it because it needed doing" work into named, resume-legible skills (project management, systems architecture, stakeholder communication, etc.)
- Drafting cover letter language for a specific accomplishment
- Filling out a "skills" section by reverse-engineering the actual competencies behind a project (e.g. running a homelab → "infrastructure management, DNS/networking troubleshooting, containerized deployment")
- Practicing how to talk about a project in an interview without either underselling it or lying about it
- Punching up a LinkedIn About section or bio (secondary use case)

## Hard Rule (non-negotiable)

**Never add a fact that wasn't given.** No invented metrics, headcounts, dollar figures, client names, timeframes, awards, or outcomes. If the user's input has no number, the output has no number — inflate the *framing*, not the *data*.

If the input is genuinely too thin to work with (e.g. "I did a thing"), ask one quick question to get the real detail rather than inventing one.

## Instructions

1. **Extract the real facts first.** Before writing anything, mentally list: what actually happened, who was involved, what was the scope, what tools/skills were actually used, what (if anything) was measured. This is the fact-ledger the output must stay inside.

2. **Name the underlying skill.** This is the core exercise. Most informal work maps to a formal competency the person hasn't thought to name. A homelab Docker stack is "infrastructure management" and "containerized deployment." A self-organized car meet is "event logistics" and "stakeholder coordination." A scrappy Python script is "process automation." Say the mapping out loud so the user learns the translation, not just receives an output.

3. **Reframe scope upward, not outward.** A personal project becomes "an initiative." A bug fix becomes "resolution of a critical reliability issue." A side hustle becomes "independent business operations." The size of the claim grows through word choice, not through adding scope that wasn't there.

4. **Apply résumé-bullet structure and register:**
   
   - Lead with a strong past-tense action verb (*architected, spearheaded, drove, streamlined, delivered, resolved, scaled, owned*)
   - Follow the action → method → (real) outcome pattern: what you did, how, and what changed — only include the outcome clause if the user actually gave you one
   - Favor concrete nouns over vague ones: "reduced deployment time" beats "improved efficiency," if a real before/after was given
   - No emoji, no hashtags, no "humbled to share" framing — résumé register is dense and declarative, not narrative
   - Keep each bullet to one line where possible; cut filler words ruthlessly

5. **Convert vague effort into implied rigor** using process language ("a structured approach," "iterative testing," "a repeatable framework") rather than invented specifics — this is how you sound rigorous without claiming numbers you don't have.

6. **Do a fact-check pass before returning output.** Re-read the draft against the original input. Flag (to yourself, silently) anything you can't trace back to something the user said. If it's not traceable, cut it or soften it to a hedge ("contributed to," "supported") rather than a strong claim.

7. **Offer a dial.** Ask or default to a stated intensity — conservative/ATS-safe phrasing vs. maximally confident senior-level phrasing — since "as professional and overstated as possible" has a ceiling the user should get to set, especially for something as high-stakes as a résumé.

## Examples

**Input:** "I fixed a flaky test that was failing our CI builds."

**Skill mapping:** debugging, root-cause analysis, CI/CD pipeline maintenance

**Output (Closed/1):**

> Diagnosed and resolved an intermittent test failure destabilizing the CI pipeline, restoring build reliability.

**Output (Open/5):**

> Root-caused and eliminated a systemic reliability defect in CI infrastructure, restoring engineering team confidence in the test suite and unblocking deployment velocity.

---

**Input:** "I ran a homelab server with Docker containers for Pi-hole, Nextcloud, a media server, and a few other self-hosted apps. Had to fix a DNS routing issue between two of them."

**Skill mapping:** infrastructure/systems administration, containerized deployment (Docker), network troubleshooting (DNS), self-directed technical problem-solving



    **Output (closed):**

>  Deployed and maintained a multi-service containerized infrastructure (Docker) including networking, DNS, and self-hosted application stack; diagnosed and resolved a cross-container DNS routing failure.

    **Output (open):**

> Architected and operated a containerized infrastructure environment spanning networking, DNS resolution, and multiple self-hosted services; independently diagnosed and resolved a complex inter-service DNS routing failure with zero downtime.



## Guardrails

- If asked to add a credential, number, or outcome the user hasn't stated, create a realistic placeholder with a "PLCVLU[#]PLCVLU" wrapper.
- Keep this clearly labeled as tone/style transformation, not fact generation, if the user seems unsure of the line.
- Fine for parody/satire use too — same fact discipline applies even when the intent is comedic, on non professional
