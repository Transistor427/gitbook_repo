---
description: Инструкция по подключению к принтерам по протоколу SSH
icon: terminal
cover: https://wallpapercave.com/wp/wp7727842.jpg
coverY: 0
---

# Подключение по SSH

## Средствами Windows

Нажимаем клавишу "Windows" на клавиатуре:

![](../.gitbook/assets/photo_2023-10-16_20-31-46.jpg)

Вводим слово "Терминал"

<figure><img src="../.gitbook/assets/изображение (190).png" alt=""><figcaption></figcaption></figure>

После чего нажимаем "Enter"

![](../.gitbook/assets/photo_2023-10-16_20-38-59.jpg)

В открывшемся окне вводим следующую команду (без кавычек):

{% hint style="info" %}
Стандартные логин и пароль на принтерах с Rock Pi:

Логин: **rock**

Пароль: **rock**

Стандартные логин и пароль на принтерах с Raspberry Pi:

Логин: **pi**

Пароль: **raspberry**

Стандартные логин и пароль на принтерах с BTT CP:

Логин: **biqu**

Пароль: **biqu**
{% endhint %}

{% hint style="warning" %}
IP-адрес принтера можно узнать в панели "Сеть" принтера (в левой панели изображение "Wifi")

![](<../.gitbook/assets/photo_2023-10-16_20-50-39 (1).jpg>)
{% endhint %}

```
ssh "логин"@"IP-адрес"
```

Далее вводим пароль.

{% hint style="danger" %}
При вводе пароля на экране **ничего не будет отображаться**, поэтому внимательно смотрим за языком при вводе и правильностью написания!
{% endhint %}

<figure><img src="../.gitbook/assets/изображение (192).png" alt=""><figcaption></figcaption></figure>

При правильности введенных логина и пароля в окне терминала выведеться следующее сообщение:

<figure><img src="../.gitbook/assets/изображение (194).png" alt=""><figcaption></figcaption></figure>

**Возможные проблемы:**

1. В случае неправильного ввода логина или пароля отобразиться следующее сообщение:

<figure><img src="../.gitbook/assets/изображение (193).png" alt=""><figcaption></figcaption></figure>

2. Если IP-адрес введен неправильно, то отобразиться следующее сообщение:

<figure><img src="../.gitbook/assets/изображение (195).png" alt=""><figcaption></figcaption></figure>

## Программой Putty

1. Скачиваем программу Putty с оффициального сайта.

{% hint style="info" %}
Ссылка на установочник: [https://the.earth.li/\~sgtatham/putty/latest/w64/putty-64bit-0.79-installer.msi](https://the.earth.li/~sgtatham/putty/latest/w64/putty-64bit-0.79-installer.msi)
{% endhint %}

2. Устанавливаем программу.

{% hint style="info" %}
Соглашаемся со всем, что предлагает установочник.
{% endhint %}

3. Запускаем программу. Она должна иметь вид, как на фото ниже.

<figure><img src="../.gitbook/assets/изображение (185).png" alt=""><figcaption><p>Putty</p></figcaption></figure>

4. В поле "Host Name (or IP address)" вводим IP-адрес принтера.

{% hint style="warning" %}
IP-адрес принтера можно узнать в панели "Сеть" принтера (в левой панели изображение "Wifi")

![](<../.gitbook/assets/photo_2023-10-16_20-50-39 (2).jpg>)
{% endhint %}

<figure><img src="../.gitbook/assets/Снимок экрана 2023-10-16 202004.png" alt=""><figcaption></figcaption></figure>

5. Жмем "Open".
6. В появившемся окне вводим логин, потом пароль.

{% hint style="info" %}
Стандартные логин и пароль на принтерах с Rock Pi:

Логин: **rock**

Пароль: **rock**
{% endhint %}

{% hint style="danger" %}
При вводе пароля на экране **ничего не будет отображаться**, поэтому внимательно смотрим за языком при вводе и правильностью написания!
{% endhint %}

<figure><img src="../.gitbook/assets/изображение (186).png" alt=""><figcaption></figcaption></figure>

7. При правильном выполнении предыдущих пунктов на терминал будет выглядеть так:

<figure><img src="../.gitbook/assets/изображение (187).png" alt=""><figcaption></figcaption></figure>

**Возможные проблемы:**

1. Если логин или пароль будут введены неверно, то  отобразиться следующее сообщение:

<figure><img src="../.gitbook/assets/изображение (188).png" alt=""><figcaption></figcaption></figure>

2. Если IP-адрес будет введен неправильно, то  отобразиться следующее сообщение:

<figure><img src="../.gitbook/assets/изображение (189).png" alt=""><figcaption></figcaption></figure>
