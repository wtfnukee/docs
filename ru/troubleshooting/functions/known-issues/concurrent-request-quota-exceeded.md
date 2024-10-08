
# Устранение ошибки `No node can serve the request (concurrent requests exceeded)`


## Описание проблемы {#issue-description}

При попытке вызова функции {{ sf-name }} код функции не выполняется, а в логах выполнения функции появляется сообщение:

```
 429 Message: No node can serve the request: Concurrent requests exceeded` 
```

## Решение {#issue-resolution}

Эта ошибка связана с превышением одной или нескольких квот из этого списка:

* **Количество одновременных операций над функциями и версиями в облаке**;
* **Количество одновременных операций над одной функцией и ее версиями**;
* **Количество одновременных вызовов**.

Проверьте текущее потребление по указанным выше квотам [в консоли управления]({{ link-console-quotas }}) и при необходимости сформируйте запрос на увеличение уровня квот в вашем облаке.

## Если проблема осталась {#if-issue-still-persists}

Если вышеописанные действия не помогли решить проблему, [создайте запрос в техническую поддержку]({{ link-console-support }}). При создании запроса укажите следующую информацию:

1. Идентификатор облачной функции или контейнера {{ serverless-containers-name }}.
1. Полный текст сообщения об ошибке из лога облачной функции или контейнера.