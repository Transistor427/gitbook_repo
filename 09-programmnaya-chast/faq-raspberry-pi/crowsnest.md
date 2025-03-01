---
description: Установка и настройка демона веб-камеры Crowsnest
---

# 🎥 Crowsnest

{% embed url="https://github.com/mainsail-crew/crowsnest" %}
Ссылка на репозиторий Crowsnest
{% endembed %}

{% embed url="https://crowsnest.mainsail.xyz/configuration/cam-section" %}
Параметры конфигурационного файла
{% endembed %}

Подключаемся к принтеру по SSH.

Скачиваем и устанавливаем Crowsnest командами:

```bash
cd ~
git clone https://github.com/mainsail-crew/crowsnest.git
cd ~/crowsnest
sudo make install
```

Проверяем список USB-камер командой:

```bash
ls /dev/serial/by-id/
```

После установки открываем конфигурационный файл:

```bash
sudo nano ~/printer_data/config/crowsnest.conf
```

Далее редактируем файл так же, как и ниже:

{% code fullWidth="true" %}
```tsconfig
[crowsnest]
log_path: /home/pi/klipper_logs/crowsnest.log
log_level: verbose                      # Valid Options are quiet/verbose/debug
delete_log: false                       # Deletes log on every restart, if set to true
no_proxy: false

[cam raspi]
mode: camera-streamer                   # ustreamer - Provides mjpg and snapshots. (All devices)
                                        # camera-streamer - Provides webrtc, mjpg and snapshots.(rpi + Raspi OS based only
enable_rtsp: true                       # If camera-streamer is used, this enables also usage of an rtsp server
rtsp_port: 8554                         # Set different ports for each device!
port: 8080                              # HTTP/MJPG Stream/Snapshot Port
device: /dev/v4l/by-id/usb-046d_0825_3F6321B0-video-index0 # See Log for available ...
resolution:1280x720                     # widthxheight format
max_fps: 15                             # If Hardware Supports this it will be forced, otherwise ignored/coerced.
```
{% endcode %}

После внесения изменений сохраняем и выходим: Ctrl+S, Ctrl+X

Перезагружаем принтер командой:

```bash
sudo reboot
```
