---
Type: fact
tags: 
Data: 2023-12-06
---
Карта [[Master]] це карта де записані всі модулі([[Server Logic]],[[Connector Manager]]) їхні зв'язки та тд. Це потрібно для того щоб знаходити найшвидший шлях до конкретного поду([[Connector Manager]]). Це дає [[Оптимізація]]. Також потім там буде розрахування по завантаженню [[Server Logic]] та шукатись оптимальний шлях. 
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