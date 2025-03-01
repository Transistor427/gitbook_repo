---
description: Инструкция по кастомизации нового KlipperScreen
---

# 🖥️ KlipperScreen 5.10 FAQ

## Добавление кнопок в боковую панель (wifi и shutdown)

Открываем файл panels/base\_panel.py

Для кнопки **wifi**

В начале добавляем:

```python
self.wifipanel = {
        "name": _('Network'),
        "panel": "network",
        "icon": "network"
}
self.control['wifi'] = self._gtk.Button('network', scale=abscale)
self.control['wifi'].connect("clicked", self.menu_item_clicked, self.wifipanel)
```

<figure><img src="../../../.gitbook/assets/изображение (37).png" alt=""><figcaption></figcaption></figure>

Включаем отображение:

```python
self.action_bar.add(self.control['wifi'])
```

<figure><img src="../../../.gitbook/assets/изображение (38).png" alt=""><figcaption></figcaption></figure>

Активируем кнопку:

```python
for control in ('wifi'):
    self.set_control_sensitive(True, control='wifi')
```

<figure><img src="../../../.gitbook/assets/изображение (39).png" alt=""><figcaption></figcaption></figure>



Для кнопки **shutdown**

В начале файле возле остальный кнопок добавляем:

```python
self.control['shutdown'] = self._gtk.Button('shutdown', scale=abscale)
        self.control['shutdown'].connect ("clicked", self.shutdown)
```

<figure><img src="../../../.gitbook/assets/изображение (35).png" alt=""><figcaption></figcaption></figure>

Включаем отображение:

```python
self.action_bar.add(self.control['shutdown'])
```

<figure><img src="../../../.gitbook/assets/изображение (34).png" alt=""><figcaption></figcaption></figure>

Активируем кнопку:

```python
for control in ('shutdown'):
    self.set_control_sensitive(True, control='shutdown')
```

<figure><img src="../../../.gitbook/assets/изображение (36).png" alt=""><figcaption></figcaption></figure>

В конец добавить:

```python
def shutdown(self, widget):
    if self._screen.printer.state != "disconnected":
        self._screen._confirm_send_action(widget, _("Are you sure you wish to shutdown the system?"), "machine.shutdown")
    else:
        logging.info("OS Shutdown")
        os.system("systemctl poweroff")
```

## Изменение отображение нагревателей на главном экране



**Еще не разобрался...**



## Убираем Spoolman из меню экструзия (если не установлен, то не нужно)

Отрываем файл panels->extrude.py

В нем нужно закомментировать все строки с надписью "spoolman"

<figure><img src="../../../.gitbook/assets/изображение (30).png" alt=""><figcaption></figcaption></figure>

В секции enable\_buttons нужно убрать spoolman

<figure><img src="../../../.gitbook/assets/изображение (31).png" alt=""><figcaption></figcaption></figure>

## Редактирование сетки меню

В файле panels->menu.py меняем кол-во столбцов на 4

<figure><img src="../../../.gitbook/assets/изображение (32).png" alt=""><figcaption></figcaption></figure>

## Настройка панели обновлений

Файл default.conf меняем updates на sustem

<figure><img src="../../../.gitbook/assets/изображение (33).png" alt=""><figcaption></figcaption></figure>

## Настройка панели сети

Устанавливаем программу для генерации qr-кодов:

```bash
sudo apt-get install qrencode
```

Комментируем все строки, где есть IPv6:

<figure><img src="../../../.gitbook/assets/изображение (40).png" alt="" width="375"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/изображение (41).png" alt="" width="268"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/изображение (42).png" alt="" width="375"><figcaption></figcaption></figure>

Далее добаляем строчки:

### 01. Кнопка с QR-кодом IP-адреса для старого KS

Устанавливаем программу qrencode

```bash
sudo apt install qrencode
```

Добавляем иконку ниже в папку по пути styles->z-bolt->images/qrcode.svg

<figure><img src="../../../.gitbook/assets/qrcode (1).svg" alt=""><figcaption><p>QR-код для иконки KS (он белый на белом фоне)</p></figcaption></figure>

Далее в файле panels->network.py добавляем следующие строки&#x20;

<figure><img src="../../../.gitbook/assets/изображение (242).png" alt=""><figcaption><p><strong>Путь, где будет сохраняться сгенерированный qr-код</strong></p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/изображение (243).png" alt=""><figcaption><p><strong>Создание кнопки</strong></p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/изображение (244).png" alt=""><figcaption><p><strong>Включение отображения</strong></p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/изображение (245).png" alt=""><figcaption><p><strong>Функция генерирования QR-кода и его отображения</strong></p></figcaption></figure>



### 02. Кнопка с QR-кодом IP-адреса для нового KS

<figure><img src="../../../.gitbook/assets/изображение (227).png" alt="" width="325"><figcaption></figcaption></figure>

```python
self.filename = "/home/rock/printer_data/logs/qrcode.png"
```

<figure><img src="../../../.gitbook/assets/изображение (228).png" alt="" width="375"><figcaption></figcaption></figure>

```python
    def show_fullscreen_qrcode(self, widget):
    
        ifadd = netifaces.ifaddresses(self.interface)
        curr_ip = ifadd[netifaces.AF_INET][0]['addr']
        logging.info(f"Generate QR-code with IP: {curr_ip}")
        os.system(f'qrencode -s 10 -l H -o "{self.filename}" "{curr_ip}"')
        logging.info(f"Generate QR-code")
    
        buttons = [
            {"name": _("Close"), "response": Gtk.ResponseType.CANCEL}
        ]
    
        image = Gtk.Image.new_from_file(self.filename)
        box = Gtk.Box(orientation=Gtk.Orientation.VERTICAL)
        box.add(image)
        box.set_vexpand(True)
        self._gtk.Dialog(self.filename, buttons, box, self._gtk.remove_dialog)
        logging.info(f"Show QR-code")
    
    def close_fullscreen_qrcode(self, dialog):
        self._gtk.remove_dialog
```



<figure><img src="../../../.gitbook/assets/изображение (229).png" alt="" width="375"><figcaption></figcaption></figure>

```python
        qrcode = self._gtk.Button("qrcode", None, "color1", .88)
        qrcode.connect("clicked", self.show_fullscreen_qrcode)
        qrcode.set_hexpand(False)
        qrcode.set_halign(Gtk.Align.END)
```

<figure><img src="../../../.gitbook/assets/изображение (230).png" alt="" width="347"><figcaption></figcaption></figure>

```python
buttons.pack_end(qrcode, False, False, 0)
```

Добавляем в папку KlipperScreen->style->z-bolt/images файл qrcode.svg (он ниже белый на белом фоне)&#x20;

<figure><img src="../../../.gitbook/assets/qrcode.svg" alt=""><figcaption><p>Файл qrcode.svg</p></figcaption></figure>



