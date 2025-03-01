---
description: Инструкция по установке и запуску базы катушек
---

# 🧵 Spoolman

{% hint style="warning" %}
Перед началом работы необходимо обновить весь программный пакет принтера до актуальной версии.
{% endhint %}

## 01. Установка

Подключаемся к принтеру по SSH.

Устанавливаем Spoolman (копируем все):

{% code overflow="wrap" fullWidth="true" %}
```bash
sudo apt-get update && \
sudo apt-get install -y curl jq && \
mkdir -p ./Spoolman && \
source_url=$(curl -s https://api.github.com/repos/Donkie/Spoolman/releases/latest | jq -r '.assets[] | select(.name == "spoolman.zip").browser_download_url') && \
curl -sSL $source_url -o temp.zip && unzip temp.zip -d ./Spoolman && rm temp.zip && \
cd ./Spoolman && \
bash ./scripts/install.sh
```
{% endcode %}

Заходим в веб-интерфейс в вкладку "Конфигурация".

Открываем файл moonraker.conf и вставляем в конец следующий код:

```django
[spoolman]
server: http://192.168.31.179:7912
#   URL адрес сервера Spoolman (указать IP-адрес принтера или сервера)
sync_rate: 5
#   Интервал синхронизации с сервером
```

```
[update_manager client Spoolman]
type: git_repo
path: ~/Spoolman
origin: https://github.com/Donkie/Spoolman.git
managed_services: Spoolman
install_script: scripts/install_debian.sh
```

Далее редактируем файл moonraker:

```bash
sudo nano /home/rock/printer_data/moonraker.asvc
```

Добавляем в него строчку Spoolman, сохраняем и выходим (Ctrl+S, Ctrl+X).

Сохраняем и перезагружам принтер.

Если настроен адрес сервера с настроенной базой филамента, то ничего больше делать не нужно. Если указан адрес принтера с пустой базой, то переходим к следующему пункту.

## 02. Настройка Spoolman

Переходим по адресу, указанному в прошлом пункте.

Создаем производителя.

Далее создаем филамент.

После чего создаем катушку от производителя с филаментом.

В итоге в флюиде появится такое окошко:

<figure><img src="../../.gitbook/assets/изображение (220).png" alt=""><figcaption></figcaption></figure>
