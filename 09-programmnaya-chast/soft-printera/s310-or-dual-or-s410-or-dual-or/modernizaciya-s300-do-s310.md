---
description: Инструкция по настройке S300 до S310
---

# 📳 Модернизация S300 до S310

Меняем название принтера:

Открываем веб-интерфейс -> Настройки -> Имя принтера -> Z-Bolt S310 (Z-Bolt S310 Dual)

<figure><img src="../../../.gitbook/assets/изображение (2).png" alt=""><figcaption></figcaption></figure>

Подключаемся по SSH.

Переходим в домашнюю директорию:

```bash
cd ~
```

Настраиваем USB-ключ доступа согласно инструкции:

[usb-klyuch-dostupa-v1.0-dlya-printerov-do-zbs352576.md](usb-klyuch-dostupa-v1.0-dlya-printerov-do-zbs352576.md "mention")

Далее настраиваем активацию веб-интерфейса Fluidd согласно инструкции:

[aktivaciya-veb-interfeisa-fluidd.md](aktivaciya-veb-interfeisa-fluidd.md "mention")

Настраиваем **систему оповещения соснояния принтера** согласно инструкции:

[sistema-opovesheniya-sostoyaniya-printera.md](sistema-opovesheniya-sostoyaniya-printera.md "mention")

Отключаем обновления системы и сторонних репориториев:

[#otklyuchenie-sistemnykh-obnovlenii](otklyuchenie-obnovlenii.md#otklyuchenie-sistemnykh-obnovlenii "mention")

Проверяем отсутствие удаленных пакетов в панели "Настройки" раздел "Обновление ПО":

<figure><img src="../../../.gitbook/assets/изображение (287).png" alt=""><figcaption></figcaption></figure>

Проверяем конфигурацию принтера (максимальные температуры, область печати и т.п) согласно таблице характеристик:

{% embed url="https://docs.google.com/spreadsheets/d/1bt7-CNXhpd8SHu7sSWu0CXSXV6xjgGy8-oyC5oyDUsA/edit?gid=0#gid=0" %}
