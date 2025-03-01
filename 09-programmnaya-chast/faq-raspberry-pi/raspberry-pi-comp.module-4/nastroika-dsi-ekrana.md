---
description: Инструкция по включению DSI экрана на BTT PI4B Adapter и Raspberry Pi CP4
icon: display-medical
---

# Настройка DSI экрана

{% embed url="https://www.raspberrypi.com/documentation/computers/compute-module.html" %}

{% embed url="https://manuals.plus/m/301c0ee66a7853b2b6ba247698e244a1bd6b1ea6d99a37ce859c1a7ec6759b44_optim.pdf" %}

Подключение DSI дисплея к BTT PI4B Adapter и Raspberry Pi CP4:

<figure><img src="../../../.gitbook/assets/изображение (250).png" alt="" width="375"><figcaption></figcaption></figure>

Подключаемся по SSH.

Скачиваем драйвер для DSI экрана:

{% code fullWidth="false" %}
```bash
sudo wget https://datasheets.raspberrypi.com/cmio/dt-blob-disp1-cam1.bin -O /boot/dt-blob.bin
```
{% endcode %}

Открываем конфигурационный файл raspberry командой:

```bash
sudo nano /boot/firmware/config.txt
```

В самый конец вставляем строчку:

```bash
dtoverlay=vc4-kms-dsi-7inch
```

<figure><img src="../../../.gitbook/assets/изображение (249).png" alt=""><figcaption></figcaption></figure>

Сохраняем: Ctrl+S, Ctrl+X.

Перезагружаем систему командой:

```bash
sudo reboot
```

Проверяем работу дисплея и тачскрина.
