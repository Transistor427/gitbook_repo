---
description: Инструкция по сборке кос для новой платы расширения версии 3
---

# 🪡 Сборка кос для Ext.PCB v3

{% hint style="warning" %}
**ВНИМАНИЕ! ВСЕ КОСЫ С 29.08.2024**
{% endhint %}

## Подготовка проводов

{% tabs %}
{% tab title="Коса T0 (левая длинная)" %}
Длина проводов - 2050 мм.

Провод 20AWG - 2 шт. на 1 косу (нагреватель)

Длина проводов - 2050 мм.

Провод 24AWG - 6 шт. на 1 косу (термистор, двигатель)

Длина проводов - 2110 мм.

Провод 24AWG - 2 шт. на 1 косу (вентилятор)
{% endtab %}

{% tab title="Коса T1 (правая короткая)" %}
Длина проводов - 1750 мм.

Провод 20AWG - 2 шт. на 1 косу (нагреватель)

Длина проводов - 1750 мм.

Провод 24AWG - 6 шт. на 1 косу (термистор, двигатель)

Длина проводов - 1810 мм.

Провод 24AWG - 2 шт. на 1 косу (вентилятор)
{% endtab %}
{% endtabs %}

## Обжимка проводов

{% tabs %}
{% tab title="Коса T0 (левая длинная)" %}
**Провода нагревателя:**

* 20AWG 2 шт. 2050 мм
* Обжимаем с одной стороны в черные НШВИ, с другой в XHD
*

    <figure><img src="../../../.gitbook/assets/изображение (236).png" alt="" width="375"><figcaption></figcaption></figure>

**Провода термистора:**

* 24AWG 2 шт.  2050 мм.
* обжимаем с одной стороны в белые НШВИ, с другой в XHD
*

    <figure><img src="../../../.gitbook/assets/изображение (237).png" alt="" width="375"><figcaption></figcaption></figure>

**Провода вентилятора:**

* 24AWG 2 шт. 2110 мм
* обжимаем с одной стороны в XH2.54-2pin (сразу вставляем их в разьемы), с другой в XHD
*

    <figure><img src="../../../.gitbook/assets/изображение (240).png" alt="" width="375"><figcaption></figcaption></figure>

**Провода двигателя экструдера:**

* 20AWG 4 шт 2050 мм
* обжимаем с одной стороны в MMF 4 pin Мама, с другой в XHD
*

    <figure><img src="../../../.gitbook/assets/изображение (223).png" alt="" width="375"><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Коса T1 (правая короткая)" %}
**Провода нагревателя:**

* 20AWG 2 шт. 1750 мм;
* Обжимаем с одной стороны в черные НШВИ, с другой в XHD;
*

    <figure><img src="../../../.gitbook/assets/изображение (236).png" alt="" width="375"><figcaption></figcaption></figure>

**Провода термистора:**

* 24AWG 2 шт. 1750 мм;
* обжимаем с одной стороны в белые НШВИ, с другой в XHD;
*

    <figure><img src="../../../.gitbook/assets/изображение (237).png" alt="" width="375"><figcaption></figcaption></figure>

**Провода вентилятора:**

* 24AWG 2 шт. 1810 мм;
* обжимаем с одной стороны в XH2.54-2pin, с другой в XHD;
*

    <figure><img src="../../../.gitbook/assets/изображение (240).png" alt="" width="375"><figcaption></figcaption></figure>

**Провода двигателя экструдера:**

* 20AWG 4 шт. 1750 мм;
* обжимаем с одной стороны в MMF 4 pin Мама, с другой в XHD;
*

    <figure><img src="../../../.gitbook/assets/изображение (224).png" alt="" width="375"><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

## Сборка косы

{% hint style="info" %}
Схема подключения всего:

![](../../../.gitbook/assets/photo_2024-04-22_16-02-13.jpg)
{% endhint %}

### 00. Термоусадка

Перед вставлением обжатых проводов в разъемы настоятельно рекомендуется одеть на будущую косу (12 проводов) клеевую термоусадку диаметром 20мм и длиной 50мм, иначе придется делать это в пункте 04, растягивая её длинногубцами и ругаясь на разработчиков:

<div><figure><img src="../../../.gitbook/assets/Screenshot 2024-04-24 103745.png" alt="" width="159"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/Screenshot 2024-04-24 103915.png" alt="" width="188"><figcaption></figcaption></figure></div>

### 01. Хотенд

НШВИ вставляем в разъем 15EDGK-3.5-04P-14-00AH как на фото:

<figure><img src="../../../.gitbook/assets/AF1QipO3CmOe8leKLLi7jiLrw0razS00BeubQ2uVFhCm=w2048-h1536.jpg" alt="" width="375"><figcaption></figcaption></figure>

XHD вставляем в разьем XHD-12pin как на фото:

<figure><img src="../../../.gitbook/assets/XHD hotend.jpg" alt="" width="375"><figcaption></figcaption></figure>

### 02. Вентиляторы

XH2,54 вставляем в разъем XH2,54-2pin как на фото:

<figure><img src="../../../.gitbook/assets/изображение (240).png" alt="" width="375"><figcaption></figcaption></figure>

XHD вставляем в разьем XHD-12pin как на фото:

<figure><img src="../../../.gitbook/assets/XH2.54 Fan (1).jpg" alt="" width="287"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/XHD fan.jpg" alt="" width="364"><figcaption></figcaption></figure>

### 03. Провода экструдера

MMF 4 pin Мама вставляем в разъем MMF 4 pin Мама как на фото:

<figure><img src="../../../.gitbook/assets/MMF 4pin.jpg" alt="" width="375"><figcaption></figcaption></figure>

XHD вставляем в разьем XHD-12pin как на фото:

<figure><img src="../../../.gitbook/assets/XHD motor (1).jpg" alt="" width="256"><figcaption></figcaption></figure>

### 04. Сборка косы

1. Одеваем: 1.1. Пластиковую оплетку-самозаворачивалку 4мм длиной 60 мм на провода вентилятора (xh2.54).  1.2. Пластиковую оплетку-самозаворачивалку 6мм длиной 40 мм на провода хотэнда. 1.3. Тканую оплетку-самозаворачивалку диаметром 10мм и длиной 1400мм на всю косу.&#x20;
2. Клеевую термоусадку диаметром 20мм и длиной 50мм усаживаем поверх тканой оплетки-самозаворачивалки со стороны ПГ таким образом, чтобы от конца термоусадки до разъемов хотэнда и мотора осталось 40мм, а до разъема ветилятора - 100мм:

<div><figure><img src="../../../.gitbook/assets/Screenshot 2024-04-24 100639.png" alt="" width="186"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/Screenshot 2024-04-24 100700.png" alt="" width="155"><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/Screenshot 2024-04-24 100726.png" alt="" width="172"><figcaption></figcaption></figure></div>

3. С обратной стороны стяжку, чтобы оплетка не елозила туда-сюда.

С обратной стороны стяжку, чтобы оплетка не елозила туда-сюда



**Фото отсутствует....**
