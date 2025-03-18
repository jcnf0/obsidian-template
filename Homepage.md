---
banner: "[[purple-sky-banner.gif]]"
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
```dataviewjs
await dv.view("MISC/TASK CALENDAR", {pages: "", view: "week", firstDayOfWeek: "1", options: "style11 filter", dailyNotes: "MISC/DAILY NOTES", dailyNoteFormat:"YYYY-MM-DD_ddd", "section": "# Tasks/Notes"})
```

```dataviewjs
dv.view("MISC/TASK TIMELINE", {pages: "", dailyNoteFolder: "MISC/DAILY NOTES", options: "noCounters noQuickEntry noDone", dailyNoteFormat:"YYYY-MM-DD_ddd", section:"# Tasks/Notes"})
```

*Possible improvements:* Dropdown for each big section to leave space + daily/weekly note