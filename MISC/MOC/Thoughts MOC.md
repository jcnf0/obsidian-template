
#MOC

```meta-bind-button
label: New Thought
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: MISC/TEMPLATES/Thought Template.md
    folderPath: PERSONAL/DIARY/THOUGHTS
    fileName: Thought
    openNote: true

```
```dataview
TABLE file.cday as Created, summary
FROM "PERSONAL/DIARY/THOUGHTS" and -#MOC
SORT file.cday DESC
LIMIT 10
```