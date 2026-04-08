<%*
let game_template = `---
title:
release_date:
release_year:
genres:
author:
publisher:
store_link:
available_on:
finished_by:
reviewed_by:
image_url:
added: ` + tp.date.now('YYYY-MM-DD HH:mm') + `
type: Game
---
> [!mediacallout] Information
> \`="!"+this.image_url\`
>  # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Authors: \`=this.author\`
> #### Publisher: \`=this.publisher\`
> #### Platforms: \`=this.available_on\`
# Description:


---
# Rating:
|           |                       1                       |                       2                       |                       3                       |                       4                       |                       5                       |                       6                       |                       7                       |                       8                       |                       9                       |                      10                       |
| :-------- | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: |
| Vanessa   | <input type="checkbox" unchecked id="d2a388"> | <input type="checkbox" unchecked id="f9d389"> | <input type="checkbox" unchecked id="2ec9d0"> | <input type="checkbox" unchecked id="620412"> | <input type="checkbox" unchecked id="290069"> | <input type="checkbox" unchecked id="1b69d2"> | <input type="checkbox" unchecked id="1d339a"> | <input type="checkbox" unchecked id="468504"> | <input type="checkbox" unchecked id="73c7bf"> | <input type="checkbox" unchecked id="ef9b82"> |
| Victoria  | <input type="checkbox" unchecked id="341f7e"> | <input type="checkbox" unchecked id="d8211f"> | <input type="checkbox" unchecked id="eb1655"> | <input type="checkbox" unchecked id="c24d78"> | <input type="checkbox" unchecked id="293793"> | <input type="checkbox" unchecked id="f12914"> | <input type="checkbox" unchecked id="ea8358"> | <input type="checkbox" unchecked id="12a209"> | <input type="checkbox" unchecked id="c9cd43"> | <input type="checkbox" unchecked id="3d4b63"> |
| Vivian    | <input type="checkbox" unchecked id="a14e0d"> | <input type="checkbox" unchecked id="98af28"> | <input type="checkbox" unchecked id="9b0f7a"> | <input type="checkbox" unchecked id="6565dd"> | <input type="checkbox" unchecked id="1cd32b"> | <input type="checkbox" unchecked id="0bbd76"> | <input type="checkbox" unchecked id="e779d1"> | <input type="checkbox" unchecked id="a5fa15"> | <input type="checkbox" unchecked id="c1d1a6"> | <input type="checkbox" unchecked id="323ba6"> |
| Varg      | <input type="checkbox" unchecked id="71ea86"> | <input type="checkbox" unchecked id="935f47"> | <input type="checkbox" unchecked id="a27747"> | <input type="checkbox" unchecked id="e0723f"> | <input type="checkbox" unchecked id="6673db"> | <input type="checkbox" unchecked id="5bddfe"> | <input type="checkbox" unchecked id="e6e68a"> | <input type="checkbox" unchecked id="123993"> | <input type="checkbox" unchecked id="a5c430"> | <input type="checkbox" unchecked id="3749c2"> |
| Valerie   | <input type="checkbox" unchecked id="0b8381"> | <input type="checkbox" unchecked id="0638b5"> | <input type="checkbox" unchecked id="6a1848"> | <input type="checkbox" unchecked id="ce543d"> | <input type="checkbox" unchecked id="3fa684"> | <input type="checkbox" unchecked id="5c7d75"> | <input type="checkbox" unchecked id="328e37"> | <input type="checkbox" unchecked id="03ab2e"> | <input type="checkbox" unchecked id="92844a"> | <input type="checkbox" unchecked id="574ab6"> |
| Vixen     | <input type="checkbox" unchecked id="7d0d79"> | <input type="checkbox" unchecked id="d89fc5"> | <input type="checkbox" unchecked id="4c35d7"> | <input type="checkbox" unchecked id="cd3206"> | <input type="checkbox" unchecked id="5974a2"> | <input type="checkbox" unchecked id="4b28fe"> | <input type="checkbox" unchecked id="390139"> | <input type="checkbox" unchecked id="8772d1"> | <input type="checkbox" unchecked id="10a0e8"> | <input type="checkbox" unchecked id="600c7d"> |
| Willow    | <input type="checkbox" unchecked id="c9dfc8"> | <input type="checkbox" unchecked id="220729"> | <input type="checkbox" unchecked id="1af62a"> | <input type="checkbox" unchecked id="106b09"> | <input type="checkbox" unchecked id="1afd2b"> | <input type="checkbox" unchecked id="6bfed1"> | <input type="checkbox" unchecked id="596533"> | <input type="checkbox" unchecked id="95171e"> | <input type="checkbox" unchecked id="ee8e71"> | <input type="checkbox" unchecked id="7f2734"> |
| Birch     | <input type="checkbox" unchecked id="c8e76d"> | <input type="checkbox" unchecked id="157843"> | <input type="checkbox" unchecked id="604c65"> | <input type="checkbox" unchecked id="482f3c"> | <input type="checkbox" unchecked id="232029"> | <input type="checkbox" unchecked id="8bef18"> | <input type="checkbox" unchecked id="8d5df8"> | <input type="checkbox" unchecked id="5a82bd"> | <input type="checkbox" unchecked id="4175a3"> | <input type="checkbox" unchecked id="a509f3"> |
| Ivy       | <input type="checkbox" unchecked id="6a74d0"> | <input type="checkbox" unchecked id="185eb3"> | <input type="checkbox" unchecked id="8efcf5"> | <input type="checkbox" unchecked id="336d4e"> | <input type="checkbox" unchecked id="4f60ba"> | <input type="checkbox" unchecked id="f18219"> | <input type="checkbox" unchecked id="4c6ea2"> | <input type="checkbox" unchecked id="914b4d"> | <input type="checkbox" unchecked id="791caa"> | <input type="checkbox" unchecked id="691945"> |
| Maple     | <input type="checkbox" unchecked id="d98dff"> | <input type="checkbox" unchecked id="bd75b3"> | <input type="checkbox" unchecked id="2470b7"> | <input type="checkbox" unchecked id="5067a8"> | <input type="checkbox" unchecked id="eaf4bd"> | <input type="checkbox" unchecked id="2fdd29"> | <input type="checkbox" unchecked id="f7650d"> | <input type="checkbox" unchecked id="a4132c"> | <input type="checkbox" unchecked id="b4b9d0"> | <input type="checkbox" unchecked id="96bcf4"> |
| Dandelion | <input type="checkbox" unchecked id="bf2666"> | <input type="checkbox" unchecked id="522b62"> | <input type="checkbox" unchecked id="88c282"> | <input type="checkbox" unchecked id="ae8c5d"> | <input type="checkbox" unchecked id="c5154c"> | <input type="checkbox" unchecked id="833f54"> | <input type="checkbox" unchecked id="809c50"> | <input type="checkbox" unchecked id="7ade6a"> | <input type="checkbox" unchecked id="184b83"> | <input type="checkbox" unchecked id="3899b9"> |

---
# Review:

### Written by: 

---
# Played by:
- [ ] Vanessa
- [ ] Victoria
- [ ] Vivian
- [ ] Varg
- [ ] Valerie
- [ ] Vixen
- [ ] Willow
- [ ] Birch
- [ ] Ivy
- [ ] Maple
- [ ] Dandelion

---
# Notes:

`;
let book_template = `---
title:
release_date:
release_year:
genres:
author:
publisher:
pages:
isbn:
finished_by:
reviewed_by:
image_url:
added: ` + tp.date.now('YYYY-MM-DD HH:mm') + `
type: Book
---
> [!mediacallout] Information
> \`="!"+this.image_url\`
>  # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Authors: \`=this.author\`
> #### Publisher: \`=this.publisher\`
> #### Total number of pages: \`=this.pages\`
> #### ISBN: \`=this.isbn\`
# Description:


---
# Rating:
|           |                       1                       |                       2                       |                       3                       |                       4                       |                       5                       |                       6                       |                       7                       |                       8                       |                       9                       |                      10                       |
| :-------- | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: |
| Vanessa   | <input type="checkbox" unchecked id="d2a388"> | <input type="checkbox" unchecked id="f9d389"> | <input type="checkbox" unchecked id="2ec9d0"> | <input type="checkbox" unchecked id="620412"> | <input type="checkbox" unchecked id="290069"> | <input type="checkbox" unchecked id="1b69d2"> | <input type="checkbox" unchecked id="1d339a"> | <input type="checkbox" unchecked id="468504"> | <input type="checkbox" unchecked id="73c7bf"> | <input type="checkbox" unchecked id="ef9b82"> |
| Victoria  | <input type="checkbox" unchecked id="341f7e"> | <input type="checkbox" unchecked id="d8211f"> | <input type="checkbox" unchecked id="eb1655"> | <input type="checkbox" unchecked id="c24d78"> | <input type="checkbox" unchecked id="293793"> | <input type="checkbox" unchecked id="f12914"> | <input type="checkbox" unchecked id="ea8358"> | <input type="checkbox" unchecked id="12a209"> | <input type="checkbox" unchecked id="c9cd43"> | <input type="checkbox" unchecked id="3d4b63"> |
| Vivian    | <input type="checkbox" unchecked id="a14e0d"> | <input type="checkbox" unchecked id="98af28"> | <input type="checkbox" unchecked id="9b0f7a"> | <input type="checkbox" unchecked id="6565dd"> | <input type="checkbox" unchecked id="1cd32b"> | <input type="checkbox" unchecked id="0bbd76"> | <input type="checkbox" unchecked id="e779d1"> | <input type="checkbox" unchecked id="a5fa15"> | <input type="checkbox" unchecked id="c1d1a6"> | <input type="checkbox" unchecked id="323ba6"> |
| Varg      | <input type="checkbox" unchecked id="71ea86"> | <input type="checkbox" unchecked id="935f47"> | <input type="checkbox" unchecked id="a27747"> | <input type="checkbox" unchecked id="e0723f"> | <input type="checkbox" unchecked id="6673db"> | <input type="checkbox" unchecked id="5bddfe"> | <input type="checkbox" unchecked id="e6e68a"> | <input type="checkbox" unchecked id="123993"> | <input type="checkbox" unchecked id="a5c430"> | <input type="checkbox" unchecked id="3749c2"> |
| Valerie   | <input type="checkbox" unchecked id="0b8381"> | <input type="checkbox" unchecked id="0638b5"> | <input type="checkbox" unchecked id="6a1848"> | <input type="checkbox" unchecked id="ce543d"> | <input type="checkbox" unchecked id="3fa684"> | <input type="checkbox" unchecked id="5c7d75"> | <input type="checkbox" unchecked id="328e37"> | <input type="checkbox" unchecked id="03ab2e"> | <input type="checkbox" unchecked id="92844a"> | <input type="checkbox" unchecked id="574ab6"> |
| Vixen     | <input type="checkbox" unchecked id="7d0d79"> | <input type="checkbox" unchecked id="d89fc5"> | <input type="checkbox" unchecked id="4c35d7"> | <input type="checkbox" unchecked id="cd3206"> | <input type="checkbox" unchecked id="5974a2"> | <input type="checkbox" unchecked id="4b28fe"> | <input type="checkbox" unchecked id="390139"> | <input type="checkbox" unchecked id="8772d1"> | <input type="checkbox" unchecked id="10a0e8"> | <input type="checkbox" unchecked id="600c7d"> |
| Willow    | <input type="checkbox" unchecked id="c9dfc8"> | <input type="checkbox" unchecked id="220729"> | <input type="checkbox" unchecked id="1af62a"> | <input type="checkbox" unchecked id="106b09"> | <input type="checkbox" unchecked id="1afd2b"> | <input type="checkbox" unchecked id="6bfed1"> | <input type="checkbox" unchecked id="596533"> | <input type="checkbox" unchecked id="95171e"> | <input type="checkbox" unchecked id="ee8e71"> | <input type="checkbox" unchecked id="7f2734"> |
| Birch     | <input type="checkbox" unchecked id="c8e76d"> | <input type="checkbox" unchecked id="157843"> | <input type="checkbox" unchecked id="604c65"> | <input type="checkbox" unchecked id="482f3c"> | <input type="checkbox" unchecked id="232029"> | <input type="checkbox" unchecked id="8bef18"> | <input type="checkbox" unchecked id="8d5df8"> | <input type="checkbox" unchecked id="5a82bd"> | <input type="checkbox" unchecked id="4175a3"> | <input type="checkbox" unchecked id="a509f3"> |
| Ivy       | <input type="checkbox" unchecked id="6a74d0"> | <input type="checkbox" unchecked id="185eb3"> | <input type="checkbox" unchecked id="8efcf5"> | <input type="checkbox" unchecked id="336d4e"> | <input type="checkbox" unchecked id="4f60ba"> | <input type="checkbox" unchecked id="f18219"> | <input type="checkbox" unchecked id="4c6ea2"> | <input type="checkbox" unchecked id="914b4d"> | <input type="checkbox" unchecked id="791caa"> | <input type="checkbox" unchecked id="691945"> |
| Maple     | <input type="checkbox" unchecked id="d98dff"> | <input type="checkbox" unchecked id="bd75b3"> | <input type="checkbox" unchecked id="2470b7"> | <input type="checkbox" unchecked id="5067a8"> | <input type="checkbox" unchecked id="eaf4bd"> | <input type="checkbox" unchecked id="2fdd29"> | <input type="checkbox" unchecked id="f7650d"> | <input type="checkbox" unchecked id="a4132c"> | <input type="checkbox" unchecked id="b4b9d0"> | <input type="checkbox" unchecked id="96bcf4"> |
| Dandelion | <input type="checkbox" unchecked id="bf2666"> | <input type="checkbox" unchecked id="522b62"> | <input type="checkbox" unchecked id="88c282"> | <input type="checkbox" unchecked id="ae8c5d"> | <input type="checkbox" unchecked id="c5154c"> | <input type="checkbox" unchecked id="833f54"> | <input type="checkbox" unchecked id="809c50"> | <input type="checkbox" unchecked id="7ade6a"> | <input type="checkbox" unchecked id="184b83"> | <input type="checkbox" unchecked id="3899b9"> |

---
# Review:

### Written by: 

---
# Read by:
- [ ] Vanessa
- [ ] Victoria
- [ ] Vivian
- [ ] Varg
- [ ] Valerie
- [ ] Vixen
- [ ] Willow
- [ ] Birch
- [ ] Ivy
- [ ] Maple
- [ ] Dandelion

---
# Notes:

`;
let comic_template = `---
title:
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
image_url:
added: ` + tp.date.now('YYYY-MM-DD HH:mm') + `
type: Comic
---
> [!mediacallout] Information
> \`="!"+this.image_url\`
>  # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Authors: \`=this.author\`
> #### Publisher: \`=this.publisher\`
> #### Total number of pages: \`=this.pages\`
> #### Series: \`=this.series\`
> #### Number of chapters: \`=this.chapters\`
# Description:


---
# Rating:
|           |                       1                       |                       2                       |                       3                       |                       4                       |                       5                       |                       6                       |                       7                       |                       8                       |                       9                       |                      10                       |
| :-------- | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: |
| Vanessa   | <input type="checkbox" unchecked id="d2a388"> | <input type="checkbox" unchecked id="f9d389"> | <input type="checkbox" unchecked id="2ec9d0"> | <input type="checkbox" unchecked id="620412"> | <input type="checkbox" unchecked id="290069"> | <input type="checkbox" unchecked id="1b69d2"> | <input type="checkbox" unchecked id="1d339a"> | <input type="checkbox" unchecked id="468504"> | <input type="checkbox" unchecked id="73c7bf"> | <input type="checkbox" unchecked id="ef9b82"> |
| Victoria  | <input type="checkbox" unchecked id="341f7e"> | <input type="checkbox" unchecked id="d8211f"> | <input type="checkbox" unchecked id="eb1655"> | <input type="checkbox" unchecked id="c24d78"> | <input type="checkbox" unchecked id="293793"> | <input type="checkbox" unchecked id="f12914"> | <input type="checkbox" unchecked id="ea8358"> | <input type="checkbox" unchecked id="12a209"> | <input type="checkbox" unchecked id="c9cd43"> | <input type="checkbox" unchecked id="3d4b63"> |
| Vivian    | <input type="checkbox" unchecked id="a14e0d"> | <input type="checkbox" unchecked id="98af28"> | <input type="checkbox" unchecked id="9b0f7a"> | <input type="checkbox" unchecked id="6565dd"> | <input type="checkbox" unchecked id="1cd32b"> | <input type="checkbox" unchecked id="0bbd76"> | <input type="checkbox" unchecked id="e779d1"> | <input type="checkbox" unchecked id="a5fa15"> | <input type="checkbox" unchecked id="c1d1a6"> | <input type="checkbox" unchecked id="323ba6"> |
| Varg      | <input type="checkbox" unchecked id="71ea86"> | <input type="checkbox" unchecked id="935f47"> | <input type="checkbox" unchecked id="a27747"> | <input type="checkbox" unchecked id="e0723f"> | <input type="checkbox" unchecked id="6673db"> | <input type="checkbox" unchecked id="5bddfe"> | <input type="checkbox" unchecked id="e6e68a"> | <input type="checkbox" unchecked id="123993"> | <input type="checkbox" unchecked id="a5c430"> | <input type="checkbox" unchecked id="3749c2"> |
| Valerie   | <input type="checkbox" unchecked id="0b8381"> | <input type="checkbox" unchecked id="0638b5"> | <input type="checkbox" unchecked id="6a1848"> | <input type="checkbox" unchecked id="ce543d"> | <input type="checkbox" unchecked id="3fa684"> | <input type="checkbox" unchecked id="5c7d75"> | <input type="checkbox" unchecked id="328e37"> | <input type="checkbox" unchecked id="03ab2e"> | <input type="checkbox" unchecked id="92844a"> | <input type="checkbox" unchecked id="574ab6"> |
| Vixen     | <input type="checkbox" unchecked id="7d0d79"> | <input type="checkbox" unchecked id="d89fc5"> | <input type="checkbox" unchecked id="4c35d7"> | <input type="checkbox" unchecked id="cd3206"> | <input type="checkbox" unchecked id="5974a2"> | <input type="checkbox" unchecked id="4b28fe"> | <input type="checkbox" unchecked id="390139"> | <input type="checkbox" unchecked id="8772d1"> | <input type="checkbox" unchecked id="10a0e8"> | <input type="checkbox" unchecked id="600c7d"> |
| Willow    | <input type="checkbox" unchecked id="c9dfc8"> | <input type="checkbox" unchecked id="220729"> | <input type="checkbox" unchecked id="1af62a"> | <input type="checkbox" unchecked id="106b09"> | <input type="checkbox" unchecked id="1afd2b"> | <input type="checkbox" unchecked id="6bfed1"> | <input type="checkbox" unchecked id="596533"> | <input type="checkbox" unchecked id="95171e"> | <input type="checkbox" unchecked id="ee8e71"> | <input type="checkbox" unchecked id="7f2734"> |
| Birch     | <input type="checkbox" unchecked id="c8e76d"> | <input type="checkbox" unchecked id="157843"> | <input type="checkbox" unchecked id="604c65"> | <input type="checkbox" unchecked id="482f3c"> | <input type="checkbox" unchecked id="232029"> | <input type="checkbox" unchecked id="8bef18"> | <input type="checkbox" unchecked id="8d5df8"> | <input type="checkbox" unchecked id="5a82bd"> | <input type="checkbox" unchecked id="4175a3"> | <input type="checkbox" unchecked id="a509f3"> |
| Ivy       | <input type="checkbox" unchecked id="6a74d0"> | <input type="checkbox" unchecked id="185eb3"> | <input type="checkbox" unchecked id="8efcf5"> | <input type="checkbox" unchecked id="336d4e"> | <input type="checkbox" unchecked id="4f60ba"> | <input type="checkbox" unchecked id="f18219"> | <input type="checkbox" unchecked id="4c6ea2"> | <input type="checkbox" unchecked id="914b4d"> | <input type="checkbox" unchecked id="791caa"> | <input type="checkbox" unchecked id="691945"> |
| Maple     | <input type="checkbox" unchecked id="d98dff"> | <input type="checkbox" unchecked id="bd75b3"> | <input type="checkbox" unchecked id="2470b7"> | <input type="checkbox" unchecked id="5067a8"> | <input type="checkbox" unchecked id="eaf4bd"> | <input type="checkbox" unchecked id="2fdd29"> | <input type="checkbox" unchecked id="f7650d"> | <input type="checkbox" unchecked id="a4132c"> | <input type="checkbox" unchecked id="b4b9d0"> | <input type="checkbox" unchecked id="96bcf4"> |
| Dandelion | <input type="checkbox" unchecked id="bf2666"> | <input type="checkbox" unchecked id="522b62"> | <input type="checkbox" unchecked id="88c282"> | <input type="checkbox" unchecked id="ae8c5d"> | <input type="checkbox" unchecked id="c5154c"> | <input type="checkbox" unchecked id="833f54"> | <input type="checkbox" unchecked id="809c50"> | <input type="checkbox" unchecked id="7ade6a"> | <input type="checkbox" unchecked id="184b83"> | <input type="checkbox" unchecked id="3899b9"> |

---
# Review:

### Written by: 

---
# Read by:
- [ ] Vanessa
- [ ] Victoria
- [ ] Vivian
- [ ] Varg
- [ ] Valerie
- [ ] Vixen
- [ ] Willow
- [ ] Birch
- [ ] Ivy
- [ ] Maple
- [ ] Dandelion

---
# Notes:

`;
let manga_template = `---
title:
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
image_url:
added: ` + tp.date.now('YYYY-MM-DD HH:mm') + `
type: Manga
---
> [!mediacallout] Information
> \`="!"+this.image_url\`
>  # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Authors: \`=this.author\`
> #### Publisher: \`=this.publisher\`
> #### Total number of pages: \`=this.pages\`
> #### Series: \`=this.series\`
> #### Number of chapters: \`=this.chapters\`
> #### Demographic: \`=this.demographic\`;
# Description:


---
# Rating:
|           |                       1                       |                       2                       |                       3                       |                       4                       |                       5                       |                       6                       |                       7                       |                       8                       |                       9                       |                      10                       |
| :-------- | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: |
| Vanessa   | <input type="checkbox" unchecked id="d2a388"> | <input type="checkbox" unchecked id="f9d389"> | <input type="checkbox" unchecked id="2ec9d0"> | <input type="checkbox" unchecked id="620412"> | <input type="checkbox" unchecked id="290069"> | <input type="checkbox" unchecked id="1b69d2"> | <input type="checkbox" unchecked id="1d339a"> | <input type="checkbox" unchecked id="468504"> | <input type="checkbox" unchecked id="73c7bf"> | <input type="checkbox" unchecked id="ef9b82"> |
| Victoria  | <input type="checkbox" unchecked id="341f7e"> | <input type="checkbox" unchecked id="d8211f"> | <input type="checkbox" unchecked id="eb1655"> | <input type="checkbox" unchecked id="c24d78"> | <input type="checkbox" unchecked id="293793"> | <input type="checkbox" unchecked id="f12914"> | <input type="checkbox" unchecked id="ea8358"> | <input type="checkbox" unchecked id="12a209"> | <input type="checkbox" unchecked id="c9cd43"> | <input type="checkbox" unchecked id="3d4b63"> |
| Vivian    | <input type="checkbox" unchecked id="a14e0d"> | <input type="checkbox" unchecked id="98af28"> | <input type="checkbox" unchecked id="9b0f7a"> | <input type="checkbox" unchecked id="6565dd"> | <input type="checkbox" unchecked id="1cd32b"> | <input type="checkbox" unchecked id="0bbd76"> | <input type="checkbox" unchecked id="e779d1"> | <input type="checkbox" unchecked id="a5fa15"> | <input type="checkbox" unchecked id="c1d1a6"> | <input type="checkbox" unchecked id="323ba6"> |
| Varg      | <input type="checkbox" unchecked id="71ea86"> | <input type="checkbox" unchecked id="935f47"> | <input type="checkbox" unchecked id="a27747"> | <input type="checkbox" unchecked id="e0723f"> | <input type="checkbox" unchecked id="6673db"> | <input type="checkbox" unchecked id="5bddfe"> | <input type="checkbox" unchecked id="e6e68a"> | <input type="checkbox" unchecked id="123993"> | <input type="checkbox" unchecked id="a5c430"> | <input type="checkbox" unchecked id="3749c2"> |
| Valerie   | <input type="checkbox" unchecked id="0b8381"> | <input type="checkbox" unchecked id="0638b5"> | <input type="checkbox" unchecked id="6a1848"> | <input type="checkbox" unchecked id="ce543d"> | <input type="checkbox" unchecked id="3fa684"> | <input type="checkbox" unchecked id="5c7d75"> | <input type="checkbox" unchecked id="328e37"> | <input type="checkbox" unchecked id="03ab2e"> | <input type="checkbox" unchecked id="92844a"> | <input type="checkbox" unchecked id="574ab6"> |
| Vixen     | <input type="checkbox" unchecked id="7d0d79"> | <input type="checkbox" unchecked id="d89fc5"> | <input type="checkbox" unchecked id="4c35d7"> | <input type="checkbox" unchecked id="cd3206"> | <input type="checkbox" unchecked id="5974a2"> | <input type="checkbox" unchecked id="4b28fe"> | <input type="checkbox" unchecked id="390139"> | <input type="checkbox" unchecked id="8772d1"> | <input type="checkbox" unchecked id="10a0e8"> | <input type="checkbox" unchecked id="600c7d"> |
| Willow    | <input type="checkbox" unchecked id="c9dfc8"> | <input type="checkbox" unchecked id="220729"> | <input type="checkbox" unchecked id="1af62a"> | <input type="checkbox" unchecked id="106b09"> | <input type="checkbox" unchecked id="1afd2b"> | <input type="checkbox" unchecked id="6bfed1"> | <input type="checkbox" unchecked id="596533"> | <input type="checkbox" unchecked id="95171e"> | <input type="checkbox" unchecked id="ee8e71"> | <input type="checkbox" unchecked id="7f2734"> |
| Birch     | <input type="checkbox" unchecked id="c8e76d"> | <input type="checkbox" unchecked id="157843"> | <input type="checkbox" unchecked id="604c65"> | <input type="checkbox" unchecked id="482f3c"> | <input type="checkbox" unchecked id="232029"> | <input type="checkbox" unchecked id="8bef18"> | <input type="checkbox" unchecked id="8d5df8"> | <input type="checkbox" unchecked id="5a82bd"> | <input type="checkbox" unchecked id="4175a3"> | <input type="checkbox" unchecked id="a509f3"> |
| Ivy       | <input type="checkbox" unchecked id="6a74d0"> | <input type="checkbox" unchecked id="185eb3"> | <input type="checkbox" unchecked id="8efcf5"> | <input type="checkbox" unchecked id="336d4e"> | <input type="checkbox" unchecked id="4f60ba"> | <input type="checkbox" unchecked id="f18219"> | <input type="checkbox" unchecked id="4c6ea2"> | <input type="checkbox" unchecked id="914b4d"> | <input type="checkbox" unchecked id="791caa"> | <input type="checkbox" unchecked id="691945"> |
| Maple     | <input type="checkbox" unchecked id="d98dff"> | <input type="checkbox" unchecked id="bd75b3"> | <input type="checkbox" unchecked id="2470b7"> | <input type="checkbox" unchecked id="5067a8"> | <input type="checkbox" unchecked id="eaf4bd"> | <input type="checkbox" unchecked id="2fdd29"> | <input type="checkbox" unchecked id="f7650d"> | <input type="checkbox" unchecked id="a4132c"> | <input type="checkbox" unchecked id="b4b9d0"> | <input type="checkbox" unchecked id="96bcf4"> |
| Dandelion | <input type="checkbox" unchecked id="bf2666"> | <input type="checkbox" unchecked id="522b62"> | <input type="checkbox" unchecked id="88c282"> | <input type="checkbox" unchecked id="ae8c5d"> | <input type="checkbox" unchecked id="c5154c"> | <input type="checkbox" unchecked id="833f54"> | <input type="checkbox" unchecked id="809c50"> | <input type="checkbox" unchecked id="7ade6a"> | <input type="checkbox" unchecked id="184b83"> | <input type="checkbox" unchecked id="3899b9"> |

---
# Review:

### Written by: 

---
# Read by:
- [ ] Vanessa
- [ ] Victoria
- [ ] Vivian
- [ ] Varg
- [ ] Valerie
- [ ] Vixen
- [ ] Willow
- [ ] Birch
- [ ] Ivy
- [ ] Maple
- [ ] Dandelion

---
# Notes:

`;
let movie_template = `---
title:
release_date:
release_year:
genres:
author:
publisher:
runtime:
finished_by:
reviewed_by:
image_url:
added: ` + tp.date.now('YYYY-MM-DD HH:mm') + `
type: Movie
---
> [!mediacallout] Information
> \`="!"+this.image_url\`
>  # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Authors: \`=this.author\`
> #### Publisher: \`=this.publisher\`
> #### Runtime: \`=this.runtime\`
# Description:


---
# Rating:
|           |                       1                       |                       2                       |                       3                       |                       4                       |                       5                       |                       6                       |                       7                       |                       8                       |                       9                       |                      10                       |
| :-------- | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: |
| Vanessa   | <input type="checkbox" unchecked id="d2a388"> | <input type="checkbox" unchecked id="f9d389"> | <input type="checkbox" unchecked id="2ec9d0"> | <input type="checkbox" unchecked id="620412"> | <input type="checkbox" unchecked id="290069"> | <input type="checkbox" unchecked id="1b69d2"> | <input type="checkbox" unchecked id="1d339a"> | <input type="checkbox" unchecked id="468504"> | <input type="checkbox" unchecked id="73c7bf"> | <input type="checkbox" unchecked id="ef9b82"> |
| Victoria  | <input type="checkbox" unchecked id="341f7e"> | <input type="checkbox" unchecked id="d8211f"> | <input type="checkbox" unchecked id="eb1655"> | <input type="checkbox" unchecked id="c24d78"> | <input type="checkbox" unchecked id="293793"> | <input type="checkbox" unchecked id="f12914"> | <input type="checkbox" unchecked id="ea8358"> | <input type="checkbox" unchecked id="12a209"> | <input type="checkbox" unchecked id="c9cd43"> | <input type="checkbox" unchecked id="3d4b63"> |
| Vivian    | <input type="checkbox" unchecked id="a14e0d"> | <input type="checkbox" unchecked id="98af28"> | <input type="checkbox" unchecked id="9b0f7a"> | <input type="checkbox" unchecked id="6565dd"> | <input type="checkbox" unchecked id="1cd32b"> | <input type="checkbox" unchecked id="0bbd76"> | <input type="checkbox" unchecked id="e779d1"> | <input type="checkbox" unchecked id="a5fa15"> | <input type="checkbox" unchecked id="c1d1a6"> | <input type="checkbox" unchecked id="323ba6"> |
| Varg      | <input type="checkbox" unchecked id="71ea86"> | <input type="checkbox" unchecked id="935f47"> | <input type="checkbox" unchecked id="a27747"> | <input type="checkbox" unchecked id="e0723f"> | <input type="checkbox" unchecked id="6673db"> | <input type="checkbox" unchecked id="5bddfe"> | <input type="checkbox" unchecked id="e6e68a"> | <input type="checkbox" unchecked id="123993"> | <input type="checkbox" unchecked id="a5c430"> | <input type="checkbox" unchecked id="3749c2"> |
| Valerie   | <input type="checkbox" unchecked id="0b8381"> | <input type="checkbox" unchecked id="0638b5"> | <input type="checkbox" unchecked id="6a1848"> | <input type="checkbox" unchecked id="ce543d"> | <input type="checkbox" unchecked id="3fa684"> | <input type="checkbox" unchecked id="5c7d75"> | <input type="checkbox" unchecked id="328e37"> | <input type="checkbox" unchecked id="03ab2e"> | <input type="checkbox" unchecked id="92844a"> | <input type="checkbox" unchecked id="574ab6"> |
| Vixen     | <input type="checkbox" unchecked id="7d0d79"> | <input type="checkbox" unchecked id="d89fc5"> | <input type="checkbox" unchecked id="4c35d7"> | <input type="checkbox" unchecked id="cd3206"> | <input type="checkbox" unchecked id="5974a2"> | <input type="checkbox" unchecked id="4b28fe"> | <input type="checkbox" unchecked id="390139"> | <input type="checkbox" unchecked id="8772d1"> | <input type="checkbox" unchecked id="10a0e8"> | <input type="checkbox" unchecked id="600c7d"> |
| Willow    | <input type="checkbox" unchecked id="c9dfc8"> | <input type="checkbox" unchecked id="220729"> | <input type="checkbox" unchecked id="1af62a"> | <input type="checkbox" unchecked id="106b09"> | <input type="checkbox" unchecked id="1afd2b"> | <input type="checkbox" unchecked id="6bfed1"> | <input type="checkbox" unchecked id="596533"> | <input type="checkbox" unchecked id="95171e"> | <input type="checkbox" unchecked id="ee8e71"> | <input type="checkbox" unchecked id="7f2734"> |
| Birch     | <input type="checkbox" unchecked id="c8e76d"> | <input type="checkbox" unchecked id="157843"> | <input type="checkbox" unchecked id="604c65"> | <input type="checkbox" unchecked id="482f3c"> | <input type="checkbox" unchecked id="232029"> | <input type="checkbox" unchecked id="8bef18"> | <input type="checkbox" unchecked id="8d5df8"> | <input type="checkbox" unchecked id="5a82bd"> | <input type="checkbox" unchecked id="4175a3"> | <input type="checkbox" unchecked id="a509f3"> |
| Ivy       | <input type="checkbox" unchecked id="6a74d0"> | <input type="checkbox" unchecked id="185eb3"> | <input type="checkbox" unchecked id="8efcf5"> | <input type="checkbox" unchecked id="336d4e"> | <input type="checkbox" unchecked id="4f60ba"> | <input type="checkbox" unchecked id="f18219"> | <input type="checkbox" unchecked id="4c6ea2"> | <input type="checkbox" unchecked id="914b4d"> | <input type="checkbox" unchecked id="791caa"> | <input type="checkbox" unchecked id="691945"> |
| Maple     | <input type="checkbox" unchecked id="d98dff"> | <input type="checkbox" unchecked id="bd75b3"> | <input type="checkbox" unchecked id="2470b7"> | <input type="checkbox" unchecked id="5067a8"> | <input type="checkbox" unchecked id="eaf4bd"> | <input type="checkbox" unchecked id="2fdd29"> | <input type="checkbox" unchecked id="f7650d"> | <input type="checkbox" unchecked id="a4132c"> | <input type="checkbox" unchecked id="b4b9d0"> | <input type="checkbox" unchecked id="96bcf4"> |
| Dandelion | <input type="checkbox" unchecked id="bf2666"> | <input type="checkbox" unchecked id="522b62"> | <input type="checkbox" unchecked id="88c282"> | <input type="checkbox" unchecked id="ae8c5d"> | <input type="checkbox" unchecked id="c5154c"> | <input type="checkbox" unchecked id="833f54"> | <input type="checkbox" unchecked id="809c50"> | <input type="checkbox" unchecked id="7ade6a"> | <input type="checkbox" unchecked id="184b83"> | <input type="checkbox" unchecked id="3899b9"> |

---
# Review:

### Written by: 

---
# Watched by:
- [ ] Vanessa
- [ ] Victoria
- [ ] Vivian
- [ ] Varg
- [ ] Valerie
- [ ] Vixen
- [ ] Willow
- [ ] Birch
- [ ] Ivy
- [ ] Maple
- [ ] Dandelion

---
# Notes:

`;
let show_template = `---
title:
release_date:
release_year:
genres:
seasons:
episodes:
runtime:
status:
author:
publisher:
available_on:
finished_by:
reviewed_by:
image_url:
added: ` + tp.date.now('YYYY-MM-DD HH:mm') + `
type: Show
---
> [!mediacallout] Information
> \`="!"+this.image_url\`
>  # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Authors: \`=this.author\`
> #### Publisher: \`=this.publisher\`
> #### Number of seasons: \`=this.seasons\`
> #### Total amount of episodes: \`=this.episodes\`
> #### Total runtime: \`=this.runtime\`
> #### Status: \`=this.status\`
# Description:


---
# Rating:
|           |                       1                       |                       2                       |                       3                       |                       4                       |                       5                       |                       6                       |                       7                       |                       8                       |                       9                       |                      10                       |
| :-------- | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: |
| Vanessa   | <input type="checkbox" unchecked id="d2a388"> | <input type="checkbox" unchecked id="f9d389"> | <input type="checkbox" unchecked id="2ec9d0"> | <input type="checkbox" unchecked id="620412"> | <input type="checkbox" unchecked id="290069"> | <input type="checkbox" unchecked id="1b69d2"> | <input type="checkbox" unchecked id="1d339a"> | <input type="checkbox" unchecked id="468504"> | <input type="checkbox" unchecked id="73c7bf"> | <input type="checkbox" unchecked id="ef9b82"> |
| Victoria  | <input type="checkbox" unchecked id="341f7e"> | <input type="checkbox" unchecked id="d8211f"> | <input type="checkbox" unchecked id="eb1655"> | <input type="checkbox" unchecked id="c24d78"> | <input type="checkbox" unchecked id="293793"> | <input type="checkbox" unchecked id="f12914"> | <input type="checkbox" unchecked id="ea8358"> | <input type="checkbox" unchecked id="12a209"> | <input type="checkbox" unchecked id="c9cd43"> | <input type="checkbox" unchecked id="3d4b63"> |
| Vivian    | <input type="checkbox" unchecked id="a14e0d"> | <input type="checkbox" unchecked id="98af28"> | <input type="checkbox" unchecked id="9b0f7a"> | <input type="checkbox" unchecked id="6565dd"> | <input type="checkbox" unchecked id="1cd32b"> | <input type="checkbox" unchecked id="0bbd76"> | <input type="checkbox" unchecked id="e779d1"> | <input type="checkbox" unchecked id="a5fa15"> | <input type="checkbox" unchecked id="c1d1a6"> | <input type="checkbox" unchecked id="323ba6"> |
| Varg      | <input type="checkbox" unchecked id="71ea86"> | <input type="checkbox" unchecked id="935f47"> | <input type="checkbox" unchecked id="a27747"> | <input type="checkbox" unchecked id="e0723f"> | <input type="checkbox" unchecked id="6673db"> | <input type="checkbox" unchecked id="5bddfe"> | <input type="checkbox" unchecked id="e6e68a"> | <input type="checkbox" unchecked id="123993"> | <input type="checkbox" unchecked id="a5c430"> | <input type="checkbox" unchecked id="3749c2"> |
| Valerie   | <input type="checkbox" unchecked id="0b8381"> | <input type="checkbox" unchecked id="0638b5"> | <input type="checkbox" unchecked id="6a1848"> | <input type="checkbox" unchecked id="ce543d"> | <input type="checkbox" unchecked id="3fa684"> | <input type="checkbox" unchecked id="5c7d75"> | <input type="checkbox" unchecked id="328e37"> | <input type="checkbox" unchecked id="03ab2e"> | <input type="checkbox" unchecked id="92844a"> | <input type="checkbox" unchecked id="574ab6"> |
| Vixen     | <input type="checkbox" unchecked id="7d0d79"> | <input type="checkbox" unchecked id="d89fc5"> | <input type="checkbox" unchecked id="4c35d7"> | <input type="checkbox" unchecked id="cd3206"> | <input type="checkbox" unchecked id="5974a2"> | <input type="checkbox" unchecked id="4b28fe"> | <input type="checkbox" unchecked id="390139"> | <input type="checkbox" unchecked id="8772d1"> | <input type="checkbox" unchecked id="10a0e8"> | <input type="checkbox" unchecked id="600c7d"> |
| Willow    | <input type="checkbox" unchecked id="c9dfc8"> | <input type="checkbox" unchecked id="220729"> | <input type="checkbox" unchecked id="1af62a"> | <input type="checkbox" unchecked id="106b09"> | <input type="checkbox" unchecked id="1afd2b"> | <input type="checkbox" unchecked id="6bfed1"> | <input type="checkbox" unchecked id="596533"> | <input type="checkbox" unchecked id="95171e"> | <input type="checkbox" unchecked id="ee8e71"> | <input type="checkbox" unchecked id="7f2734"> |
| Birch     | <input type="checkbox" unchecked id="c8e76d"> | <input type="checkbox" unchecked id="157843"> | <input type="checkbox" unchecked id="604c65"> | <input type="checkbox" unchecked id="482f3c"> | <input type="checkbox" unchecked id="232029"> | <input type="checkbox" unchecked id="8bef18"> | <input type="checkbox" unchecked id="8d5df8"> | <input type="checkbox" unchecked id="5a82bd"> | <input type="checkbox" unchecked id="4175a3"> | <input type="checkbox" unchecked id="a509f3"> |
| Ivy       | <input type="checkbox" unchecked id="6a74d0"> | <input type="checkbox" unchecked id="185eb3"> | <input type="checkbox" unchecked id="8efcf5"> | <input type="checkbox" unchecked id="336d4e"> | <input type="checkbox" unchecked id="4f60ba"> | <input type="checkbox" unchecked id="f18219"> | <input type="checkbox" unchecked id="4c6ea2"> | <input type="checkbox" unchecked id="914b4d"> | <input type="checkbox" unchecked id="791caa"> | <input type="checkbox" unchecked id="691945"> |
| Maple     | <input type="checkbox" unchecked id="d98dff"> | <input type="checkbox" unchecked id="bd75b3"> | <input type="checkbox" unchecked id="2470b7"> | <input type="checkbox" unchecked id="5067a8"> | <input type="checkbox" unchecked id="eaf4bd"> | <input type="checkbox" unchecked id="2fdd29"> | <input type="checkbox" unchecked id="f7650d"> | <input type="checkbox" unchecked id="a4132c"> | <input type="checkbox" unchecked id="b4b9d0"> | <input type="checkbox" unchecked id="96bcf4"> |
| Dandelion | <input type="checkbox" unchecked id="bf2666"> | <input type="checkbox" unchecked id="522b62"> | <input type="checkbox" unchecked id="88c282"> | <input type="checkbox" unchecked id="ae8c5d"> | <input type="checkbox" unchecked id="c5154c"> | <input type="checkbox" unchecked id="833f54"> | <input type="checkbox" unchecked id="809c50"> | <input type="checkbox" unchecked id="7ade6a"> | <input type="checkbox" unchecked id="184b83"> | <input type="checkbox" unchecked id="3899b9"> |

---
# Review:

### Written by: 

---
# Watched by:
- [ ] Vanessa
- [ ] Victoria
- [ ] Vivian
- [ ] Varg
- [ ] Valerie
- [ ] Vixen
- [ ] Willow
- [ ] Birch
- [ ] Ivy
- [ ] Maple
- [ ] Dandelion

---
# Notes:

`;
let tabletop_template = `---
title:
release_date:
release_year:
genres:
author:
publisher:
reviewed_by:
image_url:
added: ` + tp.date.now('YYYY-MM-DD HH:mm') + `
type: Game
---
> [!mediacallout] Information
> \`="!"+this.image_url\`
>  # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Authors: \`=this.author\`
> #### Publisher: \`=this.publisher\`
# Description:


---
# Rating:
|           |                       1                       |                       2                       |                       3                       |                       4                       |                       5                       |                       6                       |                       7                       |                       8                       |                       9                       |                      10                       |
| :-------- | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: |
| Vanessa   | <input type="checkbox" unchecked id="d2a388"> | <input type="checkbox" unchecked id="f9d389"> | <input type="checkbox" unchecked id="2ec9d0"> | <input type="checkbox" unchecked id="620412"> | <input type="checkbox" unchecked id="290069"> | <input type="checkbox" unchecked id="1b69d2"> | <input type="checkbox" unchecked id="1d339a"> | <input type="checkbox" unchecked id="468504"> | <input type="checkbox" unchecked id="73c7bf"> | <input type="checkbox" unchecked id="ef9b82"> |
| Victoria  | <input type="checkbox" unchecked id="341f7e"> | <input type="checkbox" unchecked id="d8211f"> | <input type="checkbox" unchecked id="eb1655"> | <input type="checkbox" unchecked id="c24d78"> | <input type="checkbox" unchecked id="293793"> | <input type="checkbox" unchecked id="f12914"> | <input type="checkbox" unchecked id="ea8358"> | <input type="checkbox" unchecked id="12a209"> | <input type="checkbox" unchecked id="c9cd43"> | <input type="checkbox" unchecked id="3d4b63"> |
| Vivian    | <input type="checkbox" unchecked id="a14e0d"> | <input type="checkbox" unchecked id="98af28"> | <input type="checkbox" unchecked id="9b0f7a"> | <input type="checkbox" unchecked id="6565dd"> | <input type="checkbox" unchecked id="1cd32b"> | <input type="checkbox" unchecked id="0bbd76"> | <input type="checkbox" unchecked id="e779d1"> | <input type="checkbox" unchecked id="a5fa15"> | <input type="checkbox" unchecked id="c1d1a6"> | <input type="checkbox" unchecked id="323ba6"> |
| Varg      | <input type="checkbox" unchecked id="71ea86"> | <input type="checkbox" unchecked id="935f47"> | <input type="checkbox" unchecked id="a27747"> | <input type="checkbox" unchecked id="e0723f"> | <input type="checkbox" unchecked id="6673db"> | <input type="checkbox" unchecked id="5bddfe"> | <input type="checkbox" unchecked id="e6e68a"> | <input type="checkbox" unchecked id="123993"> | <input type="checkbox" unchecked id="a5c430"> | <input type="checkbox" unchecked id="3749c2"> |
| Valerie   | <input type="checkbox" unchecked id="0b8381"> | <input type="checkbox" unchecked id="0638b5"> | <input type="checkbox" unchecked id="6a1848"> | <input type="checkbox" unchecked id="ce543d"> | <input type="checkbox" unchecked id="3fa684"> | <input type="checkbox" unchecked id="5c7d75"> | <input type="checkbox" unchecked id="328e37"> | <input type="checkbox" unchecked id="03ab2e"> | <input type="checkbox" unchecked id="92844a"> | <input type="checkbox" unchecked id="574ab6"> |
| Vixen     | <input type="checkbox" unchecked id="7d0d79"> | <input type="checkbox" unchecked id="d89fc5"> | <input type="checkbox" unchecked id="4c35d7"> | <input type="checkbox" unchecked id="cd3206"> | <input type="checkbox" unchecked id="5974a2"> | <input type="checkbox" unchecked id="4b28fe"> | <input type="checkbox" unchecked id="390139"> | <input type="checkbox" unchecked id="8772d1"> | <input type="checkbox" unchecked id="10a0e8"> | <input type="checkbox" unchecked id="600c7d"> |
| Willow    | <input type="checkbox" unchecked id="c9dfc8"> | <input type="checkbox" unchecked id="220729"> | <input type="checkbox" unchecked id="1af62a"> | <input type="checkbox" unchecked id="106b09"> | <input type="checkbox" unchecked id="1afd2b"> | <input type="checkbox" unchecked id="6bfed1"> | <input type="checkbox" unchecked id="596533"> | <input type="checkbox" unchecked id="95171e"> | <input type="checkbox" unchecked id="ee8e71"> | <input type="checkbox" unchecked id="7f2734"> |
| Birch     | <input type="checkbox" unchecked id="c8e76d"> | <input type="checkbox" unchecked id="157843"> | <input type="checkbox" unchecked id="604c65"> | <input type="checkbox" unchecked id="482f3c"> | <input type="checkbox" unchecked id="232029"> | <input type="checkbox" unchecked id="8bef18"> | <input type="checkbox" unchecked id="8d5df8"> | <input type="checkbox" unchecked id="5a82bd"> | <input type="checkbox" unchecked id="4175a3"> | <input type="checkbox" unchecked id="a509f3"> |
| Ivy       | <input type="checkbox" unchecked id="6a74d0"> | <input type="checkbox" unchecked id="185eb3"> | <input type="checkbox" unchecked id="8efcf5"> | <input type="checkbox" unchecked id="336d4e"> | <input type="checkbox" unchecked id="4f60ba"> | <input type="checkbox" unchecked id="f18219"> | <input type="checkbox" unchecked id="4c6ea2"> | <input type="checkbox" unchecked id="914b4d"> | <input type="checkbox" unchecked id="791caa"> | <input type="checkbox" unchecked id="691945"> |
| Maple     | <input type="checkbox" unchecked id="d98dff"> | <input type="checkbox" unchecked id="bd75b3"> | <input type="checkbox" unchecked id="2470b7"> | <input type="checkbox" unchecked id="5067a8"> | <input type="checkbox" unchecked id="eaf4bd"> | <input type="checkbox" unchecked id="2fdd29"> | <input type="checkbox" unchecked id="f7650d"> | <input type="checkbox" unchecked id="a4132c"> | <input type="checkbox" unchecked id="b4b9d0"> | <input type="checkbox" unchecked id="96bcf4"> |
| Dandelion | <input type="checkbox" unchecked id="bf2666"> | <input type="checkbox" unchecked id="522b62"> | <input type="checkbox" unchecked id="88c282"> | <input type="checkbox" unchecked id="ae8c5d"> | <input type="checkbox" unchecked id="c5154c"> | <input type="checkbox" unchecked id="833f54"> | <input type="checkbox" unchecked id="809c50"> | <input type="checkbox" unchecked id="7ade6a"> | <input type="checkbox" unchecked id="184b83"> | <input type="checkbox" unchecked id="3899b9"> |

---
# Review:

### Written by: 

---
# Played by:
- [ ] Vanessa
- [ ] Victoria
- [ ] Vivian
- [ ] Varg
- [ ] Valerie
- [ ] Vixen
- [ ] Willow
- [ ] Birch
- [ ] Ivy
- [ ] Maple
- [ ] Dandelion

---
# Notes:

`;
let music_template = `---
title:
release_date:
release_year:
genres:
author:
publisher:
tracks:
runtime:
reviewed_by:
image_url:
added: ` + tp.date.now('YYYY-MM-DD HH:mm') + `
type: Game
---
> [!mediacallout] Information
> \`="!"+this.image_url\`
>  # Title: \`=this.title\`
> #### Date of release: \`=this.release_date\`
> #### Genres: \`=this.genres\`
> #### Authors: \`=this.author\`
> #### Publisher: \`=this.publisher\`
> #### Amount of tracks: \`=this.tracks\`
> #### Total runtime: \`=this.runtime\`
# Description:


---
# Rating:
|           |                       1                       |                       2                       |                       3                       |                       4                       |                       5                       |                       6                       |                       7                       |                       8                       |                       9                       |                      10                       |
| :-------- | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: |
| Vanessa   | <input type="checkbox" unchecked id="d2a388"> | <input type="checkbox" unchecked id="f9d389"> | <input type="checkbox" unchecked id="2ec9d0"> | <input type="checkbox" unchecked id="620412"> | <input type="checkbox" unchecked id="290069"> | <input type="checkbox" unchecked id="1b69d2"> | <input type="checkbox" unchecked id="1d339a"> | <input type="checkbox" unchecked id="468504"> | <input type="checkbox" unchecked id="73c7bf"> | <input type="checkbox" unchecked id="ef9b82"> |
| Victoria  | <input type="checkbox" unchecked id="341f7e"> | <input type="checkbox" unchecked id="d8211f"> | <input type="checkbox" unchecked id="eb1655"> | <input type="checkbox" unchecked id="c24d78"> | <input type="checkbox" unchecked id="293793"> | <input type="checkbox" unchecked id="f12914"> | <input type="checkbox" unchecked id="ea8358"> | <input type="checkbox" unchecked id="12a209"> | <input type="checkbox" unchecked id="c9cd43"> | <input type="checkbox" unchecked id="3d4b63"> |
| Vivian    | <input type="checkbox" unchecked id="a14e0d"> | <input type="checkbox" unchecked id="98af28"> | <input type="checkbox" unchecked id="9b0f7a"> | <input type="checkbox" unchecked id="6565dd"> | <input type="checkbox" unchecked id="1cd32b"> | <input type="checkbox" unchecked id="0bbd76"> | <input type="checkbox" unchecked id="e779d1"> | <input type="checkbox" unchecked id="a5fa15"> | <input type="checkbox" unchecked id="c1d1a6"> | <input type="checkbox" unchecked id="323ba6"> |
| Varg      | <input type="checkbox" unchecked id="71ea86"> | <input type="checkbox" unchecked id="935f47"> | <input type="checkbox" unchecked id="a27747"> | <input type="checkbox" unchecked id="e0723f"> | <input type="checkbox" unchecked id="6673db"> | <input type="checkbox" unchecked id="5bddfe"> | <input type="checkbox" unchecked id="e6e68a"> | <input type="checkbox" unchecked id="123993"> | <input type="checkbox" unchecked id="a5c430"> | <input type="checkbox" unchecked id="3749c2"> |
| Valerie   | <input type="checkbox" unchecked id="0b8381"> | <input type="checkbox" unchecked id="0638b5"> | <input type="checkbox" unchecked id="6a1848"> | <input type="checkbox" unchecked id="ce543d"> | <input type="checkbox" unchecked id="3fa684"> | <input type="checkbox" unchecked id="5c7d75"> | <input type="checkbox" unchecked id="328e37"> | <input type="checkbox" unchecked id="03ab2e"> | <input type="checkbox" unchecked id="92844a"> | <input type="checkbox" unchecked id="574ab6"> |
| Vixen     | <input type="checkbox" unchecked id="7d0d79"> | <input type="checkbox" unchecked id="d89fc5"> | <input type="checkbox" unchecked id="4c35d7"> | <input type="checkbox" unchecked id="cd3206"> | <input type="checkbox" unchecked id="5974a2"> | <input type="checkbox" unchecked id="4b28fe"> | <input type="checkbox" unchecked id="390139"> | <input type="checkbox" unchecked id="8772d1"> | <input type="checkbox" unchecked id="10a0e8"> | <input type="checkbox" unchecked id="600c7d"> |
| Willow    | <input type="checkbox" unchecked id="c9dfc8"> | <input type="checkbox" unchecked id="220729"> | <input type="checkbox" unchecked id="1af62a"> | <input type="checkbox" unchecked id="106b09"> | <input type="checkbox" unchecked id="1afd2b"> | <input type="checkbox" unchecked id="6bfed1"> | <input type="checkbox" unchecked id="596533"> | <input type="checkbox" unchecked id="95171e"> | <input type="checkbox" unchecked id="ee8e71"> | <input type="checkbox" unchecked id="7f2734"> |
| Birch     | <input type="checkbox" unchecked id="c8e76d"> | <input type="checkbox" unchecked id="157843"> | <input type="checkbox" unchecked id="604c65"> | <input type="checkbox" unchecked id="482f3c"> | <input type="checkbox" unchecked id="232029"> | <input type="checkbox" unchecked id="8bef18"> | <input type="checkbox" unchecked id="8d5df8"> | <input type="checkbox" unchecked id="5a82bd"> | <input type="checkbox" unchecked id="4175a3"> | <input type="checkbox" unchecked id="a509f3"> |
| Ivy       | <input type="checkbox" unchecked id="6a74d0"> | <input type="checkbox" unchecked id="185eb3"> | <input type="checkbox" unchecked id="8efcf5"> | <input type="checkbox" unchecked id="336d4e"> | <input type="checkbox" unchecked id="4f60ba"> | <input type="checkbox" unchecked id="f18219"> | <input type="checkbox" unchecked id="4c6ea2"> | <input type="checkbox" unchecked id="914b4d"> | <input type="checkbox" unchecked id="791caa"> | <input type="checkbox" unchecked id="691945"> |
| Maple     | <input type="checkbox" unchecked id="d98dff"> | <input type="checkbox" unchecked id="bd75b3"> | <input type="checkbox" unchecked id="2470b7"> | <input type="checkbox" unchecked id="5067a8"> | <input type="checkbox" unchecked id="eaf4bd"> | <input type="checkbox" unchecked id="2fdd29"> | <input type="checkbox" unchecked id="f7650d"> | <input type="checkbox" unchecked id="a4132c"> | <input type="checkbox" unchecked id="b4b9d0"> | <input type="checkbox" unchecked id="96bcf4"> |
| Dandelion | <input type="checkbox" unchecked id="bf2666"> | <input type="checkbox" unchecked id="522b62"> | <input type="checkbox" unchecked id="88c282"> | <input type="checkbox" unchecked id="ae8c5d"> | <input type="checkbox" unchecked id="c5154c"> | <input type="checkbox" unchecked id="833f54"> | <input type="checkbox" unchecked id="809c50"> | <input type="checkbox" unchecked id="7ade6a"> | <input type="checkbox" unchecked id="184b83"> | <input type="checkbox" unchecked id="3899b9"> |

---
# Review:

### Written by: 

---
# Played by:
- [ ] Vanessa
- [ ] Victoria
- [ ] Vivian
- [ ] Varg
- [ ] Valerie
- [ ] Vixen
- [ ] Willow
- [ ] Birch
- [ ] Ivy
- [ ] Maple
- [ ] Dandelion

---
# Notes:

`;
let document;

function get_folder() {
	const path = tp.file.folder(true).split('/');
	const folder = path[1];

	let folder_name = folder.split(' ');
	let trimmed = folder_name[2];

	switch (trimmed) {
	case "Movies":
		return movie_template;
		break;
	case "Shows":
		return show_template;
		break;
	case "Music":
		return music_template;
		break;
	case "Games":
		return game_template;
		break;
	case "Books":
		return book_template;
		break;
	case "Comics":
		return comic_template;
		break;
	case "Manga":
		return manga_template;
		break;
	case "Tabletops":
		return tabletop_template;
		break;
	default:
		return "";
	}
}

document = get_folder();
-%>
<% document %>