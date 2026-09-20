# Agent Workflow

## Agent Roles

Define one tag per agent and have each agent add its tag to notes it touches. Rename these to suit your setup — example roles:

- `#AGENT/<HOME>`: home management and personal notes
- `#AGENT/<INFRA>`: infrastructure and orchestration
- `#AGENT/<RESEARCH>`: research and paper analysis

Every agent adds its agent tag to notes it touches.

## Inbox / Outbox

Requests to agents and their responses flow through two folders, so nothing lands in the vault without review:

- `AGENTS/OUTBOX/` — **requests you send to agents.** Create one with the Outbox template: a `Request`, `Context`, and `Acceptance Criteria`, plus `priority`, optional `assignee`, and `status` (starts `new`). This is the queue an agent reads from.
- `AGENTS/INBOX/` — **drafts and proposals agents return to you.** An agent responds with the Inbox template instead of editing the target note directly: `Summary`, `Details`, and `Sources`, plus a `proposed_path` (where the note should land once approved), the originating `agent`, `status` (starts `draft`), and `in_reply_to` (a wikilink back to the originating OUTBOX request). Review it, then move it to its `proposed_path` if you accept it.

Keep the round trip traceable by linking each response to its request via `in_reply_to` / `task_id`. The `INBOX.base` view lists pending inbox items by agent, priority, and status.

## Before Writing

1. Read the target note completely enough to understand its populated sections.
2. Read the applicable template at runtime and use its current headings and fields; ignore Templater blocks when reproducing structure.
3. Check `MISC/TAGSONOMY.md` before adding tags.
4. Check whether the target already exists or whether the relevant section is populated.
5. Ask before creating notes or replacing populated content. Task insertions may proceed only when heading, date, description, and any required priority are unambiguous.

## Writing Rules

- Patch existing notes in place; create new files only for genuinely new notes.
- Insert tasks under the matching weekly heading, not at end-of-file.
- Preserve frontmatter order, blank fields, wikilinks, callouts, Dataview/Tasks blocks, and existing prose unless the requested operation changes them.
- Never edit templates, `.obsidian/`, or unrelated sections.
- Never create a daily or weekly note if it is missing; report it instead.
- Never assign `#PAPER/*`; use only taxonomy-approved tags.
- Do not overwrite a populated meeting section or research log without asking.

## Standard Workflows

### Tasks

Use the current weekly note's actual headings. The active hierarchy is generally `Meetings`; `Research` → `Reading`, `Writing`, `Experiments/Coding`; `Perso`; `Chores`; `Hobbies`; `Homelab`; and `Misc`. Use the existing note rather than assuming every heading is present.

### Meetings

Preserve `## Transcript`, `## Agenda`, and `## Materials`. Synthesize `## Notes`, `## Action Items`, and `## AI Summary`; update only the intended `summary` frontmatter and agent tag.

### Research Logs

Use the current research-log template. Leave `progress_rating` blank when present. Do not overwrite an existing log without asking.

### Vault Learning

Use recurring patterns across notes as evidence, but distinguish observed conventions from rules explicitly stated in `AGENTS.md` or `MISC/TAGSONOMY.md`. If they conflict, flag the conflict rather than silently choosing.

## Uncertainty Protocol

If unsure, ask numbered questions covering the exact target note/path, section, intended change, date, links, tags, and whether existing content may be replaced. Do not write until the ambiguity is resolved.
