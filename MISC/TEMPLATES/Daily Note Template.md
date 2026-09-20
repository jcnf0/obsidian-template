# <% moment(tp.file.title,'YYYY-MM-DD').format("dddd, MMMM DD, YYYY") %>
[[<% moment(tp.file.title,'YYYY-MM-DD_ddd').subtract(1, 'days').format("YYYY-MM-DD_ddd") %>|<< Yesterday]] | [[<% moment(tp.file.title,'YYYY-MM-DD_ddd').add(1, 'days').format("YYYY-MM-DD_ddd") %>|Tomorrow >>]]

---
# Weekly Note : [[{{date:gggg-[W]ww}}]]
`BUTTON[meeting]` `BUTTON[note]` `BUTTON[thought]` `BUTTON[reading]` `BUTTON[research-log]`

---
## Scratch Pad


---
## Summary of Day


---
## Tasks
```tasks
scheduled {{date:YYYY-MM-DD}} OR done on {{date:YYYY-MM-DD}} 
limit 20
hide tags
hide due date
```