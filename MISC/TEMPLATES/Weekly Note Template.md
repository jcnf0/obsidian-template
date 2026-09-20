# <% tp.file.title %>
[[<% moment(tp.file.title,"YYYY-[W]ww").subtract(7, 'days').format("YYYY-[W]ww")%>]] <== This Week ==> [[<% moment(tp.file.title,"YYYY-[W]ww").add(7, 'days').format("YYYY-[W]ww")%>]]
`BUTTON[meeting]` `BUTTON[note]` `BUTTON[thought]` `BUTTON[reading]` `BUTTON[research-log]`

# Main Objectives

---
# Week Tasks
<%*
const FALLBACK_HEADINGS =
`## Meetings

## Research
### Reading

### Writing

### Experiments/Coding

## Perso
### Chores

### Hobbies

## Misc
`;

function extractHeadingsOnly(wtContent) {
  let skeleton = "";
  for (const rawLine of wtContent.split("\n")) {
    const h3 = rawLine.match(/^###\s+(.*)/);
    const h2 = !h3 ? rawLine.match(/^##\s+(.*)/) : null;
    if (h3) {
      skeleton += `\n### ${h3[1].trim()}\n`;
    } else if (h2) {
      skeleton += `\n## ${h2[1].trim()}\n`;
    }
  }
  return skeleton;
}

let wtContent = null;
try {
  const wtFile = tp.file.find_tfile("MISC/Weekly Tasks");
  if (wtFile) {
    wtContent = await app.vault.read(wtFile);
  }

  if (wtContent === null) {
    throw new Error("Weekly Tasks file not found");
  }

  const weekTitle = tp.file.title; // "YYYY-[W]ww"
  const weekStart = moment(weekTitle, "YYYY-[W]ww"); // Monday of that week
  if (!weekStart.isValid()) {
    throw new Error("Could not parse week from file title");
  }

  const dayAbbrs = ["mon","tue","wed","thu","fri","sat","sun"];
  const days = dayAbbrs.map((abbr, i) => {
    const d = weekStart.clone().add(i, "days");
    return { abbr, dateStr: d.format("YYYY-MM-DD") };
  });

  let output = "";
  for (const rawLine of wtContent.split("\n")) {
    const h3 = rawLine.match(/^###\s+(.*)/);
    const h2 = !h3 ? rawLine.match(/^##\s+(.*)/) : null;
    const taskMatch = rawLine.match(/^-\s+\[([ xX])\]\s+(.*)\|\s*(.*)/);

    if (h3) {
      output += `\n### ${h3[1].trim()}\n`;
    } else if (h2) {
      output += `\n## ${h2[1].trim()}\n`;
    } else if (taskMatch) {
      const taskBody = taskMatch[2].trim();
      const taskDays = taskMatch[3].split(",").map(d => d.trim().toLowerCase());
      for (const day of days) {
        if (taskDays.includes(day.abbr)) {
          output += `- [ ] ${taskBody} ⏳ ${day.dateStr}\n`;
        }
      }
    }
  }
  tR += output;
} catch (error) {
  // Tier 1 fallback: headings derived from Weekly Tasks.md, if it was readable
  if (wtContent !== null) {
    tR += extractHeadingsOnly(wtContent);
  } else {
    // Tier 2 fallback: hardcoded default skeleton, if Weekly Tasks.md itself was unreadable
    tR += FALLBACK_HEADINGS;
  }
}
%>

---
# Unscheduled
```tasks
(not done)
((due after <% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-[W]ww") %>) AND (due before <% tp.date.now("YYYY-MM-DD", 6, tp.file.title, "YYYY-[W]ww") %>)) OR (no due date)
((scheduled before <% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-[W]ww") %>) AND (scheduled after <% tp.date.now("YYYY-MM-DD", 6, tp.file.title, "YYYY-[W]ww") %>)) OR (no scheduled date) 
group by function task.due.category.groupText
limit 20
hide tags
hide due date
```