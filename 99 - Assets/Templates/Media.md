<%*
function get_folder() {
	const path = tp.file.folder(true).split('/');
	let test = "1 - Movies";

	let folder_name = test.split(' ');
	let trimmed = folder_name[2];

	switch (trimmed) {
	case "Movies":
		return "movie";
		break;
	case "Shows":
		return "show";
		break;
	case "Music":
		return "music";
		break;
	case "Games":
		return "game";
		break;
	case "Books":
		return "book";
		break;
	case "Comics":
		return "comic";
		break;
	case "Manga":
		return "manga";
		break;
	case "Tabletops":
		return "tabletop";
		break;
	case "Creators":
		return "creator";
		break;
	}
}
const type = get_folder();
-%>
---
added: <% tp.date.now("YYYY/MM/DD HH:mm") %>
type: <% type %>
---
testtest