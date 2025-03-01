---
description: Информация по изменению KlipperScreen'а
---

# 🖥️ KlipperScreen FAQ

### &#x20;Настройка размеров букв и картинок: <a href="#docs-internal-guid-0f8aad76-7fff-834c-c7c7-6daba68544ef" id="docs-internal-guid-0f8aad76-7fff-834c-c7c7-6daba68544ef"></a>

Файл **/home/pi/KlipperScreen/ks\_includes/KlippyGtk.py**

`font_ratio = 40` # При увеличении текст уменьшается (51)

`width_ratio = 12` # При увеличении размер картинок уменьшается (16)

`height_ratio = 5.375` # При увеличении размер картинок уменьшается (9.375)

`self.header_image_scale_width = 0.6` #Изменение ширины кнопок назад и домой (1.2)

`self.header_image_scale_height = 0.8` #Изменение высоты кнопок назад и домой (1.4)

### Чтобы менять кнопки в левой панели:

**Файл /home/pi/KlipperScreen/ks\_includes/screen\_panel.py**

self.layout = Gtk.Layout()

self.layout.set\_size(self.\_screen.width, self.\_screen.height)

button\_scale = self.\_gtk.get\_header\_image\_scale()

logger.debug("Button scale: %s" % button\_scale)

if back == True:

self.control\['back'] = self.\_gtk.ButtonImage('back', None, None, button\_scale\[0], button\_scale\[1])

self.control\['back'].connect("clicked", self.\_screen.\_menu\_go\_back)

self.layout.put(self.control\['back'], 0, 0) # 0 - изменяет расстояние кнопки от краев

&#x20;   self.control\['home'] = self.\_gtk.ButtonImage('home', None, None, button\_scale\[0], button\_scale\[1])

&#x20;   self.control\['home'].connect("clicked", self.menu\_return, True)

&#x20;   self.layout.put(self.control\['home'], self.\_screen.width - round(

&#x20;   self.\_gtk.get\_image\_width() \* button\_scale\[0] \* 1.4), 0) #1.4 изменяет расстояние кнопки от краев

### Убрать кнопку экстренного стопа в левой панели:

Файл **\~/KlipperScreen/panels/base\_panel.py**

&#x20;  \#self.control\['estop'] = self.\_gtk.ButtonImage('emergency', None, None, button\_scale\[0], button\_scale\[1])

&#x20;  \#self.control\['estop'].connect("clicked", self.emergency\_stop)

&#x20;  \#self.layout.put(self.control\['estop'], int(self.\_screen.width/4\*3 - button\_scale\[0]/2), 0)

### Изменение размера картинок равнения стола по точкам:

Файл **/home/pi/KlipperScreen/panels/bed\_level.py**

self.labels\['bl'] = self.\_gtk.ButtonImage("bed-level-t-l", None, None, 2, 2) # (3,3) - стандартные значения

&#x20;       self.labels\['bl'].connect("clicked", self.go\_to\_position, self.screws\[2])

&#x20;       self.labels\['br'] = self.\_gtk.ButtonImage("bed-level-t-r", None, None, 2, 2)# (3,3)

&#x20;       self.labels\['br'].connect("clicked", self.go\_to\_position, self.screws\[3])

&#x20;       self.labels\['fl'] = self.\_gtk.ButtonImage("bed-level-b-l", None, None, 2, 2)# (3,3)

&#x20;       self.labels\['fl'].connect("clicked", self.go\_to\_position, self.screws\[0])

&#x20;       self.labels\['fr'] = self.\_gtk.ButtonImage("bed-level-b-r", None, None, 2, 2)# (3,3)

&#x20;       self.labels\['fr'].connect("clicked", self.go\_to\_position, self.screws\[1])

### Убираем  отображение IPV6 во вкладе Сеть

Файл **\~/KlipperScreen/panels/network.py**

if netinfo\['connected'] == True:

&#x20;           stream = os.popen('hostname -f')

&#x20;           hostname = stream.read().strip()

&#x20;           ifadd = netifaces.ifaddresses(self.interface)

&#x20;           ipv4 = ""

&#x20;           ipv6 = ""

&#x20;           if netifaces.AF\_INET in ifadd and len(ifadd\[netifaces.AF\_INET]) > 0:

&#x20;              ipv4 = "\<b>%s:\</b> %s " % (\_("IPv4"), ifadd\[netifaces.AF\_INET]\[0]\['addr'])

&#x20;           if netifaces.AF\_INET6 in ifadd and len(ifadd\[netifaces.AF\_INET6]) > 0:

