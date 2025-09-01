---
banner: "[[homepage.gif]]"
icon:
banner-x: 50
banner-y: 50
banner-display: cover
banner-height: 350
---

```contributionGraph
title: 
graphType: default
dateRangeValue: 360
dateRangeType: LATEST_DAYS
startOfWeek: "1"
showCellRuleIndicators: true
titleStyle:
  textAlign: center
  fontSize: 20px
  fontWeight: normal
dataSource:
  type: PAGE
  value: ""
  dateField: {}
  filters: []
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
((due before yesterday) OR ((no due date))) AND (scheduled before today)
limit 20
sort by priority
sort by due date
hide tags
hide backlink
```

# TODOs
## Reading
```dataview
TABLE file.folder AS "Folder"
WHERE contains(file.tags, "TODO/READ") AND file.name!="TAGSONOMY"
LIMIT 10
```
## Writing
```dataview
TABLE file.folder AS "Folder"
WHERE contains(file.tags, "TODO/WRITE") AND file.name!="TAGSONOMY"
LIMIT 10
```

![[Obsidian Maintenance Tasks]]