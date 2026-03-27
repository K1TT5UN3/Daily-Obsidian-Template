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
let info = "";
let note = "";

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
		info = `> # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Runtime: \`=this.runtime\`
> #### Publisher: \`=this.publisher\`
> #### Director: \`=this.director\`
> #### Writer: \`=this.writer\`
> #### Original language: \`=this.language\`
> #### Budget: \`=this.budget\`
> #### Earnings: \`=this.earnings\`
> #### Status: \`=this.status\``;
		note = `# Summary:


^Written by: 
---
# Rating:

### Name

- [ ] 10
- [ ] 9
- [ ] 8
- [ ] 7
- [ ] 6
- [ ] 5
- [ ] 4
- [ ] 3
- [ ] 2
- [ ] 1
- [ ] 0

---
# Review:

## Written by: 


---
# Quotes:

- 

---
# Watched by:

- 

---
# Notes:

`;
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
		info = `> # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Total number of seasons: \`=this.seasons\`
> #### Total number of episodes: \`=this.episodes\`
> #### Total runtime: \`=this.runtime\`
> #### Publisher: \`=this.publisher\`
> #### Director: \`=this.director\`
> #### Writer: \`=this.writer\`
> #### Original language: \`=this.language\`
> #### Budget: \`=this.budget\`
> #### Earnings: \`=this.earnings\`
> #### Status: \`=this.status\``;
		note = `# Summary:


^Written by: 
---
# Rating:

### Name

- [ ] 10
- [ ] 9
- [ ] 8
- [ ] 7
- [ ] 6
- [ ] 5
- [ ] 4
- [ ] 3
- [ ] 2
- [ ] 1
- [ ] 0

---
# Review:

## Written by: 


---
# Quotes:

- 

---
# Watched by:

- 

---
# Notes:

`;
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
reviewed_by:`;
		info = `> # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Authors: \`=this.author\`
> #### Amount of tracks: \`=this.tracks\`
> #### Runtime: \`=this.runtime\`
> #### Language: \`=this.language\``;
		note = `# Description:


^Written by: 
---
# Rating:

### Name

- [ ] 10
- [ ] 9
- [ ] 8
- [ ] 7
- [ ] 6
- [ ] 5
- [ ] 4
- [ ] 3
- [ ] 2
- [ ] 1
- [ ] 0

---
# Review:

## Written by: 


---
# Listened to by:

- 

---
# Notes:
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
reviewed_by:`;
		info = `> # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Authors: \`=this.author\`
> #### Publisher: \`=this.publisher\`
> #### Store: \`=this.store\`
> #### Platforms: \`=this.available_on\``;
		note = `# Description:


^Written by: 
---
# Rating:

### Name

- [ ] 10
- [ ] 9
- [ ] 8
- [ ] 7
- [ ] 6
- [ ] 5
- [ ] 4
- [ ] 3
- [ ] 2
- [ ] 1
- [ ] 0

---
# Review:

## Written by: 


---
# Played by:

- 

---
# Notes:

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
		info = `> # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Authors: \`=this.author\`
> #### Publisher: \`=this.publisher\`
> #### Total number of pages: \`=this.pages\`
> #### ISBN: \`=this.isbn\``;
		note = `# Summary:


^Written by: 
---
# Rating:

### Name

- [ ] 10
- [ ] 9
- [ ] 8
- [ ] 7
- [ ] 6
- [ ] 5
- [ ] 4
- [ ] 3
- [ ] 2
- [ ] 1
- [ ] 0

---
# Review:

## Written by: 


---
# Quotes:

- 

---
# Read by:

- 

---
# Notes:

`;
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
reviewed_by:`;
		info = `> # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Authors: \`=this.author\`
> #### Publisher: \`=this.publisher\`
> #### Series: \`=this.series\`
> #### Total number of pages: \`=this.pages\`
> #### Number of chapters: \`=this.chapters\``;
		note = `# Summary:


^Written by: 
---
# Rating:

### Name

- [ ] 10
- [ ] 9
- [ ] 8
- [ ] 7
- [ ] 6
- [ ] 5
- [ ] 4
- [ ] 3
- [ ] 2
- [ ] 1
- [ ] 0

---
# Review:

## Written by: 


---
# Quotes:

- 

---
# Read by:

- 

---
# Notes:

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
reviewed_by:`;
		info = `> # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Authors: \`=this.author\`
> #### Publisher: \`=this.publisher\`
> #### Series: \`=this.series\`
> #### Total number of pages: \`=this.pages\`
> #### Number of chapters: \`=this.chapters\`
> #### Demographic: \`=this.demographic\``;
		note = `# Summary:


^Written by: 
---
# Rating:

### Name

- [ ] 10
- [ ] 9
- [ ] 8
- [ ] 7
- [ ] 6
- [ ] 5
- [ ] 4
- [ ] 3
- [ ] 2
- [ ] 1
- [ ] 0

---
# Review:

## Written by: 


---
# Quotes:

- 

---
# Read by:

- 

---
# Notes:

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
		info = `> # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Authors: \`=this.author\`
> #### Publisher: \`=this.publisher\``;
		note = `# Summary:


^Written by: 
---
# Rating:

### Name

- [ ] 10
- [ ] 9
- [ ] 8
- [ ] 7
- [ ] 6
- [ ] 5
- [ ] 4
- [ ] 3
- [ ] 2
- [ ] 1
- [ ] 0

---
# Review:

## Written by: 


---
# Quotes:

- 

---
# Played by:

- 

---
# Notes:

`;
		break;
	case "creator":
		frontmatter = `name:
birth:
death:
nationality:
birthplace:
age:`;
		info = `> # Name: \`=this.name\`
> #### Born: \`=this.birth\`
> #### Died: \`=this.death\`
> #### Nationality: \`=this.nationality\`
> #### Country of birth: \`=this.birthplace\`
> #### Age: \`=this.age\``;
		note = `# Biography:


^Written by:
---
# Personal life:


^Written by:
---
# Created works:

- 

---
# Awards:

- 

---
# Notes:

`
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

> [!mediacallout] Information
> `="!"+this.image_url`
<% info %>

<% note %>