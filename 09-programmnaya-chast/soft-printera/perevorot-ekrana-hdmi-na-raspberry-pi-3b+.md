---
description: >-
  Инструкция по перевороту экрана на Raspebrry Pi 3B+ HDMI дисплеев 4.3 inch
  HDMI LCD Waveshare
---

# 🖥️ Переворот экрана HDMI на Raspberry PI 3B+

## 01. Переворот экрана для HDMI дисплея

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

1. Настраиваем отображение на экране:

* открываем файл _/boot/config.txt_:

```bash
sudo nano /boot/config.txt
```

* находим эти строчки и комментируем из (символ # вначале строки):

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

* листаем в самый низ и находим строчку display\_rotate и меняем значение на 2 (по умолчанию 0):

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

* Сохраняем и выходим:&#x20;

**Ctrl+S, Ctrl+X**

2. Настраиваем тачскрин:

* открываем файл /usr/share/X11/xorg.conf.d/40-libinput.conf

<pre class="language-bash"><code class="lang-bash"><strong>sudo nano /usr/share/X11/xorg.conf.d/40-libinput.conf
</strong></code></pre>

* добавляем строчку в секции **Section "InputClass" Identifier "libinput touchscreen catchall":**

```bash
Option "TransformationMatrix" "-1 0 1 0 -1 1 0 0 1"
```

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

* Сохраняем и выходим:&#x20;

**Ctrl+S, Ctrl+X**

{% hint style="info" %}
Для выбора поворота тачскрина необходимо воспользоваться таблицей:

![](<../../.gitbook/assets/изображение (218).png>)

При повороте экрана нормально (**normal**) используем следующее значение (**0**):

**1 0 0 0 1 0 0 0 1**

При повороте экрана влево (**left**) используем следующее значение (**90 Clockwise**):

**0 -1 1 1 0 0 0 0 1**

При повороте экрана вправо (**right**) используем следующее значение (**90 Counter-Clockwise**):

**0 1 0 -1 0 1 0 0 1**

При повороте экрана перевернуто (**inverted**) используем следующее значение (**180 Inverts X and Y**):

**-1 0 1 0 -1 1 0 0 1**
{% endhint %}

Перезагружаем Raspberry Pi и проверяем работу тачскрина:

```bash
sudo reboot
```

<details>

<summary>Памятка</summary>

`xrandr` is an Xwindows utility and expects to be run inside an X session, that's where the `Cant open display` comes from.

You could do this (if your DISPLAY is :0):

```
$ export DISPLAY=:0
$ xrandr --listmonitors
$ xrandr your_command
```

![](<../../.gitbook/assets/изображение (53).png>)

[https://www.waveshare.com/wiki/7inch\_HDMI\_LCD\_(C)](https://www.waveshare.com/wiki/7inch_HDMI_LCD_\(C\))





</details>
