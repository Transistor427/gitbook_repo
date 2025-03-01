---
description: Инструкция по снятию образа с EMMC Raspberry Pi CM4
icon: floppy-disk-circle-arrow-right
---

# Снятие образа с RPICM4

{% hint style="danger" %}
**ВНИМАНИЕ! ВСЕ ДЕЙСТВИЯ ПРОВОДЯТСЯ В ОПЕРАЦИОННОЙ СИСТЕМЕ LINUX!**
{% endhint %}

1. Скачиваем и устаналиваем rpiboot:

* для Mac и Linux:

{% embed url="https://github.com/raspberrypi/usbboot#building" %}

2. Переводим переключатели на борде (3 и 4) в верхнее положение:

<figure><img src="../../../.gitbook/assets/PI4B_eMMC.png" alt=""><figcaption></figcaption></figure>

3. Подключаем CP к компьютеру, включаем rpiboot командой **sudo ./rpiboot** и ждем окончания прошивки.
4. После окончания прошивки проверяем, определилось ли хранилище в системе командой:

```bash
lsblk
```

Должно быть устройство с общим объемом 32Гб.

5. Вводим в терминал команду (sdb заменить на полученное выше название):

```bash
sudo dd if=/dev/sdb of=image_rpicm4_26082024.img bs=8m status=progress
```

После снятия образа отключаем устройство, переводим переключатели в нижнее положение, после чего включаем и проверяем работу.
