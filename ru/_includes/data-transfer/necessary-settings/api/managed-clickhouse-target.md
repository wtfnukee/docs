* {% include [Field API Security Group](../../fields/common/api/security-groups.md) %}

   Убедитесь, что указанные группы безопасности [настроены](../../../../managed-clickhouse/operations/connect/index.md#configuring-security-groups).

* {% include [Field API Cluster ID](../../fields/common/api/mdb-cluster-id.md) %}
* `clickhouseClusterName` — группа шардов, в которую будут передаваться данные. Если параметр не указан, данные будут размещены во всех шардах.
* {% include [Field API Database](../../fields/common/api/database.md) %}
* {% include [Field API User](../../fields/common/api/user.md) %}
* {% include [Field API Password](../../fields/common/api/password.md) %}
