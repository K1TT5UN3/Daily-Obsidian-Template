---
wake_up_meteors:
sleep_meteors:
wake_up_leaves:
sleep_leaves:
note_type: daily_note
---
## [[<% "80 - Daily/" + tp.date.now("YYYY", -1, tp.file.title, "YYYY-MM-DD") + "/" + tp.date.now("MM", -1, tp.file.title, "YYYY-MM-DD") + " - " + tp.date.now("MMMM", -1, tp.file.title, "YYYY-MM-DD") + "/" + tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>|Yesterday]] <% tp.file.title %> [[<% "80 - Daily/" + tp.date.now("YYYY", 1, tp.file.title, "YYYY-MM-DD") + "/" + tp.date.now("MM", 1, tp.file.title, "YYYY-MM-DD") + " - " + tp.date.now("MMMM", 1, tp.file.title, "YYYY-MM-DD") + "/" + tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>|Tomorrow]]

---

`BUTTON[start-meteor]` `BUTTON[start-leave]` `BUTTON[end-leave]` `BUTTON[end-meteor]`

---
# Activities

## Activities done

```tasks
done on today
hide toolbar
show tree
```

## Reminders
```button
name Add common tasks
type append template
action Common tasks
```
^button-y2ga


## Time sensitive
```tasks
show tree
hide toolbar
path includes 04 - Projects
due on or before next week
```

---
```meta-bind-button
style: primary
label: Start Meteors day
id: start-meteor
hidden: true
action:
  type: updateMetadata
  evaluate: true
  bindTarget: wake_up_meteors
  value: "moment().format('YYYY/MM/DD HH:mm:ss')"
```
```meta-bind-button
style: primary
label: Start Leaves day
id: start-leave
hidden: true
action:
  type: updateMetadata
  evaluate: true
  bindTarget: wake_up_leaves
  value: "moment().format('YYYY/MM/DD HH:mm:ss')"
```
```meta-bind-button
style: primary
label: Finish Leaves day
id: end-leave
hidden: true
action:
  type: updateMetadata
  evaluate: true
  bindTarget: sleep_leaves
  value: "moment().format('YYYY/MM/DD HH:mm:ss')"
```
```meta-bind-button
style: primary
label: Finish Meteors day
id: end-meteor
hidden: true
action:
  type: updateMetadata
  evaluate: true
  bindTarget: sleep_meteors
  value: "moment().format('YYYY/MM/DD HH:mm:ss')"
```