+++
title = "How To Add KaTeX"
date = "2022-09-16T09:48:56-04:00"
author = "Samuel Jones"
tags = ["Hugo", "KaTeX", "LaTeX"]
description = "How to add KaTeX to a Hugo site"
showFullContent = false
readingTime = true
hideComments = false
katex = true
+++
Hugo doesen't ship with a LaTeX renderer. If you wan't to render it, you need 3rd party library for it, like [KaTeX](https://katex.org/).

# Adding a Partial Template
- To add a partial template, create an empty html file: ```themes/{your_theme}/layouts/partials/katex.html```.
- Open your partial file and follow the [guide provided by KaTeX](https://katex.org/docs/browser.html):
```html
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.2/dist/katex.min.css" integrity="sha384-bYdxxUwYipFNohQlHt0bjN/LCpueqWz13HufFEV1SUatKs1cm4L6fFgCi1jT643X" crossorigin="anonymous">
    <script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.2/dist/katex.min.js" integrity="sha384-Qsn9KnoKISj6dI8g7p1HBlNpVx0I8p1SvlwOldgi3IorMle61nQy4zEahWYtljaz" crossorigin="anonymous"></script>
    <script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.2/dist/contrib/auto-render.min.js" integrity="sha384-+VBxd3r6XgURycqtZ117nYw44OOcIax56Z4dCRWbxyPt0Koah1uHoK0o4+/RRE05" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
```

- Open your head partial (```themes/{your_theme}/layouts/partials/head.html```) and add the following to render when _katex_ is set to true in the frontmatter:
```
{{ if or .Params.katex .Site.Params.katex }}
  {{ partial "katex.html" . }}
{{ end }}
```

Alternatively, if you want it always to render, paste the following:
```
{{ partial "katex.html" . }}
```

# Results
Once, KaTeX is loaded on a page, you can write and render LaTeX. Here is an example: $$\int_{a}^{b} x^2 dx$$