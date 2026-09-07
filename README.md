# nonprofit-agent-team-starter

A small, ready-to-run AI agent team for a nonprofit -- one orchestrator and three specialist roles, built to hand off a real first task (drafting a short piece of content from a set of source facts) with a human checkpoint at the end, not a black box that publishes on its own.

> Built on the myPKA(TM) Scaffold by Paperless Movement(R) / ICOR(R).
> Source: https://github.com/myICOR/myPKA
> Licensed under CC BY-SA 4.0.
>
> Not an official myPKA product; not affiliated with or endorsed by myICOR or Paperless Movement S.L.

See `NOTICE` and `LICENSE-MAP.md` for the full attribution and per-subtree license detail. This repository as a whole is licensed CC BY-SA 4.0 -- see `LICENSE`.

## What this is

Four roles, in one repo, each with a plain-text contract an LLM can read and follow:

| Name | Role | Purpose |
|---|---|---|
| **Guide** | Orchestrator | Routes work to the right specialist, never drafts or reviews itself |
| **Drafter** | Content writer | First-draft pass on a factual brief (blurb, note, post) |
| **Scout** | Fact-checker / researcher | Checks a draft's claims against the brief's source facts |
| **Gatekeeper** | Reviewer / quality gate | Pass/fail call against the brief's "good enough" standard, before a human signs off |

Every output lands in `deliverables/` for a human to read and act on. No role in this repo posts, sends, or publishes anything on its own -- see `governance/guardrails.md` for the standing rules behind that.

That human checkpoint is, by default, you -- the person directing this team. This is a single-person AI team, not a shared org-wide one, so the reviewer a task's `checkpoint` field names is, by default, whoever is running the repo, not a separate coworker or organizational role. An organization can still layer its own additional sign-off on top (an ED or comms director doing a further review before something goes out under the org's name) -- that's a legitimate extra step some setups add, never the assumed default here.

This repo works the same way whether you found it on its own or you're taking the course it pairs with (see below). It's meant to be genuinely useful past a single sitting -- clone it, point an AI coding assistant (Claude Code, or anything else that reads a root `AGENTS.md`) at the folder, and use it for your own organization's real first task.

## Getting started

1. Clone this repository and open it in an AI coding assistant that reads `AGENTS.md` (Claude Code, or similar).
2. Point the assistant at the repo and let it read the root `AGENTS.md`. On a first run, it will ask you three quick questions (your name, your organization's name and mission, and what kind of task you're hoping to eventually hand off) and save the answers locally to `.profile.yaml` -- this file never leaves your machine and is gitignored.
3. Work through the starter sample task first: `tasks/starter-task-nonprofit-blurb.md`, a safe, fully worked example using a fictional organization (`sample-data/fictional-nonprofit-facts.md`). Watch the team go Drafter -> Scout -> Gatekeeper, and see what a first draft gets wrong before a human (you) catches it.
4. Copy `tasks/_template.md` (already personalized with your organization's name and mission once onboarding has run) into a new file under `tasks/` for your own real task.

If Claude Code (or your assistant) supports dispatching subagents in parallel, each specialist is also directly runnable via its shim in `.claude/agents/` -- `drafter`, `scout`, `gatekeeper`. Running a specialist directly without going through Guide first works fine; it just won't have your name or org context until you've run onboarding once.

## The roster, and why it's generic

Guide, Drafter, Scout, and Gatekeeper are deliberately generic names, not a specific product's cast of characters -- this is your team, and the four roles here are a floor, not a ceiling. See the "Adding a new role" section of the root `AGENTS.md` for how to add a fifth role suited to your own organization's actual gap (a donor-outreach specialist, an editor, a scheduler -- whatever you actually need).

## If you're taking the paired course

If you're taking Empathy Forward's "AI Agent Teams for Nonprofits" course, this repository is the Lesson 6-7 hands-on starter -- Lesson 6 walks through running the starter sample task end to end, and Lesson 7 has you write your own guardrail (there's a marked slot waiting for it in `governance/guardrails.md`) and set up your own real task. That said, nothing in this repository requires the course -- everything above works the same whether or not you've ever heard of it.

## License

CC BY-SA 4.0 for the whole repository. See `LICENSE`, `NOTICE`, and `LICENSE-MAP.md` for the full detail, including which parts are adapted from the myPKA Scaffold's pattern and which are original to this course.
