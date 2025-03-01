---
description: Инструкция по настройке пользователя и ограничению доступа Fluidd
---

# 🔐 Активация веб-интерфейса Fluidd

Открываем файл moonraker.conf и в конец секции \[authorization] добавляем сточку:

```
force_logins: true
```

<figure><img src="../../../.gitbook/assets/изображение (270).png" alt=""><figcaption></figcaption></figure>

Сохраняем и перезагружаем.

Переходим в панель "Настройки" раздел "Аутентификация":

<figure><img src="../../../.gitbook/assets/изображение (271).png" alt=""><figcaption></figcaption></figure>

Выбираем пункт "Добавить пользователя", далее задаем ему логин (например Z-Bolt) и пароль (6-ти значный пароль, который состоит из цифр серийного номера (Серийник **ZBS352500**, то пароль **352500**)). <mark style="color:red;">**Не забываем сохранить эти данные в сборочный лист принтера (вкладка Software)!**</mark>

Далее нажимаем кнопку "КЛЮЧ API" и копируем ключ:

<figure><img src="../../../.gitbook/assets/изображение (285).png" alt=""><figcaption></figcaption></figure>

Далее открываем KlipperScreen.conf и добавляем в начало секцию:

<figure><img src="../../../.gitbook/assets/изображение (286).png" alt=""><figcaption></figcaption></figure>

```django
[printer Z-Bolt]
moonraker_host: 127.0.0.1
moonraker_port: 7125
moonraker_api_key: "скопированный ключ без кавычек"
```

Сохраняем и перезагружаем.

{% hint style="danger" %}
ВНИМАНИЕ!

В случае, если ключ API moonraker'а был изменен (специально или случайно), то новый ключ необходимо добавить в файл KlipperScreen.conf с заменой старого, иначе KlipperScreen будет выдавать ошибку!
{% endhint %}

Перезагружаем принтер и проверяем:

* при первом запуске должно появиться окошко ввода URL API:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-21 124234.png" alt=""><figcaption></figcaption></figure>

* далее открываеся страница авторизации:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-21 124250.png" alt=""><figcaption></figcaption></figure>

* после закрытия и повторного открытия вкладки при отмене сохрания логина и пароля принтер должен запросить их повторно.

Всю информацию заносим в сборочный лист принтера (вкладка Software):

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-24 123838.png" alt=""><figcaption></figcaption></figure>
