## Lecture 3 - Mongo DB

Написать запрос для поиска всех студентов, у которых score > 87% и < 93% по любому из типов выполненных заданий.

```js
db.users.find({
  scores: {
    $elemMatch: {
      score: {
        $gt: 87,
        $lt: 93
      }
    }
  }
})
```

Написать запрос-агрегацию для выборки всех студентов, у которых результат по экзамену (type: "exam") более 90% (использование unwind)

```js
```

Студентам с именем Dusti Lemmond добавить поле “accepted” со значением true.

```js
db.users.updateMany({
  name: 'Dusti Lemmond'
}, {
  $set: {
    accepted: true
  }
})
```
