---
description: Инструкция по добавлению камеры Logitech
cover: >-
  https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn.wallpapersafari.com%2F73%2F6%2FzexW2p.jpg&f=1&nofb=1&ipt=afaa2f95e42f9d6565d356a84996c92b866b42998437cdc2d41816eaef92ad6a&ipo=images
coverY: 0
---

# 🎥 Добавление камеры Logitech

Подключаемся к Rock Pi по ssh (логин: rock, пароль: rock):

```bash
ssh rock@192.168.31.106
```

<figure><img src="../.gitbook/assets/изображение (199).png" alt=""><figcaption></figcaption></figure>

Получаем ID камеры командой:

```bash
ls -al /dev/v4l/by-id
```

<figure><img src="https://lh3.googleusercontent.com/S_4k6GE3WZUmg_G3_Mpphkhk4vpsH8M1GY8Al1-M-dBgUsXN6McEEp6JThzSp6u8wNMVVM8w7vbETuDuEnKTRbqdw0pH_JhNng0wEhVSrYvjfEDGsGppZHYDslCHIHKStTiw7VgFwiNNSW1m7EjvOWE" alt=""><figcaption></figcaption></figure>

Открываем конфигуарционный файл сервиса **Crowsnest** командой:

```bash
sudo nano ~/printer_data/config/crowsnest.conf
```

В открывшемся окне меняем название камеры на то, которое узнали ранее, а также меняем разрешение на 1280х720 если оно не установлено:

<figure><img src="https://lh3.googleusercontent.com/7PBHj9Q9VIjkAqWq44LzYpRoGIwfsyCwtOkh_HjD5wxS1c4XwH8bXp-7sLqT8AgO5faGwyplthkc970MYzkKn1UTgTqxyuON4VK49cEPkuaF2WBkD_hzHKlV0q658KPBjojyI2PYD6j9_EoKnFZYYIQ" alt=""><figcaption></figcaption></figure>

Сохраняем изменения **CTRL+S** и выходим из редактора **CTRL+X**

Перезагружаем принтер с помощью команды:

```bash
sudo reboot
```

Проверяем в веб-интерфейсе работает ли камера.

<figure><img src="../.gitbook/assets/изображение (196).png" alt=""><figcaption></figcaption></figure>
