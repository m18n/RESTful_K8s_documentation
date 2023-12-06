---
Type: fact
tags: 
Data: 2023-12-06
---
[[RESTServer]] складається з Crow(це веб сервер) та коду який менеджер завдань. Та приймає від [[RESTConnector]] запити
## Facts
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
AND contains(Type, "fact")
```
## Topics
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
AND contains(Type, "topic")
```
## Ideas
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
AND contains(Type, "idea")
```
## Questions
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
AND contains(Type, "question")
```
## Answers
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
AND contains(Type, "answer")
```
## Bugs
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
AND contains(Type, "bug")
```
## Fixs
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
AND contains(Type, "fix")
```
## Tasks
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
AND contains(Type, "task")
```
## Roots
```dataview
LIST FROM ""
WHERE contains(file.inlinks.file.name, this.file.name)
```

## Childs
```dataview
LIST FROM ""
WHERE contains(file.outlinks.file.name, this.file.name)
```