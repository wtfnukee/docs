# Как узнать скорость доступа к дискам виртуальной машины


## Описание сценария {#case-description}

Необходимо узнать скорость доступа к дискам виртуальной машины и что на нее влияет.

## Решение {#case-resolution}

Скорость определяют тип диска, физический размер блока и размер диска. Подробнее про это можно прочитать в [документации](../../../compute/concepts/disk.md#performance).

{% note info %}

На скорость доступа к дискам не влияет, загрузочный ли диск или дополнительный. 

{% endnote %}

Диски ограничены лимитами на IOPS и пропускную способность. Подробнее об этом можно прочитать [здесь](../../../compute/concepts/limits.md#limits-disks).  

Для получения максимального значения IOPS рекомендуется делать чтения и записи размером не более 4 КБ, а чтобы получить максимальное значение пропускной способности — до 4 МБ. 
