<%*
let title = await tp.system.prompt("Inbox title", null, true);
let proposed_path = await tp.system.prompt("Proposed vault path", "", false);
let agent = await tp.system.prompt("Originating agent", "", false);
let priority = await tp.system.suggester(
  ["Low", "Medium", "High", "Highest"],
  ["low", "medium", "high", "highest"],
  false,
  "Priority"
);
let source = await tp.system.prompt("Source", "", false);
let in_reply_to = await tp.system.prompt("OUTBOX wikilink (optional)", "", false);

priority = priority ?? "medium";
const yamlString = value => JSON.stringify(value ?? "");
const invalidChars = /[:\/\\*?"<>|]/g;
const created = tp.date.now("YYYY-MM-DD");
await tp.file.move("AGENTS/INBOX/" + title.replace(invalidChars, ""));
%>---
proposed_path: <% yamlString(proposed_path) %>
agent: <% yamlString(agent) %>
priority: <% priority %>
status: draft
created: <% created %>
modified: <% created %>
source: <% yamlString(source) %>
task_id: ""
in_reply_to: <% yamlString(in_reply_to) %>
---
# <% Title %>

## Summary

==What is being proposed or delivered?==

## Details


## Sources