&#x20;              ipv6 = ipv6 = "\<b>%s:\</b> %s " % (\_("IPv6"), ifadd\[netifaces.AF\_INET6]\[0]\['addr'].split('%')\[0])

&#x20;              connected = "\<b>%s\</b>\n\<b>%s:\</b> %s\n%s\n" % (\_("Connected"),\_("Hostname"),hostname, ipv4)

Заменить нижнюю строчку на верхнюю

&#x20;   \#connected = "\<b>%s\</b>\n\<b>%s:\</b> %s\n%s%s\n" % (\_("Connected"),\_("Hostname"),hostname, ipv4, ipv6)

### Создание тестовой сети для инициализации WIFI           &#x20;

&#x20;    Примечание: делается через линукс либо SSH     &#x20;

&#x20;   Файл /etc/wpa\_supplicant/wpa\_supplicant.conf - добавляем сеть zbtest с паролем 11111111

&#x20;   Файл /boot/fluidd-wpa\_supplicant.conf - добавляем сеть zbtest с паролем 11111111

### Изменение размера шрифтов

&#x20;   /home/pi/KlipperScreen/styles/z-bolt/styles.css

### Убрать вывод информации при загрузке

Заменить содержимое файла /boot/cmdline.txt на это:

console=serial0,115200 console=tty3 root=PARTUUID=99040e20-02 rootfstype=ext4 elevator=deadline fsck.repair=yes rootwait logo.nologo consoleblank=0 loglevel=3 vt.global\_cursor\_default=0 quite

### Обнуление пробега

Если во FluiddPI не получается сбить "пробег" принтера, то необходимо заменить базу мунрейкера (\~/.moonraker\_database/data.mdb) на базу с нулевым пробегом (находится в папке с этим файлом). Открываем WinSCP, подключаемся по IP к принтеру, включаем отображение скрытых файлов (параметры - настройки - панели - показывать скрытые файлы). Идем в папку /home/pi/.moonraker\_database и меняем файл  data.mdb на наш девственный. Перезагружаем систему. В вебинтерфейсе флюида на вкладке НАСТРОЙКИ переименовываем имя принтера с Z-Bolt L32 на необходимую модель.

### Прочее

Moonraker/home/pi/moonraker/moonraker/components - все файлы для мунрейкера

machine.py - настройки действий на кнопки выключения в панели system.py

power.py - настройки&#x20;

### Добавление удаленного отображения экрана для кастомизации klipperscreen

* Заходим в принтер по SSH
* sudo apt-get update & sudo apt-get upgrade
* sudo raspi-config
* третий пункт (interface settings)
* третий пункт (VNC……)
* да

Качаем устанавливаем  прогу  RealVNC viewer

Запускаем RealVNC viewer, вводим IP принтера, явки, пароли, видим рекламу, возвращаемся в SSH И вводим:

sudo systemctl stop vncserver-x11-serviced.service

sudo reboot

ждем некоторое время, переподключаемся и видим экран принтера.

### Редактирование структуры меню

SSH

nano \~/KlipperScreen/ks\_includes/defaults\_simple.conf

&#x20;перезагрузка после сохранения изменений:

sudo systemctl restart KlipperScreen.service\


Вики по клипперскрину: [https://klipperscreen.readthedocs.io/en/latest/Configuration/#configuration](https://klipperscreen.readthedocs.io/en/latest/Configuration/#configuration)

### Изменение бранча, на который ссылается конкретный принтер при обновлении (актуально для сильно кастомных принтеров и для разработчиков)

1. Создаем новый бранч в репозитории https://github.com/Z-Bolt/KlipperScreen

например с помощью Github Desktop, если мы не скиловые консольные программисты:

![](https://lh7-us.googleusercontent.com/xXTEKWgAB_2qXQd1R141j1k1hB_ByxZlKKx6cVFozxEicjNT_7q8497j60ewCelVBmxWiX8oAdtZbnmgSPHh1arcyDC0kJpP25ZlajiDbKG5ve8Fw1UABKPZdiZmMSfIgTQX1DT0Mi2rUaK5hC66ow)

Обзываем его как-нибудь, например Z-BoltUI-S400dev.

2. Заходим в вебморду принтера по адресу 192.168…… , идем на вкладку КОНФИГУРАЦИЯ и редактируем файл moonraker.conf.

Ближе к низу меняем строку&#x20;

primary\_branch: Z-BoltUI

на

primary\_branch: Z-BoltUI-S400dev

Сохраняем, перезагружаем.

3. Заходим в принтер по SSH (Putty, Kitty и т.п.), pi/raspberry, пишем в командной строке:

&#x20;mv ./KlipperScreen ./KlipperScreen\_old (переименовываем папку клипперскрина на \_олд, можно просто удалить, но оставляем бэкап)

git clone [https://github.com/Z-Bolt/KlipperScreen](https://github.com/Z-Bolt/KlipperScreen) –branch Z-BoltUI-S400dev (создаем новую папку KlipperScreen, которая ссылается уже не на основную ветку, а на наш свежесозданный бранч)

4. Проверяем, что всё получилось командами:

cd KlipperScreen

git branch

Принтер должен ответить зеленой строкой в которой есть название нашего бранча.

5. Заходим через экран принтера в меню КОНФИГУРАЦИЯ - СИСТЕМА и обновляем klipperscreen и moonraker (значки обновить СЛЕВА), затем перезагружаем клиппер и прошивку. Всё должно обновиться и заработать. Если нет - выключаем из розетки и включаем. Теперь точно должно заработать)))).

