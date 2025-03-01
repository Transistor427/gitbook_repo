---
description: Инструкция по настройке (неочень) правильного выключения RPI CM4 через M81
icon: power-off
---

# Выключение системы для старых принтеров на RPI CM4

<pre class="language-bash"><code class="lang-bash"><strong>sudo nano ~/KlipperScreen/panels/shutdown.py
</strong></code></pre>

Листаем в самый низ и находим функцию def reboot\_poweroff\_confirm:

<figure><img src="../../../.gitbook/assets/{C2CA11D1-10BA-4736-AD28-92B2E95AF0A5}.png" alt=""><figcaption></figcaption></figure>

Добавляем следующую строчку в указанные на фото ниже места:

```python
self._screen._send_action(dialog, "printer.gcode.script", {"script": 'M81'})
```

<figure><img src="../../../.gitbook/assets/{AC424BEC-6B35-4CED-9544-FBE054F64630}.png" alt=""><figcaption></figcaption></figure>

Комментируем следующие строчки:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-11-03 114153.png" alt=""><figcaption></figcaption></figure>

```bash
sudo nano ~/KlipperScreen/panels/splash_screen.py
```

Листаем в самый низ и находим функцию def reboot\_poweroff\_confirm:

<figure><img src="../../../.gitbook/assets/{4A46FD0B-D509-432B-8FEF-3E4BC641AAA6}.png" alt=""><figcaption></figcaption></figure>

Добавляем строчки и комментируем:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-11-03 114414.png" alt=""><figcaption></figcaption></figure>

