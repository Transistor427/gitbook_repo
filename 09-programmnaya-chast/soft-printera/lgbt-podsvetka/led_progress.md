# led\_progress

{% embed url="https://github.com/digitalninja-ro/klipper-neopixel/blob/master/led_progress.cfg" %}

## Настройка

Файл printer.cfg:

<figure><img src="../../../.gitbook/assets/изображение (7).png" alt=""><figcaption></figcaption></figure>

```django
[include klipper-config/led_progress.cfg]

[neopixel my_led]
pin: PD3 # пин уравления лентой на Spider
chain_count: 10 # кол-во светодиодов в ленте
```

Файл klipper-config/led\_progress.cfg:

&#x20;Создаем файл led\_progress.cfg и добавляем в него следующее содержимое:

```django
# use NEOPIXEL_DISPLAY LED=Led_Name TYPE=template_type MODE=template_mode

# for TYPE use:
# extruder_temp     :extruder temperature progress
# bed_temp          :bed temperature progress
# print_percent     :print progress
# printer_speed     :printer speed

# for MODE use:
# progress          :the leds will light up one by one
# glow              :all leds will fade from one color (or non) to other color

# more info: https://github.com/digitalninja-ro/klipper-neopixel/blob/master/README.md

[gcode_macro NEOPIXEL_DISPLAY]
gcode:
    {% raw %}
{% set led = params.LED %}
    {% set type = params.TYPE %}
    {% set mode = params.MODE %}
    {% set my_neopixel = printer.configfile.config['neopixel ' ~ led] %}

    {% if mode == 'progress' %}
        {% for i in range(my_neopixel.chain_count|int) %}
            SET_LED_TEMPLATE LED={led} INDEX={my_neopixel.chain_count|int - i} TEMPLATE={'led_' ~ type ~ '_' ~ mode} param_led_num={i+1} param_led_total={my_neopixel.chain_count|int}
        {% endfor %}
    {% endif %}
    {% if mode == 'glow' %}
        SET_LED_TEMPLATE LED={led} TEMPLATE={'led_' ~ type ~ '_' ~ mode}
    {% endif %}

[display_template led_extruder_temp_glow]
text:
    {% if printer.extruder.target > 0.0 %}
        {%  set temp = printer.extruder.target %}
    {% else %}
        {% set temp = printer.configfile.config.extruder.max_temp %}
    {% endif %}
    {% set ratio = printer.extruder.temperature / temp|float %}
    {ratio}, 0.0, {1-ratio}, 0.0

[display_template led_extruder_temp_progress]
param_led_num:  0
param_led_total: 1
text:
    {% if printer.extruder.target > 0.0 %}
        {%  set temp = printer.extruder.target %}
    {% else %}
        {% set temp = printer.configfile.config.extruder.max_temp %}
    {% endif %}
    {% set ratio = printer.extruder.temperature / temp|float %}
    {% set led_ratio = param_led_num|float / param_led_total %}
    {% if ratio > led_ratio %}
        {led_ratio}, 0.0, 0.0, 0.0
    {% else %}
        0.0, 0.0, 0.0, 0.0
    {% endif %}

[display_template led_bed_temp_glow]
text:
    {% if printer.heater_bed.target > 0.0 %}
        {%  set temp = printer.heater_bed.target %}
    {% else %}
        {% set temp = printer.configfile.config.heater_bed.max_temp %}
    {% endif %}
    {% set ratio = printer.heater_bed.temperature / temp|float %}
    {ratio}, 0.0, {1-ratio}, 0.0

[display_template led_bed_temp_progress]
param_led_num:  0
param_led_total: 1
text:
    {% if printer.heater_bed.target > 0.0 %}
        {%  set temp = printer.heater_bed.target %}
    {% else %}
        {% set temp = printer.configfile.config.heater_bed.max_temp %}
    {% endif %}
    {% set ratio = printer.heater_bed.temperature / temp|float %}
    {% set led_ratio = param_led_num|float / param_led_total %}
    {% if ratio > led_ratio %}
        0.0, 0.0, 0.0, 0.0
    {% else %}
        {led_ratio}, 0.0, 0.0, 0.0
    {% endif %}

[display_template led_print_percent_glow]
text:
    {% set ratio = printer.virtual_sdcard.progress %}
    0.0, {ratio}, 0.0, 0.0

[display_template led_print_percent_progress]
param_led_num:  0
param_led_total: 1
text:
    {% set ratio = printer.virtual_sdcard.progress %}
    {% set led_ratio = param_led_num|float / param_led_total %}
    {% if ratio > led_ratio %}
        0.0, {led_ratio}, 0.0, 0.0
    {% else %}
        0.0, 0.0, 0.0, 0.0
    {% endif %}

[display_template led_printer_speed_glow]
text:
    {% set ratio  = printer.motion_report.live_velocity|float /  printer.configfile.config.printer.max_velocity|float %}
    0.0, {ratio}, 0.0, 0.0

[display_template led_printer_speed_progress]
param_led_num:  0
param_led_total: 1
text:
    {% set ratio  = printer.motion_report.live_velocity|float /  printer.configfile.config.printer.max_velocity|float %}
    {% set led_ratio    = param_led_num|float / param_led_total %}
    {% if ratio > led_ratio %}
        0.0, {led_ratio}, 0.0, 0.0
    {% else %}
        0.0, 0.0, 0.0, 0.0
    {% endif %}
{% endraw %}
```

## Использование

Файл klipper-config/gcode-macros.cfg

```django
[gcode_macro START_PRINT]
gcode:
  NEOPIXEL_DISPLAY LED="my_led" TYPE=extruder_temp MODE=glow
  G21 ;metric values
  G90 ;absolute positioning
  M82 ;set extruder to absolute mode
  M107 ;start with the fan off
  G28 X0 Y0 Z0 ;home all
  M140 S{T_BED}
  M104 S160
  G1 X10 Y10 Z50 F900
  M190 S{T_BED}
  M109 S160
  G4 P180000 ;pause
  G34 ;bed tilt adjustment
  BED_MESH_CALIBRATE PRINT_MIN={params.PRINT_MIN} PRINT_MAX={params.PRINT_MAX} ;auto bed level
  G1 Z3 F1200 ;move the platform up 3mm
  G1 X0 Y0 F12000
  G1 Z0 F1200 ;move the platform down
  M104 S{T_EXTRUDER}
  M109 S{T_EXTRUDER}
  G1 Z3 F6000 ;move the platform up 3mm
  G92 E0 ;zero the extruded length
  ;intro line
  G1 X0 Y0 F5000
  G1 Z0.2 F2000
  G1 X50 E10 F1500
  G1 X100 E18 F1000
  G92 E0
  NEOPIXEL_DISPLAY LED="my_led" TYPE=print_percent MODE=progress
```

