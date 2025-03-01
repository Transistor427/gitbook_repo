---
description: Инструкция по отключению системных обновлений на ядре 5.10
---

# 🪛 Отключение системных обновлений

Подключаемся по SSH.

Отключаем обновления от RADXA:

Открываем файл с обновлениями от RADXA

```bash
sudo nano /etc/apt/sources.list.d/apt-radxa-com.list
```

Комментируем все строчки, которые начинаются на deb:

<figure><img src="../../../.gitbook/assets/изображение (24).png" alt=""><figcaption></figcaption></figure>

Сохраняем и выходим: Ctrl+S, Ctrl+X

Открываем файл с обновлениями Linux:

```bash
sudo nano /etc/apt/sources.list
```

Комментируем все строчки, которые начинаются на deb:

<figure><img src="../../../.gitbook/assets/изображение (25).png" alt=""><figcaption></figcaption></figure>

Сохраняем и выходим: Ctrl+S, Ctrl+X

Проверяем:

```bash
sudo apt update
```

Должно получится так:

<figure><img src="../../../.gitbook/assets/изображение (26).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Если при вводе команды появляется такое:

![](<../../../.gitbook/assets/изображение (28).png>)

То перепроверяем, во всех ли файлах закомментированы строки или обращаемя к специалистам.
{% endhint %}
