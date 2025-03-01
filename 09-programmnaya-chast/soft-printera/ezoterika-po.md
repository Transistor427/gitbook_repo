---
description: База, куда сохраняются всякие костыли ПО
---

# 🧙‍♂️ Эзотерика ПО

## Выполнение shell скриптов в KlipperScreen:

В начале файла должна быть импортирована библиотека OS:

```python
import os
```

Далее вставляем строчку (в ковычках команда):

```python
os.system("/bin/bash /home/rock/rotate_touch.sh")
```

## Выключение на старых PSU с экрана:

KlipperScreen -> panels -> base\_panel.py

В самом низу файла находим функцию:

```python
def shutdown(self, widget):
```

В ней в строке:

```python
self.screen.confirm_send_action(widget, _("bla bla bla"), "machine.shutdown")
```

Меняем:

```
"machine.shutdown"
```

На:

{% hint style="info" %}
Тут мы меняем метод **machine.shutdown** на **printer.gcode.script** с аргументом **script**
{% endhint %}

```
"printer.gcode.script", script
```

Также перед строкой добавляем переменную script со словарем:

{% hint style="info" %}
Тут мы объявляем  переменную **script**, которая содержит словарь **{"script":"M81"}**, где **"script"** - это ключ словаря, а **"M81"** - значение словаря (т.е. команда или макрос, который будет выполняться)
{% endhint %}

```
script = {"script":"M81"}
```

Должно получиться так:

<figure><img src="../../.gitbook/assets/изображение (226).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Для общего развития:

[https://moonraker.readthedocs.io/en/latest/web\_api/#run-a-gcode](https://moonraker.readthedocs.io/en/latest/web_api/#run-a-gcode)

![](<../../.gitbook/assets/изображение (235).png>)
{% endhint %}
