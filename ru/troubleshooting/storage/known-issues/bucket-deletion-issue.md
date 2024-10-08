# Устранение ошибки `Bucket is not empty` при удалении бакета


## Описание проблемы {#issue-description}

При попытке удалить бакет появляется сообщение об ошибке `Bucket is not empty`.

## Решение {#issue-resolution}

Для удаления каталога или бакета необходимо сначала удалить из него все объекты. Самые распространенные причины невозможности удалить бакет:

* В бакете есть незавершенные составные загрузки;
* В бакете остались загруженные объекты;
* В бакете удалены все объекты, но в нем включено версионирование и существуют старые версии удаленных объектов.

Вы можете удалить все старые версии объектов и незавершенные загрузки, настроив автоматическое удаление всех этих сущностей в правиле жизненного цикла бакета.

{% note info %}

Правила жизненного цикла обрабатываются в 00:00 UTC один раз в сутки.

{% endnote %}

{% list tabs %}

- Консоль управления

  Посмотреть и удалить незавершенные загрузки из [Консоли управлени]({{ link-console-main }}) можно [по этой инструкции](../../../storage/operations/objects/deleting-multipart.md).

  Удаление всех объектов из бакета средствами консоли управления описано в материале [по этой ссылке](../../../storage/operations/objects/delete-all.md).

- AWS CLI

  * Наличие незавершенных составных загрузок можно проверить командой:

    ```bash
    aws --endpoint <https://storage.yandexcloud.net> s3api list-multipart-uploads \
    --bucket \<bucket_name\>
    ```

  * Удалить такие загрузки можно командой `abort-multipart-upload`:

    ```bash
    aws --endpoint <https://storage.yandexcloud.net> s3api abort-multipart-upload \
    --bucket \<bucket_name\> --key \<object_key\> --upload-id \<upload_id\>
    ```

  * Наличие объектов в бакете можно проверить командой `list-objects`:

    ```bash
    aws --endpoint <https://storage.yandexcloud.net> s3api list-objects \
    --bucket \<bucket_name\>
    ```

  * Удалить один объект можно командой `delete-object`:

    ```bash
    aws --endpoint <https://storage.yandexcloud.net> s3api delete-object \
    --bucket \<bucket_name\> --key
    ```

  * Удалить сразу несколько объектов можно командой `delete-object`:

    ```bash
    aws --endpoint <https://storage.yandexcloud.net> s3api delete-objects \
    --bucket \<bucket_name\> --delete '\{ "Objects": \[ \{ "Key": \}, \{ "Key": \}, ...\] \}'
    ```

  * Если в вашем бакете включено версионирование, то после удаления самих объектов в каталоге или бакете все еще хранятся их прошлые версии. Их тоже необходимо удалить. Увидеть старые версии можно так:

    ```bash
    aws --endpoint <https://storage.yandexcloud.net> s3api list-object-versions \
    --bucket \<bucket_name\>

  * Удалить конкретную версию объекта можно командой:

    ```bash
    aws --endpoint <https://storage.yandexcloud.net> s3api delete-object \
    --bucket \<bucket_name\> --key \<key_name\> --version-id \<version_id\>
    ```

{% endlist %}