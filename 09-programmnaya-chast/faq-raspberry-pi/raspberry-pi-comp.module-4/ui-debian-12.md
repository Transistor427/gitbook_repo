---
description: Инструкции по настройке внешнего вида операционной системы на RPI CM4
icon: debian
---

# UI Debian 12

## Отключение консоли при запуске RPI CM4:

* Открываем файл конфигурации:

```bash
sudo nano /boot/firmware/cmdline.txt
```

* Меняем "console=Пtty0" на "console=tty3"

<figure><img src="../../../.gitbook/assets/{D7C65FF7-03C5-4E11-B3B8-B85FEFC74160} (2).png" alt=""><figcaption></figcaption></figure>

* В самый конец добавляем:

```bash
loglevel=3 quiet logo.nologo fbcon=map:2 disable_splash=1
```

<figure><img src="../../../.gitbook/assets/{E7317C79-5EA8-4464-90C3-05CCDB6C728D}.png" alt=""><figcaption></figcaption></figure>

Сохраняем и выходим: Ctrl+S, Ctrl+X

## Отключаем гардиентный квадрат при загрузке:

```bash
sudo nano /boot/firmware/config.txt
```

Находим строчку "disable\_overscan=1" и добавляем сразу под ней строчку "disable\_splash=1"

<figure><img src="../../../.gitbook/assets/{CD23D156-8758-46BF-801A-BA122F1E48AD}.png" alt=""><figcaption></figcaption></figure>

Сохраняем и выходим: Ctrl+S, Ctrl+X







<mark style="color:red;">**Полезные ссылки:**</mark>

[ttps://forums.raspberrypi.com/viewtopic.php?t=252163](https://forums.raspberrypi.com/viewtopic.php?t=252163)

[https://raspberrypi.stackexchange.com/questions/117098/how-to-remove-the-bootloader-startup-screen-on-rpi-4-buster](https://raspberrypi.stackexchange.com/questions/117098/how-to-remove-the-bootloader-startup-screen-on-rpi-4-buster)

[https://www.hackster.io/RandomRoboSmith/changing-the-splash-screen-on-your-raspberry-pi-7aee31](https://www.hackster.io/RandomRoboSmith/changing-the-splash-screen-on-your-raspberry-pi-7aee31)
