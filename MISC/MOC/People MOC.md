 #MOC
 
```meta-bind-button
label: New People Note
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: MISC/TEMPLATES/People Template.md
    folderPath: MISC/PEOPLE
    fileName: Name
    openNote: true

```
```dataview
table title
from "MISC/PEOPLE"
sort file.name asc
```