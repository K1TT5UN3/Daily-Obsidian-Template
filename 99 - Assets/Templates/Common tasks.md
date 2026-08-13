<%*
let task = await tp.system.suggester(["Gave goobies food.", "Refilled goobies water.", "Refilled water bottles.", "Cleaned litter box.", "Refilled litter box.", "Made food.", "Prepared food.", "Put on dishwasher.", "Made tea.", "Made coffee.", "Vacuumed room.", "Prepared medication.", "Cut nails.", "Took out trash.", "Washed floor.", "Shaved.", "Shaved body.", "Put up blinds.", "Pulled down blinds.", "Showered."], ["- [ ] Gave goobies food #\
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
", "- [ ] Cut nails #\
", "- [ ] Changed trash bag #\
- [ ] Took out trash #\
", "- [ ] Washed floor #\
", "- [ ] Shaved #\
", "- [ ] Shaved body #\
", "- [ ] Put up blinds #\
", "- [ ] Pulled down blinds #\
", "- [ ] Prepared shower #\
- [ ] Showered #\
- [ ] Cleaned up after shower #\
"], true, "Choose done activities");
-%>
<% task %>