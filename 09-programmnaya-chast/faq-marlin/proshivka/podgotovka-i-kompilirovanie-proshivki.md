---
description: Инструкция по подготовке и компилировании прошивки Marlin
---

# 🕹️ Подготовка и компилирование прошивки

## 01. Поиск прошивки

Скачиваем с нашего Github прошивку под нужный принтер с нужной конфигурацией.

{% hint style="info" %}
Ссылка на Github: [https://github.com/Z-Bolt/](https://github.com/Z-Bolt/Marlin-2.0-Z-Bolt-L2-allUART/)

Ссылка на репозиторий для примера:  [https://github.com/Z-Bolt/Marlin-2.0-Z-Bolt-L2-allUART/](https://github.com/Z-Bolt/Marlin-2.0-Z-Bolt-L2-allUART/)
{% endhint %}

## 02. Конфигурация

После скачивания репозитория распаковываем его и открываем в **настроенном** Visual Studio Code.

<figure><img src="../../../.gitbook/assets/изображение (52).png" alt="" width="375"><figcaption></figcaption></figure>

Для конфигурирования прошивки нам нужны 2 файла:

* Configuration.h
* Configuration\_adv.h

<figure><img src="../../../.gitbook/assets/Снимок экрана 2023-12-07 113030 — копия.png" alt="" width="183"><figcaption></figcaption></figure>

Кроме platformio нужно настроить под нужную нам плату. Делается это в файле platformio.ini в самом начале:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2023-12-07 113243.png" alt=""><figcaption><p>Конфигурация platformio.ini для SKR1.3</p></figcaption></figure>

{% hint style="info" %}
Список плат или контроллеров на них можно найти в том же файле пролистав ниже.
{% endhint %}

Возвращаемся к конфигурационным файлам Marlin. Данные файлы можно настраивать самому либо найти на нашем Github для конкретного принтера.

Основные места изменений:

* модель платы

```c
#ifndef MOTHERBOARD
  #define MOTHERBOARD BOARD_BTT_SKR_V1_3
#endif
```

* автовыключение

```c
#define PSU_CONTROL
```

* термисторы хотэнда и стола (перечень термисторов с их кодами в коде выше)

```c
#define TEMP_SENSOR_0 1047
#define TEMP_SENSOR_BED 1
```

* минимальная температура хотэнда и стола

```c
#define HEATER_0_MINTEMP   5
#define BED_MINTEMP        5
```

* максимальная температура хотэнда и стола

```c
#define HEATER_0_MAXTEMP 300
#define BED_MAXTEMP      150
```

* кинематика (стандартно оставляем COREXY)

```c
#define COREXY
```

* использование концевиков (для Limited Plus как в коде ниже)

```c
#define USE_XMIN_PLUG
// #define USE_YMIN_PLUG
#define USE_ZMIN_PLUG
//#define USE_IMIN_PLUG
//#define USE_JMIN_PLUG
//#define USE_KMIN_PLUG
//#define USE_XMAX_PLUG
#define USE_YMAX_PLUG
#define USE_ZMAX_PLUG
//#define USE_IMAX_PLUG
//#define USE_JMAX_PLUG
//#define USE_KMAX_PLUG
```

* модель драйвера двигателя

```c
#define X_DRIVER_TYPE  TMC2208
#define Y_DRIVER_TYPE  TMC2208
#define Z_DRIVER_TYPE  TMC2208
#define E0_DRIVER_TYPE TMC2208
```

* ускорения и рывки оставляем по дефолту
* использование ПГ с автоуровнем

```c
#define Z_MIN_PROBE_USES_Z_MIN_ENDSTOP_PIN
```

* инвертирование двигателей

```c
#define INVERT_X_DIR false
#define INVERT_Y_DIR false
#define INVERT_Z_DIR true
#define INVERT_E0_DIR false
```

* расположение концевиков

<pre class="language-c"><code class="lang-c">// Direction of endstops when homing; 1=MAX, -1=MIN
<strong>#define X_HOME_DIR -1
</strong>#define Y_HOME_DIR 1
#define Z_HOME_DIR -1
</code></pre>

* область построения

```c
#define X_BED_SIZE 299
#define Y_BED_SIZE 199
#define Z_MAX_POS 337
```

* включение автоуровня

```c
#define AUTO_BED_LEVELING_BILINEAR
```

* по скольки точкам строится автоуровень

```c
  #define GRID_MAX_POINTS_X 5
  #define GRID_MAX_POINTS_Y 3
```

* настройки дисплея

```c
#define LCD_LANGUAGE en
#define DISPLAY_CHARSET_HD44780 JAPANESE
#define LCD_INFO_SCREEN_STYLE 0
```

## 03. Компилирование

{% hint style="warning" %}
<mark style="color:red;">**ВНИМАНИЕ! Если при попытке скомпилировать прошивку возникают различные ошибки, то установите режим питания компьютера на экономный!**</mark>
{% endhint %}

Для компилирования прошивки нажмите кнопку Build в левом нижнем углу:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2023-12-07 114312 (1).png" alt=""><figcaption></figcaption></figure>

После окончания компиляции прошивку можно достать по пути **.pio -> build -> LPC1768 -> firmware.bin**

<figure><img src="../../../.gitbook/assets/Снимок экрана 2023-12-07 114816.png" alt=""><figcaption></figcaption></figure>

Далее закидываем этот файл на карточку, вставляем карточку в плату, подаем питание. Готово!
