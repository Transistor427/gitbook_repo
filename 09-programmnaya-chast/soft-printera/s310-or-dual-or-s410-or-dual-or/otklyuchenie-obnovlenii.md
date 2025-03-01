---
description: Инструкиция по отключению обновлений программного обеспечения принтера
---

# 🔼 Отключение обновлений

## Отключение системных обновлений

{% hint style="info" %}
[https://moonraker.readthedocs.io/en/latest/configuration/](https://moonraker.readthedocs.io/en/latest/configuration/)

Секция \[update\_manager]
{% endhint %}

<figure><img src="../../../.gitbook/assets/изображение (259).png" alt="" width="188"><figcaption></figcaption></figure>

Для отлюкчения системных обновлений одноплатного компьютера в файле **moonraker.conf** в секции \[**update\_manager**] необходимо добавить параметр, который включает (True) или выключает (False) системные обновления:

```django
[update_manager]
enable_auto_refresh: True
enable_repo_debug: True
enable_system_updates: False
```

Должно получиться как на фото:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-03-20 143000.png" alt="" width="176"><figcaption></figcaption></figure>

Если обновления выключены, то в веб-интерфейсе пропадет сторочка с системными обновлениями:

<figure><img src="../../../.gitbook/assets/изображение (260).png" alt="" width="375"><figcaption></figcaption></figure>

## Отключение обновлений KlipperScreen

Для отключения обновлений KlipperScreen в файле **moonraker.conf** необходимо закомментировать или удалить всю секцию \[udate\_manager KlipperScreen]:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-24 115848.png" alt=""><figcaption></figcaption></figure>

## Отключение обновлений Fluidd

Для отключения обновлений Fluidd в файле **moonraker.conf** необходимо закомментировать или удалить всю секцию \[udate\_manager Fluidd]:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-24 115851.png" alt=""><figcaption></figcaption></figure>
