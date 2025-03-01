---
description: Инструкция по настройке принтера для компенсации неперпендикулярности балки X
---

# ❕ Компенсация неперпендикулярности балки X

{% hint style="info" %}
[https://www.klipper3d.org/Skew\_Correction.html](https://www.klipper3d.org/Skew_Correction.html)
{% endhint %}

## 01. Измерения

Печатаем файл 02\_skew\_correction и измеряем значения AC, BC и AD.

Записываем полученные значения.

Наименование диагоналей:

<figure><img src="../.gitbook/assets/изображение (232).png" alt=""><figcaption></figcaption></figure>

## 02. Настройка

Убеждаемся, что в файле printer.cfg прописана секция \[skew\_correction]. Если нет, прописываем:

<figure><img src="../.gitbook/assets/изображение (231).png" alt=""><figcaption></figcaption></figure>

Сохраняем и перезагружаем.

В файле klipper-config->gcode-macros.cfg создаем макрос \[gcode\_macro SKEW] (если него нет), в который вставляем значения AC, BC и AD, полученные в результате измерений из пункта 1 настоящей инструкции. После чего сохраняем и перезагружаем:

```django
[gcode_macro SKEW]
gcode:
    SET_SKEW XY=280,280.5,200
```

Где в SET\_SKEW XY=**280,280.5,200**

```
Length AC = 280
Length BD = 280.5
Length AD = 200
```

{% hint style="info" %}
Значения **280,280.5,200** получаем после замера теста диагоналей.
{% endhint %}

Далее, для проверки в терминале прописываем команду SKEW:

```django
SKEW
```

Проверяем значения командой:

```django
GET_CURRENT_SKEW
```

В файл klipper-config->gcode-macros.cfg добавляем в макрос START\_PRINT следующие строчки (или раскомментируем их, если они уже есть):

<figure><img src="../.gitbook/assets/изображение (29).png" alt="" width="178"><figcaption></figcaption></figure>

```django
SKEW
GET_CURRENT_SKEW
```

Перепечатываем тест 02\_skew\_correction, измеряем значения AC, BC. Если всё сделано правильно, должны получиться одинаковыми с погрешностью равной погрешности измерительного прибора.&#x20;
