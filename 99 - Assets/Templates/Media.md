<%*
function get_folder() {
	const path = tp.file.folder(true).split('/');
	const folder = path[1];
	let test = "1 - Movies";

	let folder_name = folder.split(' ');
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
	default:
		return "misc";
	}
}

const type = get_folder();
let frontmatter = "";

switch (type) {
	case "movie":
		frontmatter = `title:
release_date:
release_year:
genres:
runtime:
publisher:
director:
writer:
language:
budget:
earnings:
status:
finished_by:
reviewed_by:`;
		break;
	case "show":
		frontmatter = `title:
release_date:
release_year:
genres:
seasons:
episodes:
runtime:
publisher:
director:
writer:
language:
budget:
earnings:
status:
finished_by:
reviewed_by:`;
		break;
	case "music":
		frontmatter = `title:
author:
release_date:
release_year:
genres:
tracks:
runtime:
language:
finished_by:
reviewed_by:
`;
		break;
	case "game":
		frontmatter = `title:
release_date:
release_year:
genres:
author:
publisher:
store:
available_on:
finished_by:
reviewed_by:
`;
		break;
	case "book":
		frontmatter = `title:
release_date:
release_year:
genres:
author:
publisher:
pages:
isbn:
finished_by:
reviewed_by:`;
		break;
	case "comic":
		frontmatter = `title:
release_date:
release_year:
genres:
author:
publisher:
series:
pages:
chapters:
finished_by:
reviewed_by:
`;
		break;
	case "manga":
		frontmatter = `title:
release_date:
release_year:
genres:
author:
publisher:
series:
pages:
chapters:
demographic:
finished_by:
reviewed_by:
`;
		break;
	case "tabletop":
		frontmatter = `title:
release_date:
release_year:
genres:
author:
publisher:
finished_by:
reviewed_by:`;
		break;
	case "creator":
		frontmatter = `name:
birth:
death:
nationality:
birthplace:
age:
`;
		break;
	case "misc":
		break;
}
-%>
---
image_url:
<% frontmatter %>
added: <% tp.date.now("YYYY/MM/DD HH:mm") %>
type: <% type %>
---

> [!mediacallout] []