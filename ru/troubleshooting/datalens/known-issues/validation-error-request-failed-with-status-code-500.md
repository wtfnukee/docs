# Устранение ошибки `Validation error Request failed with status code 500` при сохранении дашборда


## Описание проблемы {#issue-description}

При сохранении дашборда возникает ошибка:

```text
Validation error
"Error: Request failed with status code 500 
at t.exports (https://yastatic.net/s3/cloud/datalens/static/freeze/js/vendors.1108fcc0.js:2:6017)
at t.exports (https://yastatic.net/s3/cloud/datalens/static/freeze/js/vendors.1108fcc0.js:2:8466)
at XMLHttpRequest.y (https://yastatic.net/s3/cloud/datalens/static/freeze/js/vendors.1108fcc0.js:2:1286)"
```

## Решение {#issue-resolution}

Для имени дашборда можно использовать только следующие символы: 

* Прописные и строчные буквы латиницы или кириллицы;
* Цифры;
* Дефис, точку и пробел.

Попробуйте изменить название дашборда, если в нем присутствуют символы не из разрешенного списка.

## Если проблема осталась {#if-issue-still-persists}

Если вышеописанные рекомендации не помогли решить проблему, [создайте запрос в техническую поддержку]({{ link-console-support }}). При создании запроса укажите следующую информацию:

1. Ссылку на проблемный дашборд.
1. [HAR-файл](../../../support/create-har), собранный при попытке добавления связанной таблицы в датасет.
