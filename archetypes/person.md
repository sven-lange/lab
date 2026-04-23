+++
date = '{{ .Date }}'
draft = true
title = '{{ replace .File.ContentBaseName "-" " " | title }}'
summary = ''
showDate = false
showAuthor = false
showReadingTime = false
showTableOfContents = false
featured = ""
[build]
  render = "never"
  list = "local"
[params]
  role = ""
  email = ""
  links = []
+++

Write a short bio here.
