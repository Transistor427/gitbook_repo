---
description: Инструкция по настройке стола с 9 регулировочными винтами
---

# 🪛 Screws tilt adjust

{% embed url="https://www.klipper3d.org/Config_Reference.html?h=screw#screws_tilt_adjust" %}

{% embed url="https://www.youtube.com/watch?v=APAbl5PGEh0" %}

Добавляем в файл bed.cfg секцию \[screws\_tilt\_adjust]:

```
[screws_tilt_adjust]
screw1: 0, 0
screw1_name: front left screw
screw2: 150, 00
screw2_name: front center screw
screw3: 300, 00
screw3_name: front right screw
screw4: 300, 150
screw4_name: center right screw
screw5: 150, 150
screw5_name: center center screw
screw6: 0, 150
screw6_name: center left screw
screw7: 0, 300
screw7_name: rear left screw
screw8: 150, 300
screw8_name: rear center screw
screw9: 300, 300
screw9_name: rear right screw
speed: 100 # 50
horizontal_move_z: 5
screw_thread: CCW-M4
```

<figure><img src="../.gitbook/assets/изображение (268).png" alt=""><figcaption></figcaption></figure>

Сохраняем и перезагружаем.

В терминале прописываем команды:

```
G28
SCREWS_TILT_CALCULATE
```

После окончания выполнения маркоса получаем такой вывод в терминал:

<figure><img src="../.gitbook/assets/изображение (269).png" alt="" width="563"><figcaption></figcaption></figure>

Далее подкручиваем винты согласно названию и необходимому числу оборотов, например:

rear right screw : x=290.0, y=290.0, z=-1.37809 : adjust CCW 01:25

* rear right screw  - название винта "задний правый винт".
* x=290.0, y=290.0, z=-1.37809 - координаты по X и Y, а также высота точки по Z.
* adjust CCW 01:25 - необходимо провернуть регулировочный винт против часовой стрелки (CW - по часовой, CCW - против часовой) на 1 полный оборот (01: - обозначает количество полных оборотов или же оборот часовой стрелки на стрелочных часах) и округленно еще на полоборота (:25 - это минуты на стрелочных часах. округляем до 30, т.е. полоборота).

После подкручивания всех винтов повторяем действие с пункта про команды до момента, пока максимальная разница между показаниями не составит **0,2 мм**.
