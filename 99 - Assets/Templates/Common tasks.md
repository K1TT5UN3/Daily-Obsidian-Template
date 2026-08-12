<%*
let task = await tp.system.suggester(["Gave goobies food.", "Refilled goobies water.", "Refilled water bottles.", "Cleaned litter box.", "Refilled litter box.", "Made food.", "Prepared food.", "Put on dishwasher.", "Made tea.", "Made coffee.", "Vacuumed room.", "Prepared medication."], ["- [ ] Gave goobies food #\
", "- [ ] Refilled goobies water #\
", "- [ ] Refilled water bottles #\
", "- [ ] Cleaned litter box #\
", "- [ ] Refilled litter box #\
", "- [ ] Made food #\
- [ ] Cleaned after food #\
", "- [ ] Prepared food #\
- [ ] Made food #\
- [ ] Cleaned after food #\
", "- [ ] Turned on dishwasher #\
", "- [ ] Made tea #\
", "- [ ] Made coffee #\
". "- [ ] Vacuumed room #\
", "- [ ] Prepared medication #\
", true, "Choose done activities");
-%>
<% task %>