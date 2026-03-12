# <% tp.file.title %>
[[<% moment(tp.file.title,"YYYY-[W]ww").subtract(7, 'days').format("YYYY-[W]ww")%>]] <== This Week ==> [[<% moment(tp.file.title,"YYYY-[W]ww").add(7, 'days').format("YYYY-[W]ww")%>]]
`BUTTON[meeting]` `BUTTON[note]` `BUTTON[review]` `BUTTON[thought]` `BUTTON[reading]`

# Main Objectives

# Week Tasks
## Research
### Reading

### Writing

### Coding

## Perso

## Misc


---
```tasks
(not done) OR ((done before {{date+6d:YYYY-MM-DD}}) AND (done after {{date-1d:YYYY-MM-DD}}))
((due after {{date-1d:YYYY-MM-DD}}) AND (due before {{date+6d:YYYY-MM-DD}})) OR (no due date)
((scheduled before {{date-1d:YYYY-MM-DD}}) AND (scheduled after {{date+6d:YYYY-MM-DD}})) OR (no scheduled date) 
group by function task.due.category.groupText
limit 20
hide tags
hide due date
```

## Days
### MONDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 0, tp.file.title, "YYYY-[W]ww") %>]]
```tasks
(not done) OR (status.type is CANCELLED) OR ((done before {{date+6d:YYYY-MM-DD}}) AND (done after {{date-1d:YYYY-MM-DD}}))
scheduled on {{date:YYYY-MM-DD}}
hide tags
hide due date
```
### TUESDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 1, tp.file.title, "YYYY-[W]ww") %>]]
```tasks
(not done) OR (status.type is CANCELLED) OR ((done before {{date+6d:YYYY-MM-DD}}) AND (done after {{date-1d:YYYY-MM-DD}}))
scheduled on {{date+1d:YYYY-MM-DD}}
hide tags
hide due date
```
### WEDNESDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 2, tp.file.title, "YYYY-[W]ww") %>]]
```tasks
(not done) OR (status.type is CANCELLED) OR ((done before {{date+6d:YYYY-MM-DD}}) AND (done after {{date-1d:YYYY-MM-DD}}))
scheduled on {{date+2d:YYYY-MM-DD}}
hide tags
hide due date
```
### THURSDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 3, tp.file.title, "YYYY-[W]ww") %>]]
```tasks
(not done) OR (status.type is CANCELLED) OR ((done before {{date+6d:YYYY-MM-DD}}) AND (done after {{date-1d:YYYY-MM-DD}}))
scheduled on {{date+3d:YYYY-MM-DD}}
hide tags
hide due date
```
### FRIDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 4, tp.file.title, "YYYY-[W]ww") %>]]
```tasks
(not done) OR (status.type is CANCELLED) OR ((done before {{date+6d:YYYY-MM-DD}}) AND (done after {{date-1d:YYYY-MM-DD}}))
scheduled on {{date+4d:YYYY-MM-DD}}
hide tags
hide due date
```
### SATURDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 5, tp.file.title, "YYYY-[W]ww") %>]]
```tasks
(not done) OR (status.type is CANCELLED) OR ((done before {{date+6d:YYYY-MM-DD}}) AND (done after {{date-1d:YYYY-MM-DD}}))
scheduled on {{date+5d:YYYY-MM-DD}}
hide tags
hide due date
```
### SUNDAY [[<% tp.date.now("YYYY-MM-DD_ddd", 6, tp.file.title, "YYYY-[W]ww") %>]]
```tasks
(not done) OR (status.type is CANCELLED) OR ((done before {{date+6d:YYYY-MM-DD}}) AND (done after {{date-1d:YYYY-MM-DD}}))
scheduled on {{date+6d:YYYY-MM-DD}}
hide tags
hide due date
```