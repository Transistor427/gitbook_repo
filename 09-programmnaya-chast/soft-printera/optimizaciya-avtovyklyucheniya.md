---
description: Инструкция по оптимизации автовыключения
---

# 😀 Оптимизация автовыключения

1. Заходим по SSH.
2. Вводим команду:

```bash
sudo nano ~/klipper_config/klipper-config/power.cfg
```

3. Меняем содержимое файла на следующее:

```django
#######################################
# POWER configuration
########################################
[gcode_macro M81]
description: Power off macro.
gcode:
  {action_call_remote_method("shutdown_machine")}
```

4. **Ctrl+S**, **ctrl+X** (сохраняем, закрываем)
5. Вводим команды:

```bash
sudo rm ~/PowerOFF.sh
sudo rm /etc/systemd/system/rc-local.service
```

6. Перезагружаемся командой:

```bash
sudo reboot
```

7. Проверяем, какие процессы грузят систему:

```bash
htop
```

Cреди нескольких самыми прожорливых процессов не должно быть **systemd-journal.**

В веб-интерфейсе проверяем работу автовыключения (команда M81).
