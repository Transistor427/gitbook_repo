---
description: >-
  Инструкция по запуску Klipper, Moonraker, KlipperScreen, Crowsnest на новом
  ядре для Rock Pi 4B+
---

# 🐂 Переход на ядро 5.10

## Подготовка образа

Скачиваем образ под Rock Pi с Debian 11 с [Github Radxa](https://github.com/radxa-build/rock-pi-4b/releases):

{% hint style="info" %}
Ссылка: [https://github.com/radxa-build/rock-pi-4b/releases/download/20230601-0206/rock-pi-4b\_debian\_bullseye\_kde\_b32.img.xz](https://github.com/radxa-build/rock-pi-4b/releases/download/20230601-0206/rock-pi-4b_debian_bullseye_kde_b32.img.xz)
{% endhint %}

Закидываем его на прошивочную флешку (делается из под линукса).

Разархивируем его на прошивочной флешке.

## Прошивка Rock Pi

Вставляем прошивочную флешку в Rock Pi.

Подключаемся по SSH.

Прошиваем Rock Pi командой:

{% code overflow="wrap" %}
```bash
sudo dd if=rock-pi-4b_debian_bullseye_kde_b32.img of=/dev/mmcblk1 bs=8M status=progress
```
{% endcode %}

Отключаем питание и извлекаем флешку из принтера.

## Настройка образа

Включаем прошитый принтер.

Подключаемся по SSH.

{% hint style="info" %}
Логин: rock

Пароль: rock
{% endhint %}

### 00. Устанавливаем софт&#x20;

Обновляем систему:

```bash
sudo apt-get update
sudo apt-get upgrade
```

Перезагружаемся:

```bash
sudo reboot
```

После перезагрузки ставим **GIT и WGET:**

```bash
sudo apt-get install git wget
```

Ставим весь 3д-принтерный софт кроме KlipperScreen:

```bash
cd ~
git clone https://github.com/Transistor427/kiauh -b Z-BoltUI3
./kiauh/kiauh.sh
```

Ставим наш **KlipperScreen**:

```bash
cd ~
git clone https://github.com/Transistor427/KlipperScreen -b Z-BoltUI3
cd ~/KlipperScreen/scripts
./install-debian.sh
```

После установки софта перезагружаемся:

```bash
sudo reboot
```

### 01. Включаем OVERLAY

```bash
sudo rsetup
```

Переходим по меню:&#x20;

_Overlays -> Manage overlays -> Enable RPi 7 inch Touchscreen_

{% hint style="info" %}
Жмем _**Пробел**_, чтобы выбрать пункт.
{% endhint %}

Кнопкой **Tab** переключаемся на _**Ok**_, далее жмем _**Enter**_

Выходим кнопкой _**Esc**_

### 02. Настраиваем режим GUI

```bash
sudo systemctl set-default multi-user.target
```

### 03. Редактируем конфиг X-сервера

Открываем файл командой:

```bash
sudo nano /etc/X11/Xwrapper.config
```

Добавляем в начало файла строчку:

```bash
needs_root_rights=yes
```

Сохраняем и выходим:

**Ctrl+S, Ctrl+X**

### 04. Собираем Klipper MCU под Rock Pi

Производим манипуляции из[ документации клиппера](https://www.klipper3d.org/RPi_microcontroller.html):

```
cd ~/klipper/
sudo cp ./scripts/klipper-mcu.service /etc/systemd/system/
sudo systemctl enable klipper-mcu.service
```

Собираем клиппер под Rock Pi:

<pre class="language-bash" data-overflow="wrap"><code class="lang-bash"><strong>cd ~/klipper
</strong><strong>make menuconfig
</strong></code></pre>

В меню «Архитектура микроконтроллера» установите «Процесс Linux», затем сохраните и выйдите.

Чтобы собрать и установить новый код микроконтроллера, выполните команды:

```bash
sudo service klipper stop
make flash
sudo service klipper start
```

{% hint style="warning" %}
Если klippy.log сообщает об ошибке «Отказано в доступе» при попытке подключения к /tmp/klipper\_host\_mcu, вам необходимо добавить пользователя в группу tty. Следующая команда добавит пользователя «rock» в группу tty:

```bash
sudo usermod -a -G tty rock
```
{% endhint %}

Перезагружаем принтер командой:

```bash
sudo reboot
```

## Настройка GPIO

### 01. Расчет пина

Заходим в документацию Rock Pi:

{% hint style="info" %}
Ссылка на документацию Rock Pi по работе с GPIO:

[https://wiki.radxa.com/Rock4/hardware/gpio](https://wiki.radxa.com/Rock4/hardware/gpio)
{% endhint %}

В документации есть таблица с пинами GPIO Rock Pi, их номерами и позициями.

Выбираем, какой пин нам нужен, например **GPIO4\_D4**

Далее нужно понять, какой номер у этого пина

Производим расчет:

<mark style="color:blue;">**GPIO4**</mark>**\_**<mark style="color:red;">**D**</mark><mark style="color:green;">**4**</mark>**&#x20;= 8 \* 3 + 4 = 28**

где:

GPIO**4 -**&#x20;

**\_D -** в зависимости от буквы меняется число, например если пин GPIO4\_D4, то буква **D**, значит число **3**

{% hint style="info" %}
A = 0, B = 1, C = 2, D = 3
{% endhint %}

8 \* **3 - 3 - это число из расчета выше**

GPIO4\_D**4** = 8 \* 3 + **4**

**4** - это число после буквы **D**

Производим расчет:

<mark style="color:blue;">**GPIO4**</mark>**\_**<mark style="color:red;">**D**</mark><mark style="color:green;">**4**</mark>**&#x20;= 8 \* 3 + 4 = 28**

Итого путем математических расчетов получаем число **28**

### 02. GPIO в конфигурационном файле

Инициализируем новый MCU файле printer.cfg:

```django
[mcu rock_pi]
serial: /tmp/klipper_host_mcu
```

Использование пина GPIO как выходного пина:

```django
[output_pin GP]
pin: rock_pi:gpiochip4/gpio28
value: 1
```

где:

<mark style="color:blue;">**rock\_pi**</mark> - название, которое дали при инициализации MCU

<mark style="color:red;">**gpiochip4**</mark> - номер "банки" (то, что в GPIO<mark style="color:red;">**4**</mark>\_D4 цифра <mark style="color:red;">**4**</mark>)

<mark style="color:green;">**gpio28**</mark> - <mark style="color:green;">**28**</mark> число, которое получиили методом расчета выше

{% hint style="success" %}
На пинах GPIO Rock Pi 4B+ 3 вольта
{% endhint %}

{% hint style="info" %}
Для просмотра статуса конкретного пина в системе можно воспользоваться командой:

```bash
sudo gpioinfo
```
{% endhint %}

**Готово! Теперь можно рулить GPIO из конфига принтера.**

## Исправление ошибки сервиса dnsmasq

{% hint style="info" %}
[https://unix.stackexchange.com/questions/690523/dnsmasq-failed-to-create-listening-socket-for-127-0-0-1-address-already-in-use](https://unix.stackexchange.com/questions/690523/dnsmasq-failed-to-create-listening-socket-for-127-0-0-1-address-already-in-use)
{% endhint %}

```
sudo systemctl stop systemd-resolved
sudo systemctl disable systemd-resolved
sudo systemctl mask systemd-resolved
```

## Запуск нашей версии KlipperScreen (Z-BOLTUI2)

Подключаемся по SSH к принтеру и вводим команду:

```bash
sudo nano /etc/X11/Xwrapper.conf
```

В начало записываем строчку:

```bash
needs_root_rights=yes
```

Сохраняем и выходим:

**Ctrl+S, Ctrl+X**

Далее настраиваем права командой:

```bash
sudo visudo
```

Записываем в конец конфига строчку:

```bash
rock ALL=(ALL) NOPASSWD:ALL
```

Сохраняем и выходим:

**Ctrl+S, Ctrl+X**

Перезагружаемся командой:

```bash
sudo reboot
```

## Исправление ошибки неподключения к WIFI в KS (в оригинальном KS и в нашем KS -b Z-BOLTUI2)

Создаем файл настройки конфигурации сети:

```bash
sudo nano /var/lib/polkit-1/localauthority/50-local.d/10-network-manager.pkla
```

Вписываем туда следующее содержимое:

```bash
[Allow rock modifying all network states and settings]
Identity=unix-user:rock
Action=org.freedesktop.NetworkManager.*
ResultAny=yes
ResultInactive=yes
ResultActive=yes
```

Сохраняем и выходим:

**Ctrl+S, Ctrl+X**

Создаем файл настройки доступа к сети:

```bash
sudo nano /etc/NetworkManager/conf.d/any-user.conf
```

Вставляем туда следующее содержимое:

```bash
[main]
auth-polkit=false
```

Сохраняем и выходим:

**Ctrl+S, Ctrl+X**

Перезагружаемся командой:

```bash
sudo reboot
```

После перезагрузки пробуем подключиться к WIFI.
