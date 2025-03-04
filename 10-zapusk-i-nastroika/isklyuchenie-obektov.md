---
description: Инструкция по настройке функции исключения объектов во время печати
---

# 🛑 Исключение объектов

{% embed url="https://www.klipper3d.org/Config_Reference.html#exclude_object" %}

## 01. Настройка

### Настройки принтера

В файл printer.cfg добавляем строчку:

```django
[exclude_object]
```

Сохраняем и перезагружаем.

В файле moonraker.conf добавляем сточку в секцию \[file\_manager]:

```django
enable_object_processing: True
```

Сохраняем и перезагружаем.

## 02. Использование

Слайсим g-код в Cura.

Закидываем на принтер и ставим его на печать.

После начала печати появится кнопка "Исключить объект":

<figure><img src="../.gitbook/assets/Снимок экрана 2024-02-18 010344.png" alt=""><figcaption></figcaption></figure>

При нажатии на неё откроется меню с выбором объектов:

<figure><img src="../.gitbook/assets/Снимок экрана 2024-02-18 010346.png" alt=""><figcaption></figcaption></figure>

Во время печати в этом меню мы выбираем объект, который хотим исключить (например отвалилась поддержка или отлипла деталь).

Также исключить объект можно ниже в секции "Предосмотр GCode".&#x20;

<figure><img src="../.gitbook/assets/Снимок экрана 2024-02-18 010512.png" alt=""><figcaption></figcaption></figure>

Щелкнув левой кнопкой мыши по детали вылезет вслывающее окно с подтверждением исключения:

<figure><img src="../.gitbook/assets/Снимок экрана 2024-02-18 010518.png" alt=""><figcaption></figcaption></figure>

После исключения объекта, принтер перестанет его печатать, но продолжит печатать остальные детали.
