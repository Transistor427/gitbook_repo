---
description: Инструкция по созданию новых версий Fluidd
---

# Выпуск обновлений Fluidd

Fluidd - веб-интерфейс принтера. В отличие от klipper, moonraker, KlipperScreen и т.д, которые обновляются напрямую из репозиториев Github, Fluidd в свою очередь одновляется через релизы.

<figure><img src="../../../.gitbook/assets/изображение (307).png" alt=""><figcaption></figcaption></figure>

Для того, чтобы Fluidd обновился, необходимо, чтобы в релизе был архив fluidd.zip.

Содержимое архива представлено ниже:

<figure><img src="../../../.gitbook/assets/изображение (308).png" alt=""><figcaption></figcaption></figure>

Чтобы выпускать "новые" версии Fluidd, необходимо в файлах release\_info.json и .version менять значение версий в соответствии с тегами и релизами (v1.30.3, v1.30.4, v1.30.5 и т.д.)

<figure><img src="../../../.gitbook/assets/изображение (309).png" alt=""><figcaption><p>Содержимое файл .version</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/изображение (310).png" alt=""><figcaption><p>Содержимое файл release_info.json</p></figcaption></figure>

{% hint style="danger" %}
**ВАЖНО! Чтобы корректно создать архив для обновления, эти файлы нужно сначала извлечь из архива, внести изменения, после чего копировать с заменой обратно в архив!**
{% endhint %}

## СОЗДАНИЕ НОВОГО РЕЛИЗА

1. Переходим на Github в репозиторий Fluidd и открываем раздел Releases:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-09-14 150239.png" alt=""><figcaption></figcaption></figure>

2. Далее нажимаем кнопку "Draft a new release" , чтобы создать новый релиз:

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-09-14 150033 (1).png" alt=""><figcaption></figcaption></figure>

3. В открывшемся окне нажимаем кнопку "Choose a tag" и в поле вписываем новый тег, соответствующий версии релиза (был v1.30.3, стал v1.30.4) и нажимаем "Create new tag: v1.30.4 on publish"

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-09-14 150046.png" alt=""><figcaption></figcaption></figure>

4. Далее вводим название релиза (1) в соответствии с тегом. Переносим архив с измененными файлами в область (2). Когда все готово, нажимаем кнопку (3) "Publish release".&#x20;

<figure><img src="../../../.gitbook/assets/Снимок экрана 2024-09-14 150114 (1).png" alt=""><figcaption></figcaption></figure>

**Готово. Новый релиз создан.**
