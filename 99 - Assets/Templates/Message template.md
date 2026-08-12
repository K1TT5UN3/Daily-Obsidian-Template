<%*
	let from_in = await tp.system.prompt("Input sender (yours) information.", "", true, false, false);
	let to_in = await tp.system.prompt("Input receiver information.", "", true, false, false);
	let using_in = await tp.system.prompt("Input where you will send the message from.", "", true, false, false);
	let message_in = tp.system.prompt("Write your message.", "", true, true, false);
-%>
---
## Message to <% to_in %> from <% from_in %> using <% using_in %> written on <% tp.date.now('YYYY-MM-DD HH:mm') %>.

<% message_in %>

