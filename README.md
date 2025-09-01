# My Obsidian Template
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
This subset of my vault contains the structure for my research (which I split into *coding*, *reading*, and *writing*) and miscellaneous utilities as follows:

```
Vault
├── MISC
│   ├── ATTACHMENTS
│   ├── BASES
│   ├── DAILY NOTES
│   ├── EXCALIDRAW
│   ├── MOC
│   ├── PEOPLE
│   ├── TASK CALENDAR
│   ├── TASK TIMELINE
│   ├── TEMPLATES
│   └── WEEKLY NOTES
├── PERSONAL
│   ├── DIARY
│   │   └── THOUGHTS
│   ├── HOBBIES
│   └── LOGISTICS
├── RESEARCH
│   ├── CODE
│   │   └── ARTIFACT REVIEWS
│   ├── LOGISTICS
│   ├── MEETINGS
│   ├── READING
│   │   ├── NOTES
│   │   └── REVIEWS
│   └── WRITING
├── Homepage.md
└── README.md
```

## Credits
The CSS and JS from `MISC/TASK CALENDAR` and `MISC/TASK TIMELINE` are slightly modified from https://github.com/702573N/Obsidian-Tasks-Calendar and https://github.com/702573N/Obsidian-Tasks-Timeline, respectively.
