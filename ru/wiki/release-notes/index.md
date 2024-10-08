---
title: "История изменений в {{ wiki-full-name }} в феврале 2024"
description: "Ознакомьтесь с историей изменений в {{ wiki-full-name }} за февраль 2024."
---

# История изменений в {{ wiki-full-name }} в феврале 2024

* [Сортировка в блоке tree](#edit-tree-sort)
* [Преобразование заголовка в параграф](#title-paragraph-convert)

## Сортировка в блоке <q>tree</q> {#edit-tree-sort}

В новом редакторе появилась возможность сортировки страниц раздела в блоке [tree](../actions/page-lists.md#tree). Для этого:

1. В описании блока добавьте параметр `sort_by` и укажите поле для сортировки:

   * `title` — по заголовку;
   * `cluster` — по разделу;
   * `created_at` — по дате создания;
   * `modified_at` — по дате изменения.

1. (опционально) Укажите порядок сортировки в параметре `sort`:

   * `asc` — по возрастанию;
   * `desc` — по убыванию.

Например, для сортировки по заголовку по убыванию:

```text
{{ tree sort_by="title" sort="desc"}}
```

## Преобразование заголовка в текст {#title-paragraph-convert}

В новом редакторе при [форматировании текста](../wysiwyg/text-format.md#format-wysiwyg) происходит преобразование заголовка в текст при повторном выборе для него заголовка того же уровня.

Выбор уровня ![](../../_assets/console-icons/text.svg) **Текст** теперь доступен после нажатия кнопки ![](../../_assets/console-icons/heading.svg) ![](../../_assets/console-icons/chevron-down.svg) на панели инструментов.