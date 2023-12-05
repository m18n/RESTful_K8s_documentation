---
Type: fact
tags: 
Data: 2023-12-06
---
Карта [[Master]] це карта де записані всі модулі([[Server Logic]],[[Connector Manager]]) їхні зв'язки та тд. Це потрібно для того щоб знаходити найшвидший шлях до конкретного поду([[Connector Manager]]). Це дає [[Оптимізація]]. Також потім там буде розрахування по завантаженню [[Server Logic]] та шукатись оптимальний шлях. 
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