---
description: Инструкция по настройке правильного включения и выключения PI4B CM4
icon: power-off
---

# \[OLD] Выключение на CM4

Подключаемся по SSH.

Переходим в директорию klipper командой:

```bash
cd ~/klipper
```

Далее останавливаем сервис klipper копируем файл сервиса mcu:

```bash
sudo service klipper stop
sudo cp ./scripts/klipper-mcu.service /etc/systemd/system/
```

Активируем сервис и включаем его в автозагрузку:

```bash
sudo systemctl enable klipper-mcu.service
```

Далее открываем меню конфигурации прошивки:

```bash
sudo make menuconfig
```

В пунке "Micro-controller Architecture" выбираем "Linux process":

<figure><img src="../../../.gitbook/assets/изображение (8).png" alt=""><figcaption></figcaption></figure>

Для выхода и сохранения жмём Q, далее Y.

Запускаем прошивку командой:

```bash
sudo make flash
```

После окончания прошивки перезагружаем принтер командой:

```bash
sudo reboot
```

Переходим в веб-интерфейс принтера, открываем файл power.cfg и вставляем в конец секцию ""POWER\_OFF":

```django
[output_pin POWER_OFF]
pin: rpi:gpio26
pwm: false
value: 0
```

Должно получиться так:

<figure><img src="../../../.gitbook/assets/изображение (9).png" alt="" width="251"><figcaption></figcaption></figure>

Жмём кнопку "Сохранить и перезагрузить".

Далее открываем файл printer.cfg и вставляем секцию \[mcu rpi]:

```django
[mcu rpi]
serial: /tmp/klipper_host_mcu
```

Должно получиться так:

<figure><img src="../../../.gitbook/assets/изображение (10).png" alt="" width="310"><figcaption></figcaption></figure>

Жмём кнопку "Сохранить и перезагрузить".

Провод подключается от GPIO3 на CM4 в разъем GPIO37 на PSU:

