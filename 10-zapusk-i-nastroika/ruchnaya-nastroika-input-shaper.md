---
description: Инструкция по ручной настройке Input Shaper
---

# 〰️ Ручная настройка Input Shaper

### Настройка Input Shaper в ручном режиме <a href="#docs-internal-guid-35030fe9-7fff-9fb5-7e5e-3d32d27fa122" id="docs-internal-guid-35030fe9-7fff-9fb5-7e5e-3d32d27fa122"></a>

Переходим по ссылке ниже на официальную документацию Klipper’a по настройке Input Shaper, ознакамливаемся:

{% embed url="https://www.klipper3d.org/Resonance_Compensation.html" %}

Ставим печать 06-1-input-shaper-ABS.gcode (лежит в папке с этой инструкцией, либо подготавливаем g-код самостоятельно в соответствии с документацией)

После того как напечатали первый тест измеряем частоту колебаний, запоминаем данные.&#x20;

В итоге у вас должно быть 3 цифры:&#x20;

V – скорость которая = 90

N – частота колебаний на детали&#x20;

D – расстояние, которое вы брали для подсчета колебаний

Далее по формуле  V · N / D получаем частоту, которую необходимо будет заменить в конфиге принтера в секции input\_shaper.&#x20;

{% hint style="warning" %}
**Важно!!!** Метка X на детали это Y в секции input\_shaper, а Y это X.
{% endhint %}

Стандартная секция input\_shaper:

```
[input_shaper]
shaper_freq_x: 49 (заменить на полученную частоту Y)
shaper_type_x: mzv
shaper_freq_y: 49 (заменить на полученную частоту X)
shaper_type_y: mzv
```

<mark style="color:red;">**НЕ ПРАВИЛЬНО**</mark>~~**:** На данный момент 28.01.2023 ставим mzv, в Y можно заменить на zv~~

<mark style="color:green;">**ПРАВИЛЬНО:**</mark>

Модификатор ZV слабее, чем MZV – следовательно не имеет никакого смысла ставить его для более заметного эффекта, станет только хуже!

В таблице ниже приведены параметры модификаторов. Если хотим более заметный эффект на оси Y, то нужно ставить ZVD или даже EI (**после консультации с более компетентными коллегами**):

<figure><img src="https://lh7-us.googleusercontent.com/ReA_doqGaDgkOdeVtRiOWM3RwpnHPrCWtfbBPAPUpR_XAwEN1q13PlGdZ1LamknwbN8XC866BpH--TteRbKTkYkmyV5cQ4ccqxUg-0U791420OAn33-zN-CvYEv4NzG7oDP8Pu1MGAglmFWBASAeE_M" alt="" width="375"><figcaption></figcaption></figure>

Далее ставим на печать 06-2-input-shaper-ABS.gcode

Сравниваем результаты!

Слева первый тест, справа – второй

![](https://lh7-us.googleusercontent.com/JWZbGd6k9yXxgZEpNK_AOmmOQi0q-V7CXq82OFQm89wjSV1kZ9ChFLUlxCzG-YC5wI3qD_BXqHliBKbK1NPETS8UkrtgNFZ4ItMOEYhlhUQysC2JNQ2iROAulctfYFKJuqri1VaY8wpizHnS8ZEBl7g)![](https://lh7-us.googleusercontent.com/Bp92qdrkCjjiej3o0nJOCbn4xmLm6SrInl0T0jDmpAweTBi91OTILIrXimbGB3ujIFrKtrmchxlooSbb7k-BRsdaXEASmFza4QFbRhS3x1wxEGGlQnLvWhMXArSE9K1X7uzJBuPCXekX71YWHSj582s)



При возникновении непонятных артефактов при печати инпут шейпера пробуем "притирать" каретки притирочным G-кодом и затем проверяем помогло ли&#x20;

{% embed url="https://drive.google.com/file/d/1-2OjFY-MFn8dykNoYQin5JbF7NfojsE6/view?usp=drive_link" %}
Притирочный G-код
{% endembed %}

