---
description: Инструкция по установке и настройке клиента
---

# 🧔‍♂️ SW PDM Client

Отключаем интернет.

Переходим в корень диска C и удаляем следующие папки:

```
C:\Program Files\SOLIDWORKS Corp\SOLIDWORKS PDM
C:\Program Files (x86)\SOLIDWORKS PDM
```

Запускаем установочник Solidworks 2021.

Выбираем пункт "Установить компоненты сервера", далее "Установить компоненты Solidworks PDM Server"

{% hint style="info" %}
Внимание! Автоматически установиться галочка на "SolidNetWork License Manager! Её нужно будет снять!
{% endhint %}

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-04 215843 (1).png" alt="" width="375"><figcaption></figcaption></figure>

Жмём "Далее".

Нажимаем кнопку "Изменить" напротив пункта "Solidworks PDM Server" и в появившемся окне выбираем "PDM Professional", проверяем путь установки "C:\Program Files\SOLIDWORKS Corp\SOLIDWORKS PDM" и ставим галочки напротив пункта "Клиент".

Жмём "Вернуться к сводке".

Жмём "Установить".

После установки подключаем интернет.

Открываем приложение "Администрирование"

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-04 222856.png" alt="" width="375"><figcaption></figcaption></figure>

Жмём правой кнопкой мыши на пункт "Администрация SOLIDWORKS PDM" и выбираем "Добавить сервер".

{% hint style="warning" %}
**ВНИМАНИЕ!**

**На сервере должен быть отключен брандмауэр, в ином случае подключиться не получиться!**
{% endhint %}

<figure><img src="../../../.gitbook/assets/изображение (277).png" alt="" width="375"><figcaption></figcaption></figure>

В появившемся окне прописываем имя сервера (например, DESKTOP-GGGFIB1), порт не меняем:

<figure><img src="../../../.gitbook/assets/изображение (278).png" alt=""><figcaption></figcaption></figure>

Далее в окне авторизации прописывем логин и пароль аккаунта, который настроен на сервере и от его имени запущен сервер PDM.

Далее жмём правой кнопкой мыши на появившийся в списке сервер

Выбираем пункт "Создать локальный вид...".

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-06-04 223954.png" alt="" width="282"><figcaption></figcaption></figure>

Откроется проводник и нужно будет выбрать место, куда будут сохраняться локальные копии с сервера.





