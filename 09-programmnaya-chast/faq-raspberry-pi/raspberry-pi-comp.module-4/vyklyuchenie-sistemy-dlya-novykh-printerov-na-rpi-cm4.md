---
description: Инструкция по настройке правильного включения и выключения RPI CM4
icon: power-off
---

# Выключение системы для новых принтеров на RPI CM4

Подключаемся по SSH (pi, raspberry).

Открываем файл rc.local командой :

```bash
sudo nano /etc/rc.local
```

Файл будет выглядеть примерно так:

<figure><img src="../../../.gitbook/assets/изображение (306).png" alt=""><figcaption></figcaption></figure>

Далее вставляем в него между строчками "fi" и "exit 0" строчку для включения GPIO 26:

```bash
pinctrl set 26 op pu dh
```

Должно получиться так:

<figure><img src="../../../.gitbook/assets/изображение (305).png" alt=""><figcaption></figcaption></figure>

Сохраняемся и выходим: Ctrl+S, Ctrl+X

**Более подробно с работой GPIO можно ознакомиться в данной инструкии:**

[rabota-s-gpio.md](rabota-s-gpio.md "mention")

