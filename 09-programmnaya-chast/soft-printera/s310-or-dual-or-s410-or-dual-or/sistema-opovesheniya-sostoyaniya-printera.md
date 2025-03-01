---
description: Описание работы системы оповезения сосояния принтера
---

# 💡 Система оповещения состояния принтера

## 00 Подключение

Подключаем шлейф XH2,54-3pin к модулю индикатора как на фото:

<figure><img src="../../../.gitbook/assets/Индикатор.jpg" alt="" width="375"><figcaption></figcaption></figure>

Ответную часть шлейфа поключаем в Spider как показано на фото согласно распиновке:

<figure><img src="../../../.gitbook/assets/Подключение (1).jpg" alt="" width="375"><figcaption></figcaption></figure>

## 01 Настройка

Подключаемся по SSH.

Переходим в  домашнюю директорию:

```bash
cd ~
```

Клонируем репозиторий:

```bash
git clone https://github.com/julianschill/klipper-led_effect
```

Останавливаем сервис klipper:

```bash
sudo systemctl stop klipper
```

Создаем символическую ссылку:

```bash
ln -s ~/klipper-led_effect/src/led_effect.py ~/klipper/klippy/extras/led_effect.py
```

{% hint style="warning" %}
Если установлено новые ПО (не Z-BoltUI2), то выполнять действие не нужно!

Создаем копию moonraker.conf:

```
sudo cp -f ~/klipper_config/moonraker.conf ~/printer_data/config/
```

Выдаем права доступа для файла:

```
sudo chmod 777 ~/printer_data/config/moonraker.conf
```
{% endhint %}

Устанавливаем klipper-led\_effect:

```bash
cd ~/klipper-led_effect
./install-led_effect.sh
```

При удачной установке перезагружаем принтер командой:

```bash
sudo reboot
```

Переходим в веб-интерфейс принтера. Далее открываем панель "Конфигурация", папка "klipper-config".

Нажимаем на кнопку со значком "+" -> "Добавить файл" -> led-effects.cfg" -> "Сохранить"

<figure><img src="../../../.gitbook/assets/изображение (288).png" alt=""><figcaption></figcaption></figure>

Открываем созданный файл и вставляем следующее содержимое:

```django
########################################
# NEOPIXEL configuration
########################################

[neopixel led_state]
pin: PD3 # пин для управления светодиодами
chain_count: 5 # кол-во светодиодов в ленте

########################################
# LED effects configuration
########################################

[led_effect state_ready]
autostart:              true
frame_rate:             60
leds:
    neopixel:led_state
layers:
    breathing 10.00 1.00 add (0.0,0.7,0.0)
    static 0.00 0.00 top (0.0,0.1,0.0)

[led_effect state_wait]
autostart:              false
frame_rate:             60
leds:
    neopixel:led_state
layers:
    breathing 5.00 1.00 add (0.7,0.7,0.0) 
    static 0.00 0.00 top (0.1,0.1,0.0) 

[led_effect progress_print]
leds:
    neopixel:led_state (5-1)
autostart:                          false
frame_rate:                         60
layers:
    progress -1 0 add (0.0, 0.0, 1.0),(0.0, 0.0, 0.5)
    static 0 0 top (0.0, 0.0, 0.01)

[led_effect progress_extruder]
leds:
    neopixel:led_state (5-1)
autostart:                          false
frame_rate:                         60
heater:                             extruder
layers:
    heatergauge 50 0 add (0.5,0.0,0.0),(1.0,0.0,0.0)
    static 0 0 add (0.01,0,0)
    
#[led_effect progress_extruder1]
#leds:
#    neopixel:led_state (5-1)
#autostart:                          false
#frame_rate:                         60
#heater:                             extruder1
#layers:
#    heatergauge 50 0 add (0.5,0.0,0.0),(1.0,0.0,0.0)
#    static 0 0 add (0.01,0,0)

[led_effect process_cooldown]
leds:
    neopixel:led_state
autostart:                          false
frame_rate:                         60
layers:
    gradient 0.2 0.5 add (0.1, 0.025, 0.0),(1.0, 0.25, 0.0),(0.1, 0.025, 0.0)

[led_effect process_end]
autostart:              false
frame_rate:             60
leds:
    neopixel:led_state
layers:
    gradient 0.2 0.5 add (0.0, 0.0, 0.01),(0.0, 0.0, 0.7),(0.0, 0.0, 0.01)

[led_effect process_leveling]
autostart:              false
frame_rate:             60
leds:
    neopixel:led_state
layers:
    gradient 0.2 0.5 add (0.01, 0.0, 0.01),(0.7, 0.0, 0.7),(0.01, 0.00, 0.01)

########################################
# GCODE Macro configuration
########################################

[gcode_macro STATE_READY]
gcode:
    STOP_LED_EFFECTS
    SET_LED_EFFECT EFFECT=state_ready

[gcode_macro STATE_WAIT]
gcode:
    STOP_LED_EFFECTS
    SET_LED_EFFECT EFFECT=state_wait

[gcode_macro PROGRESS_PRINT]
gcode:
    STOP_LED_EFFECTS
    SET_LED_EFFECT EFFECT=progress_print

[gcode_macro PROGRESS_EXTRUDER]
gcode:
    STOP_LED_EFFECTS
    SET_LED_EFFECT EFFECT=progress_extruder
    
#[gcode_macro PROGRESS_EXTRUDER1]
#gcode:
#    STOP_LED_EFFECTS
#    SET_LED_EFFECT EFFECT=progress_extruder1

[gcode_macro PROCESS_COOLDOWN]
gcode:
    STOP_LED_EFFECTS
    SET_LED_EFFECT EFFECT=process_cooldown

[gcode_macro PROCESS_END]
gcode:
    STOP_LED_EFFECTS
    SET_LED_EFFECT EFFECT=process_end

[gcode_macro PROCESS_LEVELING]
gcode:
    STOP_LED_EFFECTS
    SET_LED_EFFECT EFFECT=process_leveling
```

