#MOC

```meta-bind-button
label: New Meeting
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: MISC/TEMPLATES/Meeting Template.md
    folderPath: RESEARCH/MEETINGS
    fileName: Meeting
    openNote: true

```
```dataview
TABLE file.cday as Created, summary
FROM "RESEARCH/MEETINGS" and -#MOC
SORT file.cday DESC
LIMIT 10
```
