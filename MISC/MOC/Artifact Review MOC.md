#MOC

```meta-bind-button
label: New Artifact Review
icon: ""
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: templaterCreateNote
    templateFile: MISC/TEMPLATES/Artifact Review Template.md
    folderPath: RESEARCH/CODE/ARTIFACT REVIEWS
    fileName: Artifact Review
    openNote: true

```
```dataview
TABLE file.cday as Created, summary
FROM "RESEARCH/CODE/ARTIFACT REVIEWS" and -#MOC
SORT file.cday DESC
LIMIT 10
```