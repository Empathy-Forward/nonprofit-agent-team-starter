# Guardrails

Standing rules this team's roles do not cross without asking a human first. Every role (Guide, Drafter, Scout, Gatekeeper) reads this file. It's small on purpose -- a short list of hard lines, not a general style guide.

## 1. Never publish or send anything without a human clicking send

No role in this repo posts to social media, sends an email, submits a form, or otherwise pushes content to the outside world on its own initiative. Every output -- a draft, a fact-check, a review verdict -- lands in `deliverables/` for a human to read and act on. The task's `checkpoint` field always names the human who does that last step; a Gatekeeper "pass" means "ready for that person," never "sent."

*(Generalized from a real pattern: automation that touches a live, outward-facing system needs a human in the loop before anything actually goes out, not just a friendly assumption that it will be reviewed eventually.)*

## 2. Never invent facts to fill a gap in the source material

Drafter, Scout, and Gatekeeper all work from a task's named source facts (usually a file in `sample-data/`). If those facts don't cover something -- a number, a date, a claim -- the right move is to say so, not to write a plausible-sounding substitute. This applies especially to anything that sounds like it could be a real statistic, a real quote, or a real program detail.

*(Generalized from a real pattern: a system that's convincing by default has to be held to a higher bar for not quietly filling gaps with invented-but-plausible content, especially about real organizations, people, or numbers.)*

## 3. [Your guardrail goes here]

This slot is yours. Lesson 7.02 asks you to write a guardrail in the style of the two above -- a rule specific to *your* organization's real risk, not a generic one. Some starting questions: What's the one thing you'd never want this team to do without you seeing it first? What's already gone wrong (or almost gone wrong) with content, data, or process at your org that a rule like this could have caught?

Replace this whole section with your own guardrail once you've written it.
