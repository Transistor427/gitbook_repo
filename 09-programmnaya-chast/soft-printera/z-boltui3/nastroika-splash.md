---
description: Инструкция по настройке темы системы и загрузочного экрана на принтере
---

# ⭕ Настройка Splash

{% hint style="info" %}
[https://wiki.ubuntu.com/Plymouth](https://wiki.ubuntu.com/Plymouth)

[https://wiki.debian.org/plymouth](https://wiki.debian.org/plymouth)

[https://scribles.net/customizing-boot-up-screen-on-raspberry-pi/](https://scribles.net/customizing-boot-up-screen-on-raspberry-pi/)
{% endhint %}

Директория с темами на ядре 5.10:

<pre class="language-bash"><code class="lang-bash"><strong>/usr/share/plymouth/themes/
</strong></code></pre>

Получние списка с доступными темами:

```bash
sudo plymouth-set-default-theme -l
```

Активация темы по уполчанию:

```bash
sudo plymouth-set-default-theme -R z-bolt
```

{% hint style="info" %}
Ссылка на архив с темой Z-Bolt:

[https://drive.google.com/open?id=1wfn3VjBRgx7MR-yClRWTGwRmqkVnDPTI\&usp=drive\_fs](https://drive.google.com/open?id=1wfn3VjBRgx7MR-yClRWTGwRmqkVnDPTI\&usp=drive_fs)
{% endhint %}
