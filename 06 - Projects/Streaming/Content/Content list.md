## Streaming
```dataview
TABLE WITHOUT ID
file.link AS "Name",
file.frontmatter.status AS "Status"
FROM "06 - Projects/Streaming/Content/Streaming"
WHERE file.frontmatter.main = "1"
SORT file.frontmatter.status ASC
```
---
## Videos
```dataview
TABLE WITHOUT ID
file.link AS "Name",
file.frontmatter.status AS "Status"
FROM "06 - Projects/Streaming/Content/Videos"
WHERE file.frontmatter.main = "1"
SORT file.frontmatter.status ASC
```
---
## Shorts
```dataview
TABLE WITHOUT ID
file.link AS "Name",
file.frontmatter.status AS "Status"
FROM "06 - Projects/Streaming/Content/Shorts"
WHERE file.frontmatter.main = "1"
SORT file.frontmatter.status ASC
```
---
## Music
```dataview
TABLE WITHOUT ID
file.link AS "Name",
file.frontmatter.status AS "Status"
FROM "06 - Projects/Streaming/Content/Music"
WHERE file.frontmatter.main = "1"
SORT file.frontmatter.status ASC
```
---
## Misc
```dataview
TABLE WITHOUT ID
file.link AS "Name",
file.frontmatter.status AS "Status"
FROM "06 - Projects/Streaming/Content/Misc"
WHERE file.frontmatter.main = "1"
SORT file.frontmatter.status ASC
```
