---
description: Описание процесса корретировки шагов двигателей X Y по методу Колбасера
---

# 🔧 Корректировка шагов X Y

### Необходимая оснастка:

<table data-view="cards"><thead><tr><th></th><th></th></tr></thead><tbody><tr><td>Заглушка хотенда с иглой</td><td><img src="../.gitbook/assets/photo_2023-11-15_11-24-40 (1).jpg" alt="" data-size="original"></td></tr><tr><td>Заглушка термистора (запаян резистор, чтобы принтер не выпадал в ошибку)</td><td><img src="../.gitbook/assets/photo_2023-11-15_11-24-57.jpg" alt="" data-size="original"></td></tr><tr><td>Специальная линейка</td><td><img src="../.gitbook/assets/photo_2023-11-15_11-25-01 (2).jpg" alt="" data-size="original"></td></tr></tbody></table>

### Процесс корретировки&#x20;

Бумажным скотчем приклеиваем специальную линейку с передней стороне стола:

<figure><img src="../.gitbook/assets/photo_2023-11-15_11-25-25.jpg" alt="" width="375"><figcaption></figcaption></figure>

Вставляем заглушки хотенда и термистора в печатную голову:

<figure><img src="../.gitbook/assets/photo_2023-11-15_11-25-31.jpg" alt="" width="370"><figcaption></figcaption></figure>

Переходим в веб-интерфейс принтера:

<figure><img src="../.gitbook/assets/изображение (213).png" alt="" width="375"><figcaption></figcaption></figure>

В консоль (на скриншоте выше справа снизу) вводим команду:

```django
G28
```

После ввода команды принтер паркует все оси и приедет в левый ближний угол.

<figure><img src="../.gitbook/assets/изображение (203).png" alt="" width="375"><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/изображение (204).png" alt="" width="375"><figcaption></figcaption></figure>

В ручном режиме двигаем стол к игле, после чего выравниваем линейку по игле, чтобы игла была ровно на линии с отметкой **10:**

<figure><img src="../.gitbook/assets/изображение (205).png" alt="" width="375"><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/изображение (206).png" alt="" width="375"><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/изображение (207).png" alt="" width="375"><figcaption></figcaption></figure>

Далее в ручном режиме двигаем ось X на 300 мм:

<figure><img src="../.gitbook/assets/изображение (209).png" alt="" width="375"><figcaption></figcaption></figure>

Игла должна стать напротив отметки **310:**

<figure><img src="../.gitbook/assets/изображение (210).png" alt="" width="375"><figcaption></figcaption></figure>

Если игла не совпала с отметкой 310, то в зависимости от случая:

* если игла зашла за отметку, то в веб-интрефейте в файле **Конфигурация->klipper-config->steppers.cfg** меняем значения **rotation\_distance** для **stepper X** и **stepper Y** в большую сторону на сотки/десятки.
* если игла не зашла за отметку, то в веб-интрефейте в файле **Конфигурация->klipper-config->steppers.cfg** меняем значения **rotation\_distance** для **stepper X** и **stepper Y** в меньшую сторону на сотки/десятки.

{% hint style="info" %}
Занимательная страничка:

Предположительно, но не точно, изменение значение **rotation\_distance** на **0,02** изменаяет величину перемещения на **0,5 мм.**

**Требуется проверить.**
{% endhint %}

<figure><img src="../.gitbook/assets/изображение (212).png" alt=""><figcaption></figcaption></figure>

После изменения значения **rotation\_distance** нажимаем кнопку **Сохранить и перезагрузить** и повторяем операцию с пункта про ввод команды _**G28.**_

В итоге при перемещении на 300 мм игла должна стать ровно над риской **310** на линейке.
