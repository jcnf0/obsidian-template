# My Obsidian Template (by Jean-Charles Noirot Ferrand)
This repository contains the current structure, plugins, and settings of my Obsidian vault. It is meant to be a starting place to recreate a vault and a way for me to organize my own vault. For more details about the vault and how I use it, I encourage you to read my [blog post](https://jcnf.me/posts/my_obsidian_setup.html).

> **Note:** The structure of my vault is constantly refined as I see fit. I took inspiration from files and configurations that I've seen and assembled them in a way that makes sense for me, but there might be better ways to organize your own vault depending on profile.

## Installation
You can clone and remove the `git` files with:

```
git clone https://github.com/jcnf0/obsidian-template.git
rm -rf .git
find . -name ".gitkeep" -delete
```

## The Vault
### Structure
This subset of my vault contains the structure for my research (which I split into *coding*, *reading*, and *writing*), personal notes, and miscellaneous utilities as follows:

```
Vault
├── AGENTS               # agent inbox/outbox
│   ├── INBOX
│   └── OUTBOX
├── CLASSES              # course notes
├── MISC
│   ├── AFFILIATIONS
│   │   ├── COMPANIES
│   │   └── UNIVERSITIES
│   ├── ATTACHMENTS
│   │   └── BANNERS
│   ├── BASES            # Obsidian Bases views
│   ├── CLIPPINGS
│   ├── COPILOT
│   ├── DAILY NOTES
│   ├── EVENTS
│   │   ├── PHD
│   │   └── VENUES
│   ├── EXCALIDRAW
│   ├── PEOPLE
│   ├── PLANNING AND REVIEW
│   ├── TEMPLATES
│   ├── WEEKLY NOTES
│   ├── TAGSONOMY.md     # the tag authority
│   └── Weekly Tasks.md  # recurring-task scaffold
├── PERSONAL
│   ├── HOBBIES
│   │   ├── GAME DEVELOPMENT
│   │   ├── HOMELAB
│   │   └── STYLING
│   ├── LOGISTICS
│   ├── LOGS
│   ├── READING
│   │   ├── BOOKS
│   │   └── OTHER
│   └── WRITING
│       ├── OTHER
│       └── THOUGHTS
├── RESEARCH
│   ├── CODE
│   │   └── ARTIFACT REVIEWS
│   ├── LOGISTICS
│   ├── LOGS
│   ├── MEETINGS
│   ├── PROJECTS
│   │   └── IDEA
│   ├── READING
│   │   ├── OTHER
│   │   ├── PAPERS
│   │   ├── REVIEWS
│   │   └── SPECIFICATIONS
│   └── WRITING
│       ├── Fellowships
│       ├── Grants
│       ├── Guides
│       └── THOUGHTS
├── AGENTS.md            # agent workflow
├── Homepage.canvas
└── README.md
```

### Agent Setup
`AGENTS.md` defines a lightweight, generalized agent workflow you can adapt or delete — rename the example agent roles/tags and adjust the conventions to your own setup.

Agents exchange work through `AGENTS/OUTBOX/` (requests you send to agents) and `AGENTS/INBOX/` (drafts agents return for your review), using the Outbox/Inbox templates and the `INBOX.base` review queue. See `AGENTS.md` for the full convention.

> **Note:** Secrets are never committed. Plugin data for LiveSync, Local REST API, and Whisper is intentionally excluded — configure those locally after cloning.