### Подключение по SSH через VS

1. В расширениях качаем Remote Development&#x20;



2.После установки в левом нижнем углу появится зеленая херь\
![](https://lh7-us.googleusercontent.com/KC9dsIpBt-yM9D9YwXySc2WWWRvdYhbrK9vKAl_0O-1E7Ar56SrirPjL81Vxe6RcEPR3lGpOjdLpKobJsyR1EHoXIcTfUx5MGrq5usjGm93KINH13F1N4k4uZXG3Kl-Jnn2eQbTnm9bODV_FDrbywQ)

3.Нажимаем  и в разделе Remote-SSH выбираем (Open SSH Conf file)\
![](https://lh7-us.googleusercontent.com/huocmYovMztC0WbdbPkMr9Gy0Nn1ldmxYR2m9dyWysUWE2geUZxrw-dJLMJAP_v-G0127TmhqCAnhlkjPi_HcIAfphn-wmSlkE2E28R8YNdtUQfgs1gJpSp2naftPRp_B5W_g4G6pOCJegjfhBImvA)

4.Далее выбираем директорию пользователя&#x20;

![](https://lh7-us.googleusercontent.com/3hGqxpdI4OdAfPJJu2RVQxARqF9OeRKieHEShxz1db1Olix33thOTh6kWb9mPB2q06sM6i39DXV9EonQ4HglgKBDjElJWwx_e1eK1vB7wzq3W-ziqnBYoWQS2eCOh0mCCVRQ6z4lgiDR909wyd41Sg)

Откроется конфиг файл где устанавливаем параметры для входа\


Host 192.168….. (Можно и поменять роли не играет)

Host name 192.168.31.62 (Строчка гду указываем url принтера)

User pi \


5.После настройки снова нажимаем на Открытие удаленного сервера(зеленые стрелочки как в шаге 2). И выбираем  Connect to Host

![](https://lh7-us.googleusercontent.com/cXDo0v_MY9ZMJOeMiv15U2A9XdYQhpKdwsVZ9iEO7YC-o_z6yGc-iqOEpfHUhH76DlxDLYRVVfyy_njadTXeyeKpJV2qgSbUA85eIasKc4or4TlfL22w7dp8TviiAlJDykOoHUxZUs70S5jtKZ0k0w)

Выбираем Host к которому хотим подключиться, выбираем linux, вводим пароль, ждем загрузку конфигурации, открываем папку с файлами, если надо, то еще раз вводим пароль.

### Конфигурации версий  moonraker&#x20;

hom/pi/ -> /moonraker/ -> /moonracker/ -> /components/ -> /update\_manager/ -> /update\_manager.conf/

### Биндим кнопку с gcode

1. Создаем gcode для кнопки:&#x20;

Для этого заходим в голову принтера , конфигурация и в файле printer.cfg создаем gcode. Например:

\[gcode\_macro CLEAN\_NOZZLE]&#x20;

gcode:

&#x20; G28 X0

&#x20;  G28 Y0

сохраняем

2. Далее необходимо создать кнопку , которая выполнит этот процесс.

2.1 Если добавляем кнопку в defaults.conf , то в нужной нам панеле  добавляем,

в методе указываем

method: printer.gcode.script

а в параметр записываем название нашей кнопки

params: {"script":"CLEAN\_NOZZLE"}

2.2 Если добавляем кнопку на панели, сначала ее необходимо описать, возможно добавить действие ‘клика’ и далее

&#x20;для нее необходима ф-н, которая будет ссылаться на наш gcode

Например&#x20;

def clean\_nozzle(self, widget):

&#x20;       self.\_screen.\_ws.klippy.gcode\_script("CLEAN\_NOZZLE")
