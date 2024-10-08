---
title: "How to create a {{ mgl-full-name }} instance"
description: "In this tutorial, you will learn how to create a {{ mgl-name }} instance."
---

# Creating and activating a {{ mgl-name }} instance

## Creating a {{ GL }} instance {#create}

To create a {{ mgl-name }} instance, you need the [{{ roles-vpc-user }}](../../../vpc/security/index.md#vpc-user) role and the [{{ roles.gitlab.editor }} role or higher](../../security/index.md#roles-list). For information on assigning roles, see the [{{ iam-name }} documentation](../../../iam/operations/roles/grant.md).

{% list tabs group=instructions %}

- Management console {#console}

  {% include [instance-create-console](../../../_includes/managed-gitlab/instance-create-console.md) %}

{% endlist %}

{% include [HTTPS info](../../../_includes/managed-gitlab/note-https.md) %}

## Activating the {{ GL }} instance {#activate}

After the instance status changes to **Running**, activate the instance:

1. Follow the link you received in your administrator mailbox after creating the instance.

   If you cannot open the {{ GL }} web interface, create a separate security group and [configure it](../configure-security-group.md) so that the rules allow incoming traffic from the required ports and IP addresses.

1. Change the administrator password.
1. Log in using the administrator username and password.

Further on, to open the {{ GL }} web interface, [get detailed information about your instance](instance-list.md#get) and follow the link in **{{ ui-key.yacloud.gitlab.field_domain }}**.
