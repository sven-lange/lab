+++
date = '{{ .Date }}'
draft = true
title = '{{ replace .File.ContentBaseName "-" " " | title }}'
showAuthor = false
showDate = false
showReadingTime = false
[build]
  render = "never"
  list = "local"
[params]
  year = 2026
  authorsDisplay = ""
  authorNotes = "" # optional, for symbols like * co-first, # corresponding
  journal = ""
  doi = ""
+++
