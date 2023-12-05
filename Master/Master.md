---
Type: topic
tags: 
Data: 2023-12-06
---
Цей модуль являється мастер тому що він роздає всі карти розтушування модулів у [[Server Logic]] і [[Connector Manager]] в [[kubernetes]]. 
## Idea
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
AND contains(Type, "idea")
```
## Question
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
AND contains(Type, "question")
```
## Answer
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
AND contains(Type, "answer")
```
## Bug
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
AND contains(Type, "bug")
```
## Fix
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
AND contains(Type, "fix")
```
## Root
```dataview
LIST FROM ""
WHERE contains(file.inlinks.file.name, this.file.name)
```

## Child
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
```