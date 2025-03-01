---
description: Инструкция по настройке образа на прошивочной флекшке для автопрошивки Rock Pi
---

# 📲 Подготовка флешки с автопрошивкой

{% hint style="info" %}
Сслыка на репозиторий:

[https://github.com/Transistor427/rpi\_flash\_image](https://github.com/Transistor427/rpi_flash_image)
{% endhint %}

Берем флешку с залитым образом для прошивки Rock Pi.

{% hint style="success" %}
**При использовании ветки zip появляется возможность прошивать Rock Pi заархивированным образом!**
{% endhint %}

Вставляем ее в любой Rock Pi, подключаем к нему Ethernet и питание.

Ждем загрузки и подключаемся к нему по SSH.

Далее установка:

* переходим в домашнюю директорию:

```bash
cd ~
```

* обновляем систему и устанавливаем Git:

```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt install git
```

* клонируем репозиторий и заходим в него:

```bash
git clone https://github.com/Transistor427/rpi_flash_image
cd ~/rpi_flash_image
```

* выдаем права на исполненние:

```bash
sudo chmod 777 ./install.sh
```

* запускаем установку:

```bash
./install.sh
```

После окончания установки перезагружаем Rock Pi командой sudo reboot.

После перезагруки снова подключаемся к Rock Pi по SSH и проверяем наличие активного сервиса dd с помощью команды htop.

Теперь при вставленной флешке и поданном питании Rock Pi сам прошьется тем образом, который лежит на флешке, после чего выключиться (время прошивки около 15 минут).
