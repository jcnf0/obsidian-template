<%*
const invalidChars = /[:\/\\*?"<>|]/g;
const m = moment(tp.date.now("YYYY-MM-DD"), "YYYY-MM-DD");
const date = m.format("YYYY-MM-DD"); // Dataview sort field
const log_date_link = m.format("YYYY-MM-DD_ddd"); // Daily note link
const log_year = m.format("YYYY");
await tp.file.move(`RESEARCH/LOGS/${log_year}/${log_date_link} Research Log`);
%>---
type: log
daily_note: <% date %>
progress_rating:
summary:
projects:
tags:
  - TODO/WRITE
---
# <% log_date_link %> Research Log

## Progress
==How is progress looking so far?==

---
## Ideas

---
## Reading
==Any papers read?==

| Paper Note | Reading Depth    | Reason   |
| ---------- | ---------------- | -------- |
| ==PAPER==  | ==Skimmed/Full== | ==Why?== |


## Writing
==What section was written? Notes on the current framing of the paper?==

---
## Code
==Any code artifacts updated/created?==

## Experiments
==If there are any experiments==
```
### Experiment X
**Goal:** ==What is the objective of this experiment?==

**Method:** ==What are you doing? What is measured?**

**Results:** ====

**Data Considered:**

**Practical Considerations:**
*Resources:* ==What was used? (GPUs? VMs? Laptop?)==
*Cost:* ==How much?==
*Time:* ==How long?==

**Other Notes:** ==If Any==
```

---
## Next Steps
==What are the next actionables TODO? Experiments, Writing, Code, etc.==