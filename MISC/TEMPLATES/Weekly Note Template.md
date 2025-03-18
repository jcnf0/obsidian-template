---
created: <% tp.file.creation_date() %>
---
# <% tp.file.title %>
[[<%tp.date.now("YYYY-[W]ww", -9)%>]] <== This Week ==> [[<%tp.date.now("YYYY-[W]ww", 2)%>]]

# Main Objectives


---
# Week Tasks
```tasks
not done
due after {{date:YYYY-MM-DD}}
due before {{date+6d:YYYY-MM-DD}}
limit 20
sort by priority
sort by due date
group by function task.tags.join(", ").replace("#","").toUpperCase()
hide backlink
hide due date
```

---
# Days

## MONDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 0, tp.file.title, "YYYY-[W]ww") %>]]
## TUESDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 1, tp.file.title, "YYYY-[W]ww") %>]]
## WEDNESDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 2, tp.file.title, "YYYY-[W]ww") %>]]
## THURSDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 3, tp.file.title, "YYYY-[W]ww") %>]]
## FRIDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 4, tp.file.title, "YYYY-[W]ww") %>]]
