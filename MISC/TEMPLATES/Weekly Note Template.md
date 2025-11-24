# <% tp.file.title %>
[[<%tp.date.now("YYYY-[W]ww", -7)%>]] <== This Week ==> [[<%tp.date.now("YYYY-[W]ww", 7)%>]]
`BUTTON[meeting]` `BUTTON[note]` `BUTTON[review]` `BUTTON[thought]`

# Main Objectives

# Week Tasks
## Research

## Perso

## Misc


---
```tasks
(not done) OR ((done before {{date+6d:YYYY-MM-DD}}) AND (done after {{date-1d:YYYY-MM-DD}}))
(due after {{date-1d:YYYY-MM-DD}}) AND (due before {{date+6d:YYYY-MM-DD}}) OR (no due date)
(no scheduled date) OR (scheduled before {{date-1d:YYYY-MM-DD}}) OR (scheduled after {{date+6d:YYYY-MM-DD}})
group by function task.due.category.groupText
limit 20
sort by priority
sort by due date
hide tags
hide due date
```

## Days
### MONDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 0, tp.file.title, "YYYY-[W]ww") %>]]
```tasks
(not done) OR (status.type is CANCELLED) OR ((done before {{date+6d:YYYY-MM-DD}}) AND (done after {{date-1d:YYYY-MM-DD}}))
scheduled on {{date:YYYY-MM-DD}}
sort by priority
sort by due date
hide tags
hide due date
```
### TUESDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 1, tp.file.title, "YYYY-[W]ww") %>]]
```tasks
(not done) OR (status.type is CANCELLED) OR ((done before {{date+6d:YYYY-MM-DD}}) AND (done after {{date-1d:YYYY-MM-DD}}))
scheduled on {{date+1d:YYYY-MM-DD}}
sort by priority
sort by due date
hide tags
hide due date
```
### WEDNESDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 2, tp.file.title, "YYYY-[W]ww") %>]]
```tasks
(not done) OR (status.type is CANCELLED) OR ((done before {{date+6d:YYYY-MM-DD}}) AND (done after {{date-1d:YYYY-MM-DD}}))
scheduled on {{date+2d:YYYY-MM-DD}}
sort by priority
sort by due date
hide tags
hide due date
```
### THURSDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 3, tp.file.title, "YYYY-[W]ww") %>]]
```tasks
(not done) OR (status.type is CANCELLED) OR ((done before {{date+6d:YYYY-MM-DD}}) AND (done after {{date-1d:YYYY-MM-DD}}))
scheduled on {{date+3d:YYYY-MM-DD}}
sort by priority
sort by due date
hide tags
hide due date
```
### FRIDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 4, tp.file.title, "YYYY-[W]ww") %>]]
```tasks
(not done) OR (status.type is CANCELLED) OR ((done before {{date+6d:YYYY-MM-DD}}) AND (done after {{date-1d:YYYY-MM-DD}}))
scheduled on {{date+4d:YYYY-MM-DD}}
sort by priority
sort by due date
hide tags
hide due date
```