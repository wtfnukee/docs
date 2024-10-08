# Как получать чеки при совершении платежа с банковской карты


## Описание сценария {#case-description}

Необходимо получить чек об оплате после совершения платежа.

## Решение {#case-resolution}

Возможность получения чека зависит от страны резиденства вашего платежного аккаунта:

{% list tabs %}

- Резиденты РФ и РК
    
    В соответствии с № 54-ФЗ «О применении контрольно-кассовой техники» после оплаты ресурсов с помощью банковской карты вы получаете чек об оплате по электронной почте. Адрес указан в [Консоли управления]({{ link-console-settings }}) у владельца платежного аккаунта.

    Чек об оплате — первичный учетный документ, подтверждающий перевод денежных средств с помощью банковской карты. Мы рекомендуем хранить все чеки — это поможет разобраться, если c каким-либо платежом возникнут проблемы.

    Сумма чека соответствует сумме, списанной с привязанной банковской карты. Подробнее – в нашей [документации](../../../billing/concepts/individual-bill.md).

- Нерезиденты РФ и РК
    
    Согласно [договору-оферте]({{ billing-oferta-url }}) п.6.4, {{ yandex-cloud }} предоставляет для таких аккаунтов инвойс на сумму потребления. В этом случае чек на оплату не формируется.

{% endlist %}
