# Klipper LED Effect

## 01. Конфиг

{% hint style="info" %}
[https://www.klipper3d.org/Config\_Reference.html#neopixel](https://www.klipper3d.org/Config_Reference.html#neopixel)
{% endhint %}

Добавляем секцию с параметрами:

```django
[neopixel _ARGB]
pin: PD3 # управляющий пин
chain_count: 11 # кол-во светодиодов в ленте
```

<figure><img src="../../../.gitbook/assets/изображение (247).png" alt=""><figcaption></figcaption></figure>

В консоли можно управлять лентой командой:

```django
SET_LED LED=ARGB GREEN=0.012 RED=0.902 BLUE=0
```

{% hint style="info" %}
Софт для всяких красивых эффектов

[https://github.com/julianschill/klipper-led\_effect](https://github.com/julianschill/klipper-led_effect)
{% endhint %}



## 02. Подключение ленты

Модель ленты:

* WS2812B - адресная светодиодная лента с рабочим напряжением 5В.

<figure><img src="../../../.gitbook/assets/PXL_20240215_103410620.jpg" alt="" width="375"><figcaption></figcaption></figure>

Для подключения ленты важно знать несколько нюансов.

1. У ленты есть направление подключение (зеленая стрелочка). Если подключить не в том направлении, то лента не включится (связано с спецификой работы светодиодов.
2. 3 пина: +5В, DIN, GND. +5В и GND - это питание. DIN - пин для управления (подключается в spider).
3. В зависимости от кол-ва и длинны лента может потреблять очень большой ток по 5В линии (<mark style="color:red;">**150 светодиодов на полной яркости белого цвета будут потреблять около 9А**</mark>!), поэтому нужно смотреть, можно ли ее подключать к spider напрямую или нужен отдельный БП.
