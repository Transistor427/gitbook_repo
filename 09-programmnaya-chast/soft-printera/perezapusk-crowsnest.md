---
description: >-
  Инструкция по автоматической перезагрузке сервиса Crowsnest для принтеров с
  моргающей камерой
---

# 📷 Перезапуск Crowsnest

Подключаемся по SSH.

Создаем в любом удобном месте файл для перезагрузки:

```bash
sudo nano ~/restart_crowsnest.sh
```

Далее записываем в его следующее:

```bash
#!/bin/bash
sudo systemctl restart crowsnest
```

Сохраняем и выходим.

Далее переходим к настройке запуска скрипта по времени.

{% hint style="info" %}
[**https://gsdent.ru/zapusk-bash-skripta-v-opredelennoe-vremya/**](https://gsdent.ru/zapusk-bash-skripta-v-opredelennoe-vremya/)
{% endhint %}

Открываем файл сервиса cron:

```bash
sudo crontab -e
```

Далее в самый конец файла записываем строчку:

```bash
*/5 * * * * /home/rock/restart_crowsnest.sh
```

Сохраняем и выходим.

Перезагружаем принтер командой:

```bash
sudo reboot
```

Проверяем работу.

{% hint style="info" %}
Для проверки запущенных задач используем команду:

<pre class="language-bash"><code class="lang-bash"><strong>sudo crontab -l
</strong></code></pre>
{% endhint %}
