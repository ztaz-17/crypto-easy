New-Item -Path "content/index.md" -ItemType File -Value @"

\---

title: "Test page"

layout: "index"

\---



\# Тестовая страница



Это тестовая страница на Hugo.  

Локально: `hugo server`  

Сборка: `hugo`

"@

