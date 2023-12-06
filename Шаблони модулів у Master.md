---
Type: fact
tags: 
Data: 2023-12-06
---
це структура шаблона модулів([[Connector Manager]],[[Server Logic]]) в [[Карта Master]] яка зберігається в [[База даних]]
Та це шаблон по якому створюються [[Запущені модулів у Master]]
Поясню за поля
1. hash_tamplate: це унікальний код шаблона 
2. name_container: це назва контейнера докера
3. name_node: це вказівник на [[Приклад шаблона у базі даних]] по якому був створений цей модуль
5. name: це назва яка дадуть модулю
6. count: це кількість модулів яка має бути запущена 
7. connections: це масив інших модулів з яким пов'язаний цей модуль
### Це приклад реального запущеного модуля
```json
{
      "hash_tamplate":"2xde",
      "name_container": "Tasker",
      "name_node":"test",
      "name":"Local Tasker",
      "count":"1",
      "connections": [""]
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