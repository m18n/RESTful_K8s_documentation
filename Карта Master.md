---
Type: fact
tags: 
Data: 2023-12-06
---
Карта [[Master Server]] це карта де записані всі модулі([[RESTServer]],[[RESTConnector]]) їхні зв'язки та тд. Всі записи будуть в [[База даних]]. Це потрібно для того щоб знаходити найшвидший шлях до конкретного поду([[RESTConnector]]). Це дає [[Оптимізація]]. Також потім там буде розрахування по завантаженню [[RESTServer]] та шукатись оптимальний шлях.
Зв'язки можна подивитись в [[Приклад схеми комунікацій]]
[[Комунікація між модулями]]
В карті будуть зберігатись [[Шаблони модулів у Master]] по яким будуть створюватись [[Запущені модулі у Master]]
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