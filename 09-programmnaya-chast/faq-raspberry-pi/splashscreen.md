---
description: Настройка загрузочного экрана
---

# 👻 SplashScreen

Подключаемся к принтеру по SSH.

{% hint style="info" %}
Логин: pi

Пароль: raspberry
{% endhint %}

Обновляем систему:

```bash
sudo apt-get update
sudo apt-get upgrade
```

Устанавливаем пакет fbi:

```bash
sudo apt-get install fbi
```

Создаем файл сервиса под названием splashscreen командой:

```bash
sudo nano /etc/systemd/system/splashscreen.service
```

Далее прописываем в него следующее:

```arduino
[Unit]
Description=Splash screen
DefaultDependencies=no
After=local-fs.target

[Service]
ExecStart=/usr/bin/fbi -d /dev/fb0 --noverbose -a /home/pi/splash.png
StandardInput=tty
StandardOutput=tty

[Install]
WantedBy=sysinit.target
```

Далее подключаемся к принтеру через WinSCP или FileZilla и закидываем в домашнюю директорию файл splash.png (можно скачать ниже):

<figure><img src="../../.gitbook/assets/splash.png" alt=""><figcaption></figcaption></figure>

Регистируем и добавляем в автозагрузку сервис командами:

```
sudo systemctl enable splashscreen.service
sudo systemctl start splashscreen.service
```

Готово. Теперь после перезагрузки будет отображаться загрузочное лого.

