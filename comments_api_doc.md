## Комментарии (/comments)

#### GET:
Получение _всех_ комментариев

**Пример запроса**: 

/comments

**Ответ сервера**:

```json
[
    {
        "comment_id": "_1gtbcnde4",
        "text": "Вежливый персонал, низкие цены. Пять баллов!",
        "likes": 7
    },
    {
        "comment_id": "_d59ks928d",
        "text": "Отличный магазин! Быстрая доставка!",
        "likes": 1
    }
]
```

---

#### POST
Добавление комментария

**Параметры запроса**:
- text

**Пример запроса**: 

/comments?**text=Отличный магазин! Быстрая доставка!**

**Ответ сервера**:

Информация о созданном комментарии
```json
{
    "comment_id": "_d59ks928d",
    "text": "Отличный магазин! Быстрая доставка!",
    "likes": 0
}
```

---

#### PATCH
Лайк комментария

**Параметры запроса**:
- comment_id

**Пример запроса**: 

/comments?**comment_id=_d59ks928d**

**Ответ сервера**:

Информация об оценённом комментарии (с новым количеством лайков)
```json
{
    "comment_id": "_d59ks928d",
    "text": "Отличный магазин! Быстрая доставка!",
    "likes": 1
}
```

---

#### DELETE
Удаление комментария

**Параметры запроса**:
- comment_id

**Пример запроса**: 

/comments?**comment_id=_d59ks928d**

**Ответ сервера**:

Информация об удалённом комментарии
```json
{
    "comment_id": "_d59ks928d",
    "text": "Отличный магазин! Быстрая доставка!",
    "likes": 1
}
```