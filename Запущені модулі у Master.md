---
Type: fact
tags: 
Data: 2023-12-06
---
це структура запущених модулів в [[Карта Master]] яка зберігається в [[База даних]]
Поясню за поля
1. hash: це унікальний код модуля
2. name_container: це назва контейнера докера
3. hash_tamplate: це вказівник на шаблон( [[Шаблони модулів у Master]] ) по якому був створений цей модуль
4. name: це назва який дає [[Master Client]]
5. name_node: це назва вузла на якому запускається модуль([[RESTConnector]],[[RESTServer]])
6. connections: це масив інших модулів з яким пов'язаний цей модуль
### Це приклад реального запущеного модуля
```json
{
       "hash":"3xw1",
      "name_container": "Gpt",
      "hash_tamplate":"2xd2",
      "name":"gpt",
      "name_node":"niger",
      "connections": ["3xw3"]
    }
```
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