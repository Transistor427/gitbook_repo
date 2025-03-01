---
description: Инструкция по прошивке Compute Module с EMMC
icon: album-circle-plus
---

# Прошивка готовым образом CM4 с eMMC

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
4. После сообщения об успешной прошивке открываем [BalenaEtcher](https://github.com/balena-io/etcher/releases/download/v1.19.21/balenaEtcher-1.19.21.Setup.exe).
5. Выбираем готовый образ (имеет в названии rpicm4).
6. Выбираем устройство (Compute Module).
7. Запускаем прошивку.

После окончания прошивки отключаем устройство от компьютера, переводим переключаетли обратно в нижнее положение, после чего включаем и проверяем работу.
