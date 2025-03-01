---
description: Инструкция по прошивке Compute Module с EMMC
icon: album-circle-plus
---

# Прошивка пустым образом CM4 с eMMC

{% embed url="https://bttwiki.com/PI4B.html#cm4-installation" %}

_**Note: the eMMC version will not run the system from the SD card.**_

{% hint style="warning" %}
Внимание! eMMC версия CP не поддерживает загрузку с SD-карты.
{% endhint %}

1. Скачиваем и устаналиваем rpiboot:

* для Windows:

[http://github.com/raspberrypi/usbboot/raw/master/win32/rpiboot\_setup.exe](http://github.com/raspberrypi/usbboot/raw/master/win32/rpiboot_setup.exe)

* для Mac и Linux:

[https://github.com/raspberrypi/usbboot#building](https://github.com/raspberrypi/usbboot#building)

2. Переводим переключатели на борде (3 и 4) в верхнее положение:

![](https://bttwiki.com/img/PI4B/PI4B_eMMC.png)

3. Подключаем CP к компьютеру, включаем rpiboot и ждем окончания прошивки.
4. После сообщения об успешной прошивке открываем Raspberry Pi Imager, выбираем:

* Устройство: Raspberry PI 4
* Операционная система: Raspberry Pi OS (other) -> Raspberry PI OS Lite (64-bit)
* Запоминающее устройство: Подключенный CP

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-04-24 192956.png" alt="" width="341"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-04-24 193002.png" alt="" width="341"><figcaption></figcaption></figure>

5. После прошивки отключаем CP от компьютера.
6. Переводим переключатели в обратное положение.
7. Настраиваем систему.