Сохраняем и перезагружаем.

Далее открываем файл printer.cfg и вставляем строчку:

<figure><img src="../../../.gitbook/assets/изображение (289).png" alt=""><figcaption></figcaption></figure>

```django
[include klipper-config/led-effects.cfg]
```

Сохраняем и перезагружаем.

Открываем файл klipper-config -> gcode-macros.cfg и вносим изменения в макросы согласно скриншотам:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-24 122414.png" alt="" width="563"><figcaption><p>[START_PRINT]</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-24 122421.png" alt=""><figcaption><p>[END_PRINT]</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-24 122429.png" alt=""><figcaption><p>[COOLDOWN]</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-24 122450.png" alt=""><figcaption><p>[RESUME]</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-24 122533.png" alt=""><figcaption><p>[PAUSE]</p></figcaption></figure>

Сохраняем и перезагружаем.

Проверяем работу индикатора согласно разделу **02 Индикация**.

ДЛЯ КОНФИГУРАЦИИ ПРИНТЕРА DUAL

В файле **led-effects.cfg** (Веб-интерфейс -> вкладка "Конфигурация" -> klipper-config -> led-effects.cfg) необходимо раскомментировать секцию \[led\_effect progress\_extruder1]:

<figure><img src="../../../.gitbook/assets/изображение (293).png" alt=""><figcaption></figcaption></figure>

И макрос **PROGRESS\_EXTRUDER1:**

<figure><img src="../../../.gitbook/assets/изображение (296).png" alt=""><figcaption></figcaption></figure>

В файле **tools.cfg** (Веб-интерфейс -> вкладка "Конфигурация" -> klipper-config -> tools.cfg) в макросах **T0** и **T1** необходимо в начало добавить следующие строки:

В макрос T0:

```django
   {% raw %}
{% set ratio = printer.virtual_sdcard.progress %}
   {% if ratio == 0 %}
      PROGRESS_EXTRUDER
   {% endif %}
{% endraw %}
```

В макрос T1:

```django
   {% raw %}
{% set ratio = printer.virtual_sdcard.progress %}
   {% if ratio == 0 %}
      PROGRESS_EXTRUDER1
   {% endif %}
{% endraw %}
```

<figure><img src="../../../.gitbook/assets/изображение (291).png" alt=""><figcaption><p>Пример</p></figcaption></figure>

Настройка системы оповещения состояния принтера для конфигурации DUAL завершена.

## 02 Индикация

**Система оповещения состояния принтера** представляет собой модуль индикации (далее индикатор), предназначенный для оповещения оператора о состоянии принтера.

В таблице ниже представлен перечень состояний индикатора:

| **Обозначение индикатора**                                                                                                                             | <p><strong>Описание</strong><br></p>                                                   | **Состояние устройства**                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| ![](https://zbolt.happydesk.ru/api/file/download/f53b9c36-f558-4595-a9a8-8992576185ab)                                                                 | <p>Цвет: зеленый</p><p>Режим: дыхание<br>Макрос: STATE_READY</p>                       | Готов к работе                                                                   |
| ![](https://zbolt.happydesk.ru/api/file/download/d4b8594f-c8fa-4b34-bac5-58b9f817596d)                                                                 | <p> </p><p>Цвет: желтый</p><p>Режим: дыхание<br>Макрос: STATE_WAIT</p>                 | Ожидание                                                                         |
| ![](https://zbolt.happydesk.ru/api/file/download/de370d2d-c16f-49cb-976a-df1d8acc37b7)                                                                 | <p> </p><p>Цвет: синий</p><p>Режим: шкала<br>Макрос: PROGRESS_PRINT</p>                | Прогресс печати (активируется макросом, работает только при активной печати)     |
| <p><br></p><p><img src="https://zbolt.happydesk.ru/api/file/download/193f2d17-fc7d-4b40-8968-ebed75772ea3" alt="" data-size="original"></p><p><br></p> | <p>Цвет: красный</p><p>Режим:  шкала<br>Макрос:  PROGRESS_EXTRUDER</p>                 | Прогресс нагрева (активируется макросом, работает при включении нагрева хотенда) |
| <p><img src="https://zbolt.happydesk.ru/api/file/download/8b6166d8-d496-4cb3-b873-3abae3bc5f87" alt=""><br></p>                                        | <p> </p><p>Цвет: оранжевый</p><p>Режим: волна<br>Макрос: PROCESS_COOLDOWN</p>          | Отпуск детали (при активированном отпуске детали)                                |
| ![](https://zbolt.happydesk.ru/api/file/download/1af13bab-164a-49d9-86ad-7d32325cf64a)                                                                 | <p> </p><p>Цвет: синий</p><p>Режим: волна<br>Макрос: PROCESS_END</p>                   | Окончание печати                                                                 |
| ![](https://zbolt.happydesk.ru/api/file/download/7e064b73-1001-4ab8-a534-f7358acf692b)                                                                 | <p> </p><p>Цвет: фиолетовый</p><p>Режим: волна<br>Макрос: PROCESS_LEVELING</p><p> </p> | Работа автоуровня                                                                |

