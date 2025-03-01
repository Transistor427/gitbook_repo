---
description: Форматирование носителя, на который будет сохраняться образ
---

# ⚙️ Форматирование носителя

{% hint style="danger" %}
Носитель должен быть отформатирован в EXT4
{% endhint %}

Запускаем компьютер или одноплатный компьютер с ОС Linux.

Вставляем носитель в USB разъём компьютера или одноплатного компьютера.

Проверяем, обнаружена ли наш носитель командой:

```
lsblk -f
```

<figure><img src="https://lh4.googleusercontent.com/KxSKmdIGOQlGaOlmjZkVlKo-cEY0056-cphNjjTKWs8S7rrn9qchsMEiQ9tSoZfKibQNtN5xQujKDdwj7_s2QdhffTpoL1ZYNq7Xs24hUT01T76T1V05qnp0KEvVAbMwOmCDgO9V0VLSlfZqLjfTQTU" alt=""><figcaption><p>Носитель определиться под названием SDB1</p></figcaption></figure>

Далее форматируем носитель командой:

```
sudo mkfs -t ext4 /dev/sdb1
```

Проверяем, отформатировался ли носитель командой:

```
lsblk -f
```

<figure><img src="https://lh3.googleusercontent.com/PQ0yMgcjG1iktWUcW1muvQr6ahYmo8kyP4KJQO_1VazJ7SAETuaFa7Y1giGejRVrPapnjW74qv4Jmk1jahBsybWFC7WQ_PV1DvhuQyoO8pSR3Nmf9yXJ1GxrO0kSFVphhL0BW9sKoFkbbbzXEhXyAH0" alt=""><figcaption><p>Теперь носитель имеет расширение EXT4</p></figcaption></figure>
