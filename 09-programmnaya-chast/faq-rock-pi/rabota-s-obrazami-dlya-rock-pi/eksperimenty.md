# 🕹️ Эксперименты



## Запись на EMMC из архивированного образа:

{% embed url="https://github.com/Transistor427/rpi_flash_image" %}
Ветка zip создана для автопрошивки из архива
{% endembed %}

```bash
unzip -p /home/rock/image.zip | sudo dd of=/dev/mmcblk1 bs=8M status=progress
```





## ~~Снятие образа со сжатием~~

Устанавливаем ddrescue:

```bash
sudo apt-get install gddrescue
```

Создаем sparce файл:

{% hint style="info" %}
Sparce файл - это файл, заполненый бинарными нулями. Он нужен для того, чтобы при снятии и сжатии образа пустое пространство не использовалось и образ был размером с саму систему.
{% endhint %}

```bash
cat /dev/zero > zerofile
```

Снимаем образ с карточки или системы:

```bash
sudo ddrescue -S -b8M /dev/mmcblk1 ./image_S300_14112023.img
```

Ожидаем окончания клонирования.





<div><figure><img src="../../../.gitbook/assets/Снимок экрана 2024-09-27 154118.png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/Снимок экрана 2024-09-27 160919.png" alt=""><figcaption></figcaption></figure></div>
