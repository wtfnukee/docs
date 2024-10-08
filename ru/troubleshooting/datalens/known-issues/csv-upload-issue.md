# Устранение проблем при загрузке CSV-файла в датасет в качестве источника данных


## Описание проблемы {#issue-description}

При попытке загрузить файл в формате CSV в качестве источника данных для датасета отображается сообщение `Не удалось загрузить файл` или возникает ошибка `ERR.FILE.PARSE_FAILED`.

## Решение {#issue-resolution}

1. Проверьте кодировку данных вашего CSV-файла — поддерживаются кодировки UTF-8, UTF-16, Windows-1251 и UTF-8-Sig.
1. Проверьте корректность разделителей столбцов в файле, а также их наличие во всем содержимом от начала и до конца файла. Сейчас поддерживаются запятая (`,`), точка с запятой (`;`) и знак табуляции.
1. Загрузите файл заново, выполнив следующие действия:

    * Отключите блокировщики рекламы в браузере;
    * Перейдите на страницу с датасетом {{ datalens-name }} в режиме инкогнито;
    * Воспользуйтесь другим браузером.

## Если проблема осталась {#if-issue-still-persists}

Если вышеописанные рекомендации не помогли решить проблему, [создайте запрос в техническую поддержку]({{ link-console-support }}). При создании запроса укажите следующую информацию:

1. Ссылку на проблемный датасет.
1. [HAR-файл](../../../support/create-har), собранный при попытке добавления связанной таблицы в датасет.
1. CSV-файл, который вы пытаетесь загрузить в датасет в качестве источника данных.

{% note alert %}

Перед отправкой CSV-файла в техническую поддержку не забудьте исключить из него чувствительные данные.

{% endnote %}
