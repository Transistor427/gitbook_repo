---
description: Инструкция по решению проблемы с ошибкой при обновлении системы
---

# 🔼 Ошибка при обновлении системы

Подключитесь к принтеру по SSH.

Откройте файл с репозиториями командой:

<pre><code><strong>sudo nano /etc/apt/sources.list
</strong></code></pre>

Закомментируйте строчку "deb http://httpredir.debian.org/debian buster-backports main contrib non-free" добавив символ "#" в начале строки (без кавычек).

<figure><img src="../.gitbook/assets/изображение (14).png" alt=""><figcaption></figcaption></figure>

Сохраните и выйдите из редактора файла:

```
Ctrl+S, Ctrl+X
```

Перезагрузите принтер командой:

```
sudo reboot
```

После перезагрузки снова запустите обновление системы.
