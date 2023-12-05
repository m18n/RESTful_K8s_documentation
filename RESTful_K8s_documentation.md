---
Type: 
tags: 
Data: 2023-12-05
---
Цей проект складається з двух частин [[Server Logic]] і [[Connector Manager]]
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