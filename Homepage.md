---
banner: "[[homepage.gif]]"
icon:
banner-x: 50
banner-y: 40
banner-display: cover
banner-height: 460
banner-fade: -65
banner-radius: 33
---

```contributionGraph
title:
graphType: default
dateRangeValue: 6
dateRangeType: LATEST_MONTH
startOfWeek: "1"
showCellRuleIndicators: true
titleStyle:
  textAlign: center
  fontSize: 20px
  fontWeight: normal
dataSource:
  type: PAGE
  value: ""
  dateField:
    type: FILE_CTIME
  filters: []
  countField:
    type: DEFAULT
fillTheScreen: false
enableMainContainerShadow: false
cellStyle: {}
cellStyleRules:
  - id: default_b
    color: "#9be9a8"
    min: 1
    max: 2
  - id: default_c
    color: "#40c463"
    min: 2
    max: 5
  - id: default_d
    color: "#30a14e"
    min: 5
    max: 10
  - id: default_e
    color: "#216e39"
    min: 10
    max: 999

```
# Backlog
```tasks
not done
(((due before yesterday) OR ((no due date))) AND (scheduled before today)) OR ((no due date) AND (no scheduled date))
limit 20
group by function task.due.category.groupText
sort by priority
sort by due date
hide tags
hide backlink
```

# 📚 The Stack
```dataview
TABLE file.folder AS "Folder"
WHERE contains(file.tags, "TODO/READ") AND !contains(file.path, "MISC")
LIMIT 10
```
# ✍️ The Heap
```dataview
TABLE file.folder AS "Folder"
WHERE contains(file.tags, "TODO/WRITE") AND file.name!="TAGSONOMY" AND !contains(file.path, "MISC/TEMPLATES")
LIMIT 10
```

![[Obsidian Maintenance Tasks]]