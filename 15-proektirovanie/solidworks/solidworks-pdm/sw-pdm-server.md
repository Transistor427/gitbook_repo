---
description: Инструкция по установке и настройке сервера
---

# 💻 SW PDM Server

## 00. Необходимое ПО

Скачиваем установочники



Microsoft SQL Server 2019 и Update:





## 01. Установка и настройка

### Microsoft SQL Server 2019

{% hint style="info" %}
Ссылка на скачивание:

[https://rutracker.org/forum/viewtopic.php?t=5808010](https://rutracker.org/forum/viewtopic.php?t=5808010)
{% endhint %}



Запускаем установочный файл

<figure><img src="../../../.gitbook/assets/изображение (11).png" alt="" width="375"><figcaption></figcaption></figure>



Ключи:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-04 220918.png" alt="" width="375"><figcaption></figcaption></figure>





<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-04 221316.png" alt="" width="375"><figcaption></figcaption></figure>



<figure><img src="../../../.gitbook/assets/изображение (12).png" alt="" width="375"><figcaption></figcaption></figure>

Выбираем смешанный режим -> указываем пароль для администратора (его важно запомнить) -> ниже выбираем кнопку "Добавить текущего пользователя" -> Далее >

<figure><img src="../../../.gitbook/assets/изображение (13).png" alt="" width="375"><figcaption></figcaption></figure>





Запускаем Центр установки SQL Server:

<figure><img src="../../../.gitbook/assets/изображение (279).png" alt="" width="375"><figcaption></figcaption></figure>

Выбираем пункт "Новая установка изолированного экземпляра SQL Server".

<figure><img src="../../../.gitbook/assets/изображение (280).png" alt="" width="375"><figcaption></figcaption></figure>

Далее.

Выполнить новую установку SQL Server 2019.

<figure><img src="../../../.gitbook/assets/изображение (281).png" alt="" width="375"><figcaption></figcaption></figure>

Далее.

Введите ключ продукта:

```
PMBDC-FXVM3-T777P-N4FY8-PKFF4
```

<figure><img src="../../../.gitbook/assets/изображение (282).png" alt="" width="375"><figcaption></figcaption></figure>

Далее.

Ставим галочку в пункте "Я принимаю условия лицензии".

Далее.

Ставим галочки как на фото:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-04 221316.png" alt="" width="375"><figcaption></figcaption></figure>

Далее.

Именованный экземпляр.

<figure><img src="../../../.gitbook/assets/изображение (283).png" alt="" width="375"><figcaption></figcaption></figure>

Далее.

Далее.

Смешанный режим.

Указываем пароль для учетной записи администратора базы данных.

Добавит текущего пользователя.

<figure><img src="../../../.gitbook/assets/изображение (284).png" alt="" width="375"><figcaption></figcaption></figure>

Далее.

Проверяем все пункты и жмём "Установить".

Дожидаемся окончания установки и переходим к установке Solidworks PDM.

### Solidworks PDM

{% hint style="warning" %}
При установке Solidworks PDM обязательно необходимо отключить доступ к интернету!
{% endhint %}

Запускаем менеджер установки Solidworks 2021 SP5.

Выбираем пункт "Установить компоненты сервера" и ставим галочки также, как на фото (Solidworks PDM Server ~~и SolidNetWork License Manager~~ <mark style="color:red;">**License Manager НЕ УСТАНАВЛИВАЕМ!!!**</mark>):



Жмем кнопку далее.

Теперь переходим к настройке необходимых инструментов.

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-04 215903.png" alt="" width="375"><figcaption></figcaption></figure>

Выбираем пункт "Solidworks PDM Server" и напротив него жмем кнопку "Изменить"

Ставим пункты также, как на фото:

















