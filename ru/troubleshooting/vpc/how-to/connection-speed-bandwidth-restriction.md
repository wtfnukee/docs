# Существуют ли ограничения трафика, скорости соединения и ширины канала


## Описание сценария {#case-description}

Необходимо узнать, ограничивает ли {{ vpc-name }} трафик, скорость соединения или ширину канала.

## Решение {#case-resolution}

{{ vpc-name }} не ограничивает ширину канала, количество трафика и скорость соединения. Единственные ограничения сети, с которыми может столкнуться пользователь, – это ограничения на каналах вне зоны нашей ответственности. 

Мы тарифицируем только исходящий трафик сверх 100 ГБ в месяц. Расценки можно посмотреть [здесь](../../../vpc/pricing.md).
