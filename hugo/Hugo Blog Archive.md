Create a page archive.md in you content folder.
Insert this as the top of the page.

```
---
title: "Archive"
layout: archive
---
```
Create a page archive.html.
Paste this in archive.html.

```
{{ with .Site.GetPage "section" "posts" }}
{{ range .Data.Pages.GroupByDate "2006-01" }}
<h3>{{ .Key }}</h3>
{{ range .Pages }}
<archivetitle><a href={{ .Permalink }}>{{ .Title }}</a></archivetitle>
<div class=date><a href={{ .Permalink }}>{{ .Date.Format "Monday, Jan 2, 2006" }}</a></div>
{{ end }}
{{ end }}
{{ end }}
```

This will result in a list with all your blog posts with a nice year-month divider before each month.

If you want a yearly archive, replace this line

```
{{ range .Data.Pages.GroupByDate "2006-01" }}
```

with this line

```
{{ range .Data.Pages.GroupByDate "2006" }}
```
