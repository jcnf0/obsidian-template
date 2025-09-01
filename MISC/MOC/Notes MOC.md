 #MOC 

```meta-bind-button
label: New Note
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: MISC/TEMPLATES/Note Template.md
    folderPath: RESEARCH/READING/NOTES
    fileName: Note
    openNote: true

```
```dataview
TABLE file.cday as Created, summary
FROM "RESEARCH/READING/NOTES" and -#MOC
SORT file.cday DESC
LIMIT 10
```