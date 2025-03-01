---
description: Инструкция по установке и настройке телеграм-бота
---

# 🤖 TelegramBot

{% hint style="info" %}
[https://github.com/nlef/moonraker-telegram-bot](https://github.com/nlef/moonraker-telegram-bot/wiki/Sample-config)1
{% endhint %}

## 01. Установка

Скачиваем и устаналиваем:

```bash
cd ~
git clone https://github.com/nlef/moonraker-telegram-bot.git
cd moonraker-telegram-bot
./scripts/install.sh
```

Соглашаемся на все.

Далее настраиваем сервис в **moonraker.**

Добавляем в файл moonraker.conf следующий код:

```django
[update_manager client moonraker-telegram-bot]
type: git_repo
path: ~/moonraker-telegram-bot
origin: https://github.com/nlef/moonraker-telegram-bot.git
env: ~/moonraker-telegram-bot-env/bin/python
requirements: scripts/requirements.txt
install_script: scripts/install.sh
```

## 02. Настройка телеграм-бота:

Переходим в телеграм и находим там BotFather:

<figure><img src="../../.gitbook/assets/изображение (43).png" alt=""><figcaption></figcaption></figure>

Нажимаем на кнопку "Запустить":

<figure><img src="../../.gitbook/assets/изображение (44).png" alt=""><figcaption></figcaption></figure>

Вводим команду /newbot:

<figure><img src="../../.gitbook/assets/изображение (45).png" alt=""><figcaption></figcaption></figure>

Далее задаем ему имена и названия

<figure><img src="../../.gitbook/assets/изображение (46).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/изображение (47).png" alt=""><figcaption></figcaption></figure>

После всех настроек получаем секретный токен бота (его нельзя никому давать!)

<figure><img src="../../.gitbook/assets/изображение (48).png" alt=""><figcaption></figcaption></figure>

Далее копируем этот токен и в файле telegram.conf в секции \[bot] меняем токен на наш:

<figure><img src="../../.gitbook/assets/изображение (49).png" alt=""><figcaption></figcaption></figure>

Далее переходим в созданного бота и жмем запусить, должно появится такое сообщение с chat\_id:

<figure><img src="../../.gitbook/assets/изображение (50).png" alt=""><figcaption></figcaption></figure>

Данный chat\_id копируем и вставляем в файле telegram.conf в секции \[bot]:

<figure><img src="../../.gitbook/assets/изображение (51).png" alt=""><figcaption></figcaption></figure>

Сохраняем и перезагружаем конфиги, после чего перезагружаем принтер. После запуска принтера в телеграм должо прилететь сообщение "Printer online".&#x20;

Готово. Телеграм-бот установлен и настоен.
