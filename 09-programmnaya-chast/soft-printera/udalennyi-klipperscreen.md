---
description: Инструкция по настройке удаленного рабочего стола для KlipperScreen
---

# 📲 Удаленный KlipperScreen

{% embed url="https://www.klipper3d.org/Config_Reference.html#exclude_object" %}

## 01. Настройка принтера

Подключаемся к принтеру по SSH и вводим следующий команды:

```bash
sudo apt install tigervnc-standalone-server
sudo nano ~/KlipperScreen/scripts/launch_KlipperScreen.sh
```

Далее вставляем следующее в файл:

```bash
#!/usr/bin/env bash

# Use display 10 to avoid clashing with local X server, if anyy
Xtigervnc -rfbport 5900 -noreset -AlwaysShared -SecurityTypes none :10&
DISPLAY=:10 $KS_XCLIENT&
wait
```

Перезагружаем KlipperScreen командой:

```bash
sudo systemctl restart KlipperScreen
```

{% hint style="info" %}
Дополнительно в настройках KlipperScreen'а можно настроить следующие параметры:

![](../../.gitbook/assets/disable_dpms_poweroff.png)
{% endhint %}

## 02. Настройка устройства

Скачиваем и устанавливаем RealVNC Viewer.

{% embed url="https://downloads.realvnc.com/download/file/viewer.files/VNC-Viewer-7.9.0-Windows.exe" %}

## 03. Работа

После установки заходим в RealVNC Viewer, вводим IP-адрес принтера и порт (5900) и подключаемся, например:

```
192.168.31.183:5900
```

<figure><img src="../../.gitbook/assets/изображение (221).png" alt="" width="375"><figcaption></figcaption></figure>

При подключении появится такое окно:

<figure><img src="../../.gitbook/assets/изображение (222).png" alt="" width="243"><figcaption></figcaption></figure>

Далее со всем соглашаемся и видим окно с KlipperScreen'ом.

{% hint style="warning" %}
При работе таким способом изображение на экране пропадет. Чтобы его вернуть, нужно будет переименовать файл launch\_KlipperScreen.sh в что-то такое launch\_KlipperScreen.sh.back и перезагрузить KlipperScreen, но тогда удаленный рабочий стол перестанет работать.
{% endhint %}
