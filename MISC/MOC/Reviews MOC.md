#MOC 

```meta-bind-button
label: New Review
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: MISC/TEMPLATES/Review Template.md
    folderPath: RESEARCH/READING/REVIEWS
    fileName: Review
    openNote: true

```
```dataview
TABLE file.cday as Created, summary
FROM "RESEARCH/READING/REVIEWS" and -#MOC
SORT file.cday DESC
LIMIT 10
```