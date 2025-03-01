---
description: Инструкция по настройке временной зоны на принтере
---

# ⏲️ Настройка Timezone

1. Скачиваем и устанавливаем программу Putty.

{% hint style="info" %}
Ссылка на установочный файл с официального сайта: [ссылка](https://the.earth.li/~sgtatham/putty/latest/w64/putty-64bit-0.79-installer.msi)
{% endhint %}

2. Запускаем Putty.
3. В появившемся окне в поле 1 вводим IP-адрес принтер (узнать его можно в панели “Сеть” на экране принтера) и нажимаем на кнопку “Open” (2):

<figure><img src="https://lh7-us.googleusercontent.com/za26udDFlwt3TwSGo8wsFhcRGJaqDZCI3aLFcG_j6vPR9G1TNVzBCQeoHFaTmzi3Ki68IsnROC6CQBAtA_UpjuaXWGmpd_1x2suS0j6SuUFnCEYKAlDtORsvFdnvJ7tMwaP6IxqZNeSX3LcVqYN1lxKD9cm-PTAATT_p8rBvInFkfqYZPB6yRCUo5agPvw" alt="" width="375"><figcaption></figcaption></figure>

4. В появившемся окне нажимаем “Accept”:

<figure><img src="https://lh7-us.googleusercontent.com/WhZ7KdCwneaUFW_piHjw3iM6fWYKnGwMlorJV1pM548fp6AMef3R9Itn1nFCcVndePpCqAewf0DuVwuBo3iVgJlNpxtULRaLGPpW5nt11pBKLIeiBHdx-HQNemRQPMzQgYe4r8FdWh38Vcf2vcaITGd32mgICNET8O11LcA9rwAJGef6MQNpU8UwpUiE9Q" alt="" width="375"><figcaption></figcaption></figure>

5. Далее в окне терминала вводим данные авторизации:

{% hint style="info" %}
Логин: rock

Пароль: rock (При вводе пароля в терминале ничего отображаться не будет)
{% endhint %}

Для вводе логина жмем Enter и после ввода пароля жмем Enter

<figure><img src="https://lh7-us.googleusercontent.com/BeKrWDGEi9IZ38TGU47uR6PCTeXaidI2Uqdcyg7d71QQcz4xNNbercgND0VqcjpZAdeiFRdjaGWUxUycCcTTwivgrILtbdOLPoTtXBPkGuZZvGslYWpNHOM6d2QdhD2Wtw0Cc81mx2svKi1M26-utc9QuVMVH392LLCeVbfQ57G5tiS2Eqmu6sSbEIVNYg" alt="" width="375"><figcaption></figcaption></figure>

6. Смотрим список временных зон введя команду:

```bash
timedatectl list-timezones
```

<figure><img src="https://lh7-us.googleusercontent.com/HRrlZmWumGbdYQtF6GGKqRCX0FQmk-oX6e5i9moQbekGYjcfD1uzORldwYdV2rIrdmNbIykeiOvU9GQwvi9ebgravom-6im4-eX_I4UDyOhPLZLB8HBeedfy-TbQOJIHTJUbFwhwYpio-ifsze3V53ZSe303TtN6azl7ufh5pOmBQd-kA8pEGdMEo4l2gA" alt="" width="375"><figcaption><p>Список временных зон</p></figcaption></figure>

{% hint style="info" %}
Перемещаться по списку можно стрелочками “Вверх” и “Вних” на клавиатуре.
{% endhint %}

7. Находим необходимую временную зону, например “Europe/Minsk” (Вы выбираете свою).

<figure><img src="https://lh7-us.googleusercontent.com/4piMX9RZYBHNLBUHzTnPRPlkVrc_7gQrrMcviNx4lSpgqNAQTmNOZq08YNsRsLPVusoJjJFpLR6YeZU784UbwBhjq34owX-5DkL8UhhiK4kWTenjxpXl7ZsfZkEqOsqXvbF74CsHtPyzS_9NMGw0vM6n7tUtci_jrXERuu6ruej0WIqhnWt0oqStAT0JBQ" alt="" width="375"><figcaption></figcaption></figure>

8. Активируем временную зону командой:

```bash
timedatectl set-timezone Europe/Minsk
```

После ввода команды будет запрошен пароль: rock

<figure><img src="https://lh7-us.googleusercontent.com/f1bLSdZM32Eo7R5Ik3h-dnsKvdD61LnnObIF41oLLPxT3F-98G3DH-Lc-Xg1WYw2Ni6zxKbI04RuIX3ytPJwqf7M5CRgLPGPmtErzsdNCXQCVB54ZrTqHDpBL9Qq9i3VfTBygBoW1qY2m1NjLLwCSs7A0oCbE-o09iX_j-k5pLJ6eygIIJjC5KSq4_Vm1g" alt="" width="375"><figcaption></figcaption></figure>

9. Проверяем активацию временной зоны командой:

```bash
timedatectl
```

<figure><img src="https://lh7-us.googleusercontent.com/9WAsK7mgMXUm1V9OoHIf0WkVK-GxcKPDIrxfJevLSDcoAKyg_wAA4tuKDlBjufhTD3uYFP_2mVbhdsbS7im4EMt09IiBRxbTMfnBf4p46qqybM6P7kVI0-YfHihJkueS5IQQAH609oApKrzUzCs7N0flDO_eskmFVyty9HHxpvcDM155_ooPcAtrcilpQg" alt="" width="375"><figcaption></figcaption></figure>

10. Перезагружаем принтер командой:

```bash
sudo reboot
```

11. После перезагрузки принтера на экране отобразится время согласно установленной Вами временной зоны.
