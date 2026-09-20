<%*
let title = await tp.system.prompt("Request title", null, true);
let priority = await tp.system.suggester(
  ["Low", "Medium", "High", "Highest"],
  ["low", "medium", "high", "highest"],
  false,
  "Priority"
);
let source = await tp.system.prompt("Source (optional)", "", false);
let assignee = await tp.system.prompt("Assignee override (optional)", "", false);

priority = priority ?? "medium";
const yamlString = value => JSON.stringify(value ?? "");
const invalidChars = /[:\/\\*?"<>|]/g;
const created = tp.date.now("YYYY-MM-DD");
await tp.file.move("AGENTS/OUTBOX/" + title.replace(invalidChars, ""));
%>---
status: new
priority: <% priority %>
created: <% created %>
source: <% yamlString(source) %>
assignee: <% yamlString(assignee) %>
task_id: ""
response: ""
blocked_reason: ""
---
# <% Title %>

## Request

==What should be done?==

## Context

==Add relevant wikilinks, paths, constraints, or background.==

## Acceptance Criteria

- [ ]
