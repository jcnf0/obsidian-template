---
created: <% tp.file.creation_date() %>
---
# <% moment(tp.file.title,'YYYY-MM-DD').format("dddd, MMMM DD, YYYY") %>
<< [[<% moment(tp.file.title,'YYYY-MM-DD_ddd').subtract(1, 'days').format("YYYY-MM-DD_ddd") %>|Yesterday]] | [[<% moment(tp.file.title,'YYYY-MM-DD_ddd').add(1, 'days').format("YYYY-MM-DD_ddd") %>|Tomorrow]] >>

---
# Weekly Note : [[{{date:gggg-[W]ww}}]]
`BUTTON[meeting]` `BUTTON[note]` `BUTTON[review]` `BUTTON[thought]`
```meta-bind-button
label: New Meeting
icon: ""
hidden: true
class: ""
tooltip: ""
id: "meeting"
style: primary
actions:
  - type: templaterCreateNote
    templateFile: MISC/TEMPLATES/Meeting Template.md
    folderPath: RESEARCH/MEETINGS
    fileName: Meeting
    openNote: true
```
```meta-bind-button
label: New Note
icon: ""
hidden: true
class: ""
tooltip: ""
id: "note"
style: primary
actions:
  - type: templaterCreateNote
    templateFile: MISC/TEMPLATES/Note Template.md
    folderPath: RESEARCH/READING/NOTES
    fileName: Note
    openNote: true

```
```meta-bind-button
label: New Review
icon: ""
hidden: true
class: ""
tooltip: ""
id: "review"
style: primary
actions:
  - type: templaterCreateNote
    templateFile: MISC/TEMPLATES/Review Template.md
    folderPath: RESEARCH/READING/REVIEWS
    fileName: Review
    openNote: true

```
```meta-bind-button
label: New Thought
icon: ""
hidden: true
class: ""
tooltip: ""
id: "thought"
style: primary
actions:
  - type: templaterCreateNote
    templateFile: MISC/TEMPLATES/Thought Template.md
    folderPath: PERSONAL/DIARY/THOUGHTS
    fileName: Thought
    openNote: true

```
---
# Tasks/Notes


```tasks
path includes MISC/DAILY NOTES
(not done) OR ((done before {{date+1d:YYYY-MM-DD}}) AND (done after {{date-3d:YYYY-MM-DD}}))
limit 20
sort by priority
sort by due date
hide backlink
hide due date
hide tags
```
---
# Notes Created Today
```dataview
LIST FROM "" WHERE file.cday = date("<%moment(tp.file.title,'YYYY-MM-DD').format('YYYY-MM-DD')%>") SORT file.ctime asc
LIMIT 5
```

# Notes Edited Today
```dataview
LIST FROM "" WHERE file.mday = date("<%moment(tp.file.title,'YYYY-MM-DD').format('YYYY-MM-DD')%>") SORT file.mtime asc
LIMIT 5
```