---
description: Инструкция по сборке и настройке принтера с механизмом смены голов
---

# ⚒️ Сборка модулей и юнитов

## Сборка каретки

<figure><img src="https://lh3.googleusercontent.com/KNs7VT2CWpZ3djgWin86HP3mtdx4y3KkcjmASuHdilrn2s3apcuc6iVb40IpI_8RqHJXd7PymUnQAiKg6vfIP863Hl9ZgqauCL5jnGuLe_V1ffi1c0bznmNZkgzVco7KB-FO8O_SS64IJGd-_xI3soE" alt="" width="375"><figcaption></figcaption></figure>

#### 01. Каркас

1. Запрессовываем резьбовые заклепки.

<figure><img src="https://lh5.googleusercontent.com/iTI27cFFnbBsbX406tC-8PcfLjKCiT0pd_wY6OB-PxBsviFgRTs35ntXeVYdF75HKRknJVUMz2UTtOkkojlZHMzyiAee2F0HFx164bYjiYwuoi3IMvyRT3F9SY2Q5TzIXmR4V6Z4slJXsanEyVtO6WM" alt="" width="375"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/изображение (169).png" alt=""><figcaption></figcaption></figure>

2. Нарезаем резьбу М2.5:

<figure><img src="../../../.gitbook/assets/изображение (175).png" alt=""><figcaption></figcaption></figure>

3. Нарезаем резьбу М3:

<figure><img src="../../../.gitbook/assets/изображение (171).png" alt=""><figcaption></figcaption></figure>

4. Зенкуем отверстия под М2.5 потай:

<figure><img src="../../../.gitbook/assets/изображение (172).png" alt="" width="199"><figcaption></figcaption></figure>

5. Собираем каркас согласно картинкам ниже:

* боковины сверху М2.5х6 DIN912
* боковины снизу М2.5х8 потай
* Рельса MGN9-40mm - М3х10 DIN912, гайка самоконтр. (есть печатный кондуктор для ровной установки рельсы, ищите в коробке со всем дуаловским барахлом)
* стойки 20мм - М3х8 ISO 7380 + фиксатор резьбы
* деталь крепления рельсы (серединка) ставится более толстыми плечами вверх

{% hint style="danger" %}
Если детали каркаса крашеные, то необходимо в месте, где кайка рельсы касается каркаса, зачистить краску, иначе автоуровень может работать некорректно!
{% endhint %}

<figure><img src="../../../.gitbook/assets/изображение (173).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/изображение (174).png" alt=""><figcaption></figcaption></figure>

#### 02. Держатель печатных голов

<figure><img src="https://lh6.googleusercontent.com/OcGXlfcUNZ8cotu8SsKGe5M3NNCeLMyKXZLAWPKmI6NzvE9gr1dBYNzyMqWKpxarCSXtMM5mEu8JM4sGm5D9vSZ_XMaFCuZImKx9yXUcy6H1dOOj3pC5JDOezdutQpT1u1E34yFKdbArxOTP0erXyDk" alt="" width="375"><figcaption></figcaption></figure>

1. Зенковка М3 (для педантов Ø6.8).
2. Резьба М3. В резьбу сверху закручиваем М3х6 din 912 (на рисунке не показано).

{% hint style="info" %}
Если резьба под магнитом сорвется - можно запрессовать латунную гайку.
{% endhint %}

3. Запрессовываем пиптыки.

{% hint style="info" %}
Если отверстий нет - сверлим сверлом Ø1.9мм на расстоянии 22мм друг от друга симметрично относительно центра. Пиптыки кладем шляпкой на стол и молотком заминаем его ножку. После чего&#x20;
{% endhint %}

3. Запрессовываем подпружиненные шарики.

{% hint style="info" %}
Если шарики выпадают, то садим на суперклей.
{% endhint %}

5. Запрессовываем рога.

{% hint style="info" %}
Если болтаются, можно аккуратно въе..ать сзади керном по линии прилегания вала и алюминия.

Если не лезут совсем, можно развернуть отверстия разверткой 6мм на ⅘ длины, а в оставшиеся \~5мм допрессовать.
{% endhint %}

#### Подготовка магнита:

<figure><img src="https://lh3.googleusercontent.com/Ik3npTx33ougwZLKQxrtRu5Z2meec1t4vkh6ELb78UfswKWkbPAWnzSqK488fKoZV9LqCcni0H1yFls2oFz5k0L90wamYi-Qr27DflhJqaPcCsczK2WQ0udozROZKytKBx8GxbTGvgp73pUof9cbRDg" alt="" width="375"><figcaption></figcaption></figure>

1. Зенковка М3 (для педантов Ø6.8)
2. Делаем кастомный винт М3 потай 13.5-14мм (главное чтобы при закрученном магните не торчал за плоскость держателя печатных голов)
3. Провода (90мм) обжимаем в XH2.54 2pin, полярность не важна.

#### 03. Подготовка печатных плат <a href="#docs-internal-guid-749e46f5-7fff-6f41-5d55-65a38d2df4b1" id="docs-internal-guid-749e46f5-7fff-6f41-5d55-65a38d2df4b1"></a>

В плате коммутации нагреваем феном и выпаиваем разъем хотэнда (или не запаиваем изначально, если паяем самостоятельно). На его место с внутренней стороны к контактным площадкам нагревателя планарно припаиваем угловой XH2.54. Должно получиться так:

![](https://lh5.googleusercontent.com/2zqbzGpzRE5ttkYOkHNdLpW_2LO_LVvwZY1yMtDG8YHOY_KnkoixE-aslD1hbQyibT0di4ktofv31ikPvuqUEccIYx8isvLkmx7t_8gW9aaBX6I2B45XczHBqX0k20wC3EDII3bcneW5_vGPRYAAuAM) ![](https://lh5.googleusercontent.com/77WvJjQ5puIubvBtTggVPXShemccikARVqF5SC5IY3C9CH77dMZfGjV8a4LnNY6YRGlvpgnap5DP4qP21OHM2h2k-Cbrv--p8XSx34fuagA85pjBh37-Q1FFqkq9n9pkGNWXZHHm0zdXQfee9b7OhuI)

В плате автоуровня вместо разъема припаиваем провода от двигателей экструдера или от вентиляторов длиной 5 см и обжимаем в XH2.54:

<figure><img src="https://lh3.googleusercontent.com/ksllOD8-d64tzrBInLMHXEejwEk9zmqjX3iNA_DVunGoCeOiyLIq5EekbUfBq8Ge66e-Wt68ZLf-y9lcATifzuMjIlO63kpj90OQ3sXPJ49yOyAB2fzfMMSyjWp-huh1Tdpox7LEB85S0Ds3eQpZyPw" alt="" width="375"><figcaption></figcaption></figure>

#### 04. Сборка каретки

<figure><img src="https://lh4.googleusercontent.com/aUP4Jz3KghAd5_XLDr1xygit4SwKmYLcpJvNyEqpuOfmMYiW_soom87OxNXBsvUzTkdRv9ryZn57AT4TmT7aPD5YzGKaUxwtJ-qPqKeubOk9I82NkgTS9J4ey3HPeGsqu7QzvDOqxifx24ZogT1JSjo" alt="" width="375"><figcaption></figcaption></figure>

1. Одеваем каретку MGN9H на рельсу, затем через печатную проставку крепим плату автоуровня - М3х10 ISO 7380

<figure><img src="https://lh6.googleusercontent.com/BtA_gERaRptysq4V6lUX_dwaPyT808cPHKnP-hCPwvOKFhnVbYSHED4zItk6LKQ9ZQXXe1PHFib2JxdG88drELjD21xKriY5neY_bETaAne1fbF1ay7nQ4gH_VmtH3bTp4LF4LJ-L4won48UELoxNCQ" alt="" width="375"><figcaption></figcaption></figure>

2. Крепим держатель ПГ - М3х6 iso 7991 - 4шт и магнит - М3х13.5 iso 7991 (кастомный)

{% hint style="warning" %}
При установке магнита необходимо смазать термопастой место соприкосновения магнита и алюминиевой детали!
{% endhint %}

<figure><img src="https://lh3.googleusercontent.com/zuHJnAiGKKYS5SIs9myK59AQJMtQ6qUhLhSyq18mtTiQMC204i3KsKlgewkDJyH2aJHBTM6gIsb7pIpvcG1XcNFyMVvihj3AaI9kwZA7OwrrSmPANpqbagFrQcFNUTz_qGp7pEJdzTgHLSw3YFcvMn0" alt="" width="375"><figcaption></figcaption></figure>

<figure><img src="https://lh4.googleusercontent.com/kOKgL2qbKEzSdkwtlDQVc7hoRCnB9E9X-d0CwLgSlv1Xa0zCBO6lmrSfcg50BKG3gMXP2cwlNf4l3fvHpZR147BtQauFYzf-1nIuSWAnOGZA-2Qg-SqNoY0LOg2Ef4kEJi0nVq7MlgWbB4IS_bE-6Gw" alt="" width="375"><figcaption></figcaption></figure>

3. Устанавливаем пружинку Ø7\*0.6\*14мм (та же, что используется на парковке).
4. Вставляем разъемы с внутренней стороны платы (автоуровень в автоуровень и магнит в припаяный на место хотэнда угловой XH2.54), крепим плату на 4 винта М3х6 ISO 7380

&#x20;&#x20;

<figure><img src="https://lh5.googleusercontent.com/hwSycIIwBdd4_g8TegEzJUvWptXg1f-Pkm2Cv_8ITuDsgsc8IpcdZkMhn6avCN7QWTbpvOWENUetbYK5oyntpB9i8e-OWTcSrGxiRAFLvW6teqT9yxpb76Cmu0OdIhC_1ix4FXJE9Hh8xip480GgNzk" alt="" width="375"><figcaption></figcaption></figure>

5. Ставим вентиляторы обдува (провода сначала надо обрезать и обжать - 5 см) - М3х18 ISO 7380 - 4шт. (для винтов, которые ближе к пружине нужно поставить шайбы М3, чтобы винты не упирались в держатель)

* сам печатный обдув - М2.5х8 ISO 7380 - 2шт.

## Сборка печатной головы

{% hint style="info" %}
[ссылка на 3д-моде](https://drive.google.com/file/d/1tqiw7Klzf4yO5_oGO0vzYZ5wwTToEhN7/view?usp=share_link)ль
{% endhint %}

#### 01. Радиатор

1. Запрессовываем втулки (после запрессовки необходимо рассверлить втулки сверлом 6,1 мм и проверяем его на держателе головы).
2. Нарезаем резьбу М3. Помимо того, что показано еще 2 спереди (крепление вентилятора), 1 сбоку (под винт-фиксатор хотэнда) и 1 сзади под крепление блина.
3. Зенковка М3 (для педантов Ø6.8), так чтобы потайной винт был ниже уровня блина.
4. Сначала проходим сверлом Ø2.5, потом нарезаем резьбу М3, затем аккуратно в несколько заходов зенкуем зенкером Ø6.8 до диаметра 3.8-4.0мм. Нужно понимать, что здесь мы не зенкуем коническое отверстие под винт потай, а формируем кромку прилегания для подпружиненного шарика диаметром около 5мм и если перестараться, шарик будет утопать в вашей зенковке не подпружинивая, и голова будет плохо центроваться на каретке.&#x20;
5. Блин слегка шлифуем мелкой наждачкой и крепим винтом М3х6 ISO 7991.

<div data-full-width="true"><figure><img src="https://lh5.googleusercontent.com/q-MQfFY8y-d9auvpdWwr0bnoh996br0iNjKNfBWatwOyimO5elVoFhOqkfwiAnJ0vA525Sv7pUaoyyIFbiJyyLplu3ukATJgCTjG0GJmHjCox_5CYlvrCGL7VimxCjm0oEiuHF3foEmKeaXYapyd0Ls" alt="" width="375"><figcaption></figcaption></figure></div>

#### 02. Печатное основание

Помимо удаления поддержек и всяких дефектов-артефактов:

1. Запрессовываем гайки М3.
2. Запрессовываем хитрые латунные гайки М3 (как в экструдере).
3. Проходимся разверткой 7мм.
4. Запрессовываем цилиндрические магниты 5х5 мм (правильной стороной, чтобы работали датчики Холла!!!!)

{% hint style="info" %}
Берем эталонный датчик холла и проверяем стороны магнита.
{% endhint %}

<div align="center"><figure><img src="https://lh4.googleusercontent.com/DI16fxDh4XCeZXxb5aJA8AyqdzdQWkGsxirXI3Vpg2895kQsWZdT7v1aDTGsGzISSxWMsPSWNXkwJgNCGZ6c0q6_Iv-xk-dUPAUAawzpO1Vwx6HP3coOEkbWjDGezUb5BwUxevib6RUk5cX0dRM2mso" alt="" width="188"><figcaption></figcaption></figure></div>

<figure><img src="https://lh6.googleusercontent.com/rDFxN4bQ_QXSsmqea1bYviNsx5zO7qnh5YrFhgYcMtsUdG1AYu_jTAK8iQUQPZwzK1l8y4xturVTHs2O4KJ7OV-mwRWLzvvcZhA5p16UOZZcQn5wF6tngubD2Qdg540fRli_UMTHuMl67zTZuvnYL5A" alt="" width="188"><figcaption></figcaption></figure>

#### 03. Вентилятор радиатора&#x20;

Длина проводов вентилятора - 55 мм (обжимаем в xh2.54-2pin w-to-w МАМА).

Вставляем аккуратно его в печатную деталь и прокладываем его провода как на фото.

{% hint style="info" %}
Если разъем не очень плотно держится в печатной детали, можно капнуть чуть-чуть суперклея, но без фанатизма.
{% endhint %}

<figure><img src="https://lh5.googleusercontent.com/1SqFjLufMBI55nwaTfDcCt0nmG7OlMrATsfc3dj9zhY-8qvZtmhbsqDoUS0UppWVq0SPVafnD8bq2Ag4U9e5HwYpHirHUiBCD4SjGQHocMt_IPXLNbgKcdjvFm_kuae1McLgN8D97E4C3t8-iQqRXZc" alt="" width="188"><figcaption></figcaption></figure>

<figure><img src="https://lh5.googleusercontent.com/y-5OQE6hoZK8N8BepHWSqxe3D1zxXSTcBLqyk2pd6cQ1IYNDLBRC4GKSntbBZJ4xsgP5bQ_akgfnkVxpGWAX9Yfm_50DB0JqZ__hrKXqEWySIe7H72kClTo9PbQUKdi0wfYrmmfoRIF_aoeyo7TJNlw" alt="" width="188"><figcaption></figcaption></figure>

Рассверливаем отвертия в вентиляторе (веделены красным) сверлом 4 мм, после чего впаиваем туда латунные гайки

<figure><img src="../../../.gitbook/assets/DSC_0615 (1).JPG" alt="" width="375"><figcaption></figcaption></figure>

#### 03. Бутерброд

Собираем бутерброд из печатной детали, вентилятора и радиатора.&#x20;

Сверху - М3х10 ISO 7380

Спереди через магниты 12 мм с зенковкой:

* верхние - М3х20 ISO 7991
* нижние - М3х16 ISO 7991.

<figure><img src="../../../.gitbook/assets/изображение (176).png" alt="" width="353"><figcaption></figcaption></figure>

#### 04. Слюда

Сочиняем слюдяное пикассо.&#x20;

Слюда нужна в качестве изоляции между горячей частью снизу и холодной сверху, в радиаторе. В стандартной голове эту функцию по совместительству выполняет плата автоуровня, а здесь не выполняет. Слюду принято фрезеровать на фрезере и клеить к низу радиатора на тонкий слой высокотемпературного серого герметика. Технология фрезеровки слюды является тайным знанием и передается опытными джедаями юным подаванам из уст в уста.  Должно получиться примерно так:

<figure><img src="../../../.gitbook/assets/AF1QipO91c4knF1y68xcb_vLKWr0qS6NBOFchHbHJBCo=w2048-h1536.jpg" alt="" width="375"><figcaption></figcaption></figure>

#### 05. Хотенд

Из старой платы тензодатчика дремелем или болгаркой и сверлом 3мм колхозим плату хотэнда, припаиваем к ней [Клеммник разъемный KSE-15EDGVC-3.50-04P:](https://belchip.by/product/?selected_product=51366)

{% hint style="info" %}
Размер платы 8х21 мм
{% endhint %}

<figure><img src="../../../.gitbook/assets/изображение (183).png" alt=""><figcaption></figcaption></figure>

Собираем хотэнд по классической методике, провода не пока не обрезаем. Оголяем провода нагревателя, вставляем хотэнд в радиатор (термобарьер должен выступать из радиатора на 1,5-2 мм), фиксируем термобарьер в радиаторе (М3х25 DIN912), временно устанавливаем плату хотэнда без крышки (М3х6 ISO 7380).&#x20;

<figure><img src="../../../.gitbook/assets/AF1QipMZoODNGcmDZhVLhJKQkr7KGSnFDEmwWIsGZLXb=w1536-h2048.jpg" alt="" width="375"><figcaption></figcaption></figure>

{% hint style="warning" %}
Далее идет достаточно спорная операция с загибанием жесткой части проводов нагревателя. Временная мера, впоследствии от нее избавимся, но пока так.
{% endhint %}

Загибаем так, чтобы провода легли в паз печатной детали.

<figure><img src="https://lh3.googleusercontent.com/5U7rRGJZkiD9XdkB5dH2JdfO4n7gMocDF387aOBwFIBYsHi3VpwHvQITCGLx85uS_gaVe421xTp7G6KLyoTGEthZDQltTtMpuKiaoFH02Pvo_vLgxbX9pZKM9ICJmRUVmOJoVFcqIoBnoRhzIKv1oy4" alt="" width="375"><figcaption></figcaption></figure>

Провода нагревателя и PT1000 обрезаем, припаиваем к плате по месту. На провода нагревателя надеваем оплетку длиной 50 мм. Одеваем боковые крышки, фиксируем (M3x10 ISO 7380).

<figure><img src="https://lh6.googleusercontent.com/wT32pRZVhcsjtds5Sk1-11OBl4RRpdCz-3iTc3ZZNoXmE6Ep0H_fu1BIRJor37Q9I4QSUoDuk5ewPDV3_yPwRmSynrvSLT2lqj-PC7f83Mxa5c8AuZA27YyIpCbRXE-pQHezAi6uuxiF66rBhzGm2Pw" alt="" width="375"><figcaption></figcaption></figure>

## Сборка экструдера

{% hint style="info" %}
Экструдер собираем в конфигурации тулченджера.
{% endhint %}

* с кастомной передней деталькой (на картинке выделена синим), крепим на М3х25 ISO 7380;
* c доп. деталькой крепления косы ПГ (на картинке выделена синим);
* длина шлейфа двигателя - 80мм;&#x20;
* длина трубки экструдера - 77 мм.

<figure><img src="https://lh6.googleusercontent.com/xF5KStvHSRk2TlCXs0neSmBT9hLTyCrOc8MHdolRELbl0nNyyP0zZmEk9J49GrMMFIDlZ5vYiDsMLiYMxoq0hl0mbvW8WmiioCG8Hfwudh0gAqH7CiR-X3k_1RjJh0bNz4R6cApyncOcXrVaE_l8waY" alt="" width="188"><figcaption></figcaption></figure>

Распиновка двигателя:

<figure><img src="../../../.gitbook/assets/MMF 4 pin .jpg" alt="" width="355"><figcaption></figcaption></figure>

## Сборка парковочных мест

#### 01. Подготавливаем металлическую детальку:

1. Нарезаем резъбу M3 (иногда нужно заранее рассверлить отверстие сверлом 2.5 мм).
2. Рассверливаем отверстия сверлом 4.5 мм.
3. Шлифуем плоскость детальки с обеих сторон.

<figure><img src="https://lh6.googleusercontent.com/hbKriWhsV11-aBvqaI2vYdyDjMRXmqd4sctljNkJxGwSQrBpOdfKvnuP33QwVlMASPHVfWezU-q6RbcVOy9wg9u5T5kcGlegMbDChRKKST9qyG5W2KFSwOJeDm261bvj8mrpSNn7W0T-KqgOrqahIJo" alt="" width="375"><figcaption></figcaption></figure>

#### 02. Собираем держалку головы:

![](https://lh3.googleusercontent.com/VAerN_Q-C5XBeYVUVzxkJJoRJN6o3mDFpS8wTyMZ3qO3KdOA48c4hKTXlDniz-tm2t9CyPVR8F3ka8wCj8yUI_KCCkdY2CT1LwKGqUcB2jy2P3BOmNvAQqNniH9zfqOHaWVbtdX63Nt5T52L4mxPx70)   ![](https://lh5.googleusercontent.com/7CHiyBjqdY4YJ7GGzir4fJ0XQj16YhG63kEgpV3h4ZcKVR1NFwV3bxuTAHqGW24hem-RF9d8vkSiTYzDPAJlFOp6Tzrsej0Amw4Tf4zPXzxqmMO7vW52vR0BJLFDx2OrZGyNe7VtawRokTTyjNmb3_g)

1. Резьба М3
2. Резьба М2.5
3. М2.5x6 DIN 912
4. М3х30 ISO 7380
5. ~~М3х6 ISO 7991 и магнитики 12х2,5мм с зенковкой.~~ <mark style="color:red;">**Теперь не ставим!!!**</mark>
6. М3х8 ISO 7380

#### 03. Подготавливаем микроюнит датчика холла

{% hint style="danger" %}
**ВНИМАНИЕ!**

<mark style="color:red;">**ЕСЛИ ДАТЧИКИ ИЗ ПАРТИИ С ОЗОНА (3144 121Y) - ПЕРЕПАИВАЕМ САМ ДАТЧИК ХОЛЛА НА ПЛАТЕ НА ПРАВИЛЬНЫЙ (ЛЕЖАТ КУЧКОЙ В ОТДЕЛЬНОМ ПАКЕТИКЕ).**</mark>

Если перепаиваем дачик, то не ленимся, одеваем на ножки силиконовую изоляцию длиной 1 см от проводов кос ПГ.
{% endhint %}

&#x20;

<figure><img src="../../../.gitbook/assets/AF1QipNiyYLcTBbn0NUMysyUgJ99t3_uXnFl7tJVCBiK=w1536-h2048.jpg" alt="" width="297"><figcaption></figcaption></figure>

1. Выпаиваем разъем Dupont и с обратной стороны припаиваем XH2.54-3pin:&#x20;

<figure><img src="https://lh5.googleusercontent.com/2lyoUStAgTqy_lytg7seI3mPRt67AIuBGk5YH08sKaaa2f2rE9gimkdIc3x_fQHwelPu3O7HfO6zg6EmjervOrnVIr4B_CZ2jLEi-1gNteOltbPNPb-MAFdjGNgU4ff8yh1J7JROLEAxVBaxAHXApes" alt="" width="375"><figcaption></figcaption></figure>

2. Берем из запасов стандартный шлейф от концевика Y и меняем местами: черный с красным провода со стороны платы датчика и белый  с красным провода со стороны платы управления. Должно получиться как на фото.

<figure><img src="../../../.gitbook/assets/AF1QipPKw5KS4bqSC0h0rzzvfxHB67X5tF5u4t9DxNu_=w1536-h2048.jpg" alt="" width="375"><figcaption></figcaption></figure>

#### 04. Собираем микроюнит датчика холла:

1. Гайки М3 шестигранные - 2 шт.
2. Винт М2х8 потай - 2 шт.
3. Разъем XH2.54 3 pin - 1 шт.



<figure><img src="https://lh6.googleusercontent.com/mv4tR4Q0MfU-3WC9xtjY1j6UZgZcO8iVJm7jLN2Q06co_vc6sg71ys4l4h1KUSPtO0AQQWaUrVnYHNua_zVaJhVILh9CGJ0vRFhTT2TIDrEXuI7si7p-b9CT9DdX8eUHTZaQ6OE2Wzs5UUZENQh9uUk" alt="" width="375"><figcaption></figcaption></figure>

4. Герметизируем от греха всё, что теоретически может закоротиться:

<figure><img src="../../../.gitbook/assets/AF1QipPnrZ6YNQVfOWY2rZkL-D0S-Q9CKocqOsBkKf6A=w1536-h2048.jpg" alt="" width="375"><figcaption></figcaption></figure>

#### 05. Подготавливаем основание парковки

<figure><img src="https://lh4.googleusercontent.com/fjLr2B235PW5dTMkP1Lqbo4X730qkT9s7C3a6oaFU44HTjVwb_0yn3Gw95KJD9BxT35htJYj8pBS221_5uils9vWNdP8_FN8QJdixesH8GZfglYW-sMfFFC-526-N6UnQghhj298ykLITsaG84MfvfE" alt="" width="375"><figcaption></figcaption></figure>

1. Резьбовые заклепки М3 - 4 шт.
2. Резьбовые заклепки М4 - 2 шт.
3. Хитрые точеные детальки диаметром 6мм и резьбой М4 на фиксатор резьбы.

{% hint style="danger" %}
Так как хитрые точеные детали закончились и чтобы их не токарить, то берем штыртки от кареток. На токарнике с помощью специального центровочного сверла делаем отвертие в штырьке, после чего досверливаем в нем сверлом 2,5 мм отвертие на \~15 мм и нарезаем резьбу М3.

На парковку штырьки прикручиваем винтом М3х16 ISO 7991 с лицевой стороны парковки.

![](<../../../.gitbook/assets/DSC_0629 (1).JPG>)![](<../../../.gitbook/assets/DSC_0627 (2).JPG>)
{% endhint %}

{% hint style="danger" %}
Дополнительно.

Напротив боковых прорезей парковки сверлиться отверстие диаметром 5 мм.

Далее заклёпываем заклепку М3 с лицевой стороны.

![](../../../.gitbook/assets/DSC_0629_вф.JPG)
{% endhint %}

#### 06. Собираем парковочное место

| <ol><li>М3х8 ISO 7380</li><li>Пружинка  0.6x6x15 (берется в коробке с тулченджерным барахлом)</li><li>Плечевой винт 4x10 М3х6 (самая маленькая шляпка). Закручиваем до упора, но без фанатизма, садим на фиксатор резьбы</li></ol> | ![](https://lh6.googleusercontent.com/8GgE9FjFCh89Hn8yqHZvor_ZSoubT7bTDY0_d--0SFOGYhv0YDPQC7BfKpt_w5i4K51OmaeMmPPTZxCW3wKdQEQjZ82kY5R0l5QZ-duuH_-5Ae3DoZ30bSah0cqvgxg25MG1Y4AGqW01mz_Ml-53mew) |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

{% hint style="warning" %}
Есть нюанс - после сборки держалка должна свободно ходить по плечевым винтам при нажатиии и самостоятельно отпружинивать обратно при отпускании без всяких закусываний. Если этого не происходит, берем пассатижи и аккуратно подравниваем плечевые винты. Написано непонятно, так что спросите у Кузи, он шарит, как это делается))).
{% endhint %}

## Сборка кос печатных голов

#### **Пересборка кос из готовых**

Потрошим стандартную косу 1800мм для первой головы и длинную RnD косу 3000мм (обрезаем провода до 2100мм) для второй головы. На каждую голову надо 8 проводов 24AWG и по 2 провода 20AWG (таких у нас в косах нет, эти клянчим у Лифтера).&#x20;

Провода 20AWG (нагреватель хотэнда) обжимаем в черные НШВИ с обеих сторон:

<figure><img src="https://lh4.googleusercontent.com/byN6oQrXtrIz8V6vDlwBhrqsuw84c4JNV5twLgWQFw3jIJExLpegHZmmCWoxMfFOemmwTuSgOqOU06a8k1dxwZlyLoipxqIwThHoBU-XdiKRQCbaC1lu12MAn5zqnDyEHQrgwvVmeu4d1DihmCOPBj4" alt="" width="188"><figcaption></figcaption></figure>

Провода PT1000 c одной стороны белые НШВИ, с другой - xh2.54-2pin:

<figure><img src="https://lh5.googleusercontent.com/osYY2jwdL5c8GZLfA34v65FvGhiO7nftMPY6r6PgQVxtDxkMi-TIuyDXp1GCA2C_LnumdWxJls5jdV0auzmczqJa7gg9U1UN2DZrSm3TMpNfnEreGbPSLGcGWZcjh0xEQzOB2Lmx4cLULFVQTA3JAS8" alt="" width="188"><figcaption></figcaption></figure>

Провода вентилятора - xh2.54-2pin - xh2.54-2pin ЗЕРКАЛЬНО:

<figure><img src="../../../.gitbook/assets/изображение (178).png" alt=""><figcaption></figcaption></figure>

Провода двигателя экструдера xh2.54-4pin -  xh2.54-4pin wire-to-wire:

<figure><img src="https://lh6.googleusercontent.com/QG-WqnhPKuGxj8G9nEWwXqL-dcUnRG6PBiN6Xq6w7h-v5QCvmmXh4UWKrH5n5Btfnm9v_sxnB_TbqGe1lQsgevPu1ijycUEMcjmDQIfqFuIDz-qK2Vhdzdw_vxZm76eu_sztPGIKufJ_Fbw3dpqAAPo" alt="" width="188"><figcaption></figcaption></figure>

НШВИ с одной из сторон вставляем в разъем 15EDGK-3.5-04P-14-00AH:

<figure><img src="https://lh5.googleusercontent.com/pEoOFmzgIj6DutDyBJuKt3VtwlwHoxJUHC7a08zWSA37lQy5Fxxv9HHpnTKJQOodmcVnrggMSEf8vBXM2bUKdxY4IDM-ssAjl9369Iyk66cfl5FL9kbF-PkfZnRvnhMGctuhVp14Zc6vFraYuMZyU4c" alt="" width="188"><figcaption></figcaption></figure>

Одеваем пластиковую оплетку-самозаворачивалку 4мм длиной 100-110мм на провода вентилятора (xh2.54 c обеих сторон) и тканую оплетку-самозаворачивалку диаметром 10мм и длиной 1400мм на всю косу. С обратной стороны стяжку, чтобы оплетка не елозила туда-сюда. Должно получиться примерно так:

<figure><img src="https://lh3.googleusercontent.com/k0_BSG3bpWG87k66uRdDLpt71CQ6M1tRgjpAX_AcAD3wCnsYYx1uNJwGYQ0TMgXDFSEAh9Hw9AaINcRO7RtkzVCXUSU0h7ODAngoRAZU3fWH2PQzW023gM1SrWEjdAYKcpU75nsUfNvsmtTA3tJePns" alt="" width="188"><figcaption></figcaption></figure>

Одеваем поверх оплетки печатную детальку - держатель косы (она из гибкого материала, можно её раздвинуть пальчиками или плоскогубцами, например):

<figure><img src="https://lh5.googleusercontent.com/nVpIHsU5WVpUNeZ0L-BWsaw5d1yhBSsbh-9lDFpg6TZox1qcUKnG-8Sf7wuIKlbUzZEwPixn_FJ8w2thQLPLt6detHxUO8X9nxVEOzu3SplFZNsHIrSueOdJ-Ps4EEs_wEscT_RsdK2TlT_ITunnxnA" alt="" width="188"><figcaption></figcaption></figure>

Вставляем всё в свои разъемы, укладываем, как показано на картинках, прикручиваем печатную детальку к экструдеру, фиксируем разъем экструдера стяжкой:

![](https://lh4.googleusercontent.com/UME7RBTyPUVrT_wktPkFjn5KmH1Fon63k7Q26vkG_l1b8BVYCxCnaZbCSE8A8Wi8z_9qsAKiftlRAButBq-01p_hd_L1Wi0JQYkOTa-loAxPZVKi0DsQEtUbywBiTxLdJuqeRDu-Ye7FXa2u_pSv6Mo)    ![](https://lh6.googleusercontent.com/ouDjtGVLs-HHHbm0uXCIK3OkHdcKlB86IofcVOKN91eeclvS8u6V-g2D-Sxo7YDSCHRUe0vk4un7ozP9n1erhY-hnLmZkIavMXVSgPRAf58B1O9x1CAzHN7HmApCAiKTvVt6H1kl5r_QTo6Xyi9aBTE)

#### Сборка кос с нуля

Провода 20AWG (нагреватель хотэнда) обжимаем в черные НШВИ с обеих сторон:

{% hint style="info" %}
Длина:

для левой косы - 1800 мм

для правой косы - 2100 мм
{% endhint %}

<figure><img src="../../../.gitbook/assets/AF1QipPdn1XlrXv41J3bAzY3SgyotcdbixN9czduqf8a=w1536-h2048.jpg" alt="" width="188"><figcaption></figcaption></figure>

Провода 24AWG PT1000 c одной стороны белые НШВИ, с другой - xh2.54-2pin:

{% hint style="info" %}
Длина:

для левой косы - 1800 мм

для правой косы - 2100 мм
{% endhint %}

<figure><img src="https://lh5.googleusercontent.com/osYY2jwdL5c8GZLfA34v65FvGhiO7nftMPY6r6PgQVxtDxkMi-TIuyDXp1GCA2C_LnumdWxJls5jdV0auzmczqJa7gg9U1UN2DZrSm3TMpNfnEreGbPSLGcGWZcjh0xEQzOB2Lmx4cLULFVQTA3JAS8" alt="" width="188"><figcaption></figcaption></figure>

Провода вентилятора - xh2.54-2pin - xh2.54-2pin ЗЕРКАЛЬНО:

{% hint style="info" %}
Длина:

для левой косы - 1800 мм

для правой косы - 2100 мм
{% endhint %}

<figure><img src="../../../.gitbook/assets/изображение (178).png" alt="" width="164"><figcaption></figcaption></figure>

Провода двигателя экструдера xh2.54-4pin - xh2.54-4pin wire-to-wire:

{% hint style="info" %}
Длина:

для левой косы - 1800 мм

для правой косы - 2100 мм
{% endhint %}

<figure><img src="https://lh6.googleusercontent.com/QG-WqnhPKuGxj8G9nEWwXqL-dcUnRG6PBiN6Xq6w7h-v5QCvmmXh4UWKrH5n5Btfnm9v_sxnB_TbqGe1lQsgevPu1ijycUEMcjmDQIfqFuIDz-qK2Vhdzdw_vxZm76eu_sztPGIKufJ_Fbw3dpqAAPo" alt="" width="188"><figcaption></figcaption></figure>

НШВИ нагревателя и термистора с одной из сторон вставляем в разъем 15EDGK-3.5-04P-14-00AH:

{% hint style="info" %}
Слева - термистор

Справа - нагреватель
{% endhint %}

<figure><img src="https://lh5.googleusercontent.com/pEoOFmzgIj6DutDyBJuKt3VtwlwHoxJUHC7a08zWSA37lQy5Fxxv9HHpnTKJQOodmcVnrggMSEf8vBXM2bUKdxY4IDM-ssAjl9369Iyk66cfl5FL9kbF-PkfZnRvnhMGctuhVp14Zc6vFraYuMZyU4c" alt="" width="188"><figcaption></figcaption></figure>

Одеваем пластиковую оплетку-самозаворачивалку 4мм длиной 100-110мм на провода вентилятора (xh2.54 c обеих сторон) и тканую оплетку-самозаворачивалку диаметром 10мм и длиной 1400мм на всю косу. С обратной стороны фиксируем стяжкой. Должно получиться примерно так:

<figure><img src="https://lh3.googleusercontent.com/k0_BSG3bpWG87k66uRdDLpt71CQ6M1tRgjpAX_AcAD3wCnsYYx1uNJwGYQ0TMgXDFSEAh9Hw9AaINcRO7RtkzVCXUSU0h7ODAngoRAZU3fWH2PQzW023gM1SrWEjdAYKcpU75nsUfNvsmtTA3tJePns" alt="" width="188"><figcaption></figcaption></figure>

Одеваем поверх оплетки печатную детальку-держатель косы (она из гибкого материала, можно её раздвинуть пальчиками или плоскогубцами, например):

<figure><img src="https://lh5.googleusercontent.com/nVpIHsU5WVpUNeZ0L-BWsaw5d1yhBSsbh-9lDFpg6TZox1qcUKnG-8Sf7wuIKlbUzZEwPixn_FJ8w2thQLPLt6detHxUO8X9nxVEOzu3SplFZNsHIrSueOdJ-Ps4EEs_wEscT_RsdK2TlT_ITunnxnA" alt="" width="188"><figcaption></figcaption></figure>

Вставляем всё в свои разъемы, укладываем, как показано на картинках, прикручиваем печатную детальку к экструдеру **(М3х25 ISO 7380)**, фиксируем разъем экструдера стяжкой:

&#x20;  &#x20;

<figure><img src="https://lh4.googleusercontent.com/UME7RBTyPUVrT_wktPkFjn5KmH1Fon63k7Q26vkG_l1b8BVYCxCnaZbCSE8A8Wi8z_9qsAKiftlRAButBq-01p_hd_L1Wi0JQYkOTa-loAxPZVKi0DsQEtUbywBiTxLdJuqeRDu-Ye7FXa2u_pSv6Mo" alt="" width="375"><figcaption></figcaption></figure>

<figure><img src="https://lh6.googleusercontent.com/ouDjtGVLs-HHHbm0uXCIK3OkHdcKlB86IofcVOKN91eeclvS8u6V-g2D-Sxo7YDSCHRUe0vk4un7ozP9n1erhY-hnLmZkIavMXVSgPRAf58B1O9x1CAzHN7HmApCAiKTvVt6H1kl5r_QTo6Xyi9aBTE" alt="" width="375"><figcaption></figcaption></figure>

## Сборка дополнительного держателя катушки

#### Подготавливаем печатную деталь.



#### Обрезаем резьбовую шпильку М8 длиной 110 мм

#### Запрессовываем 2 квадратные гайки М3.

#### Собираем дополнительный держатель:

* берем 2 гайки М8, 3 подшипника 608ZZ, резьбовую шпильку
* устанавливаем гайку М8 на штатное место
* в штатные прорези устанавливаем подшипники
* закручиваем шпильку в первую гайку, не забываем про подшипники
* продев шпильку через все подшипники
* устанавливаем вторую гайку М8
* садим резьбу на фиксатор резьбы
* закручиваем шпильку во вторую гайку М8

## Установка собранных модулей и юнитов / Изменения в сборке модулей и юнитов

#### 01. Корпус

Заклёпываем резьбовые заклепки М3 крепления парковочных мест.

<figure><img src="../../../.gitbook/assets/изображение (180).png" alt="" width="180"><figcaption></figcaption></figure>

**НЕзаклепываем** резьбовые заклепки М3 крепления накладки задней стенки.

<figure><img src="../../../.gitbook/assets/изображение (181).png" alt="" width="180"><figcaption></figcaption></figure>

Рассверливаем отверстия крепления 2-го датчика филамента сверлом 5мм и заклёпываем резьбовые заклепки М3 **СНАРУЖИ**

<figure><img src="../../../.gitbook/assets/изображение (182).png" alt="" width="180"><figcaption></figcaption></figure>

#### 02. Кинематика

* меняем лапку концевика X на специальную для DUAL
* лапку концевика Y переставляем назад
* слегонца болгарим портал слева, чтобы первая голова становилась на парковку

#### 03. Электронный блок

* меняем/устанавливаем БП в эл.блоке на 200W

#### 04. Стол

{% tabs %}
{% tab title="Стол с PEI" %}
Меняем/устанавливаем алюминиевое основание стола на специальное с выборками под парковочные места.

Красиво болгарим переднюю декоративную накладку под всё те же клапана парковочных мест
{% endtab %}

{% tab title="Стол со стеклом" %}
Кладем специальное стекло для Dual с вырезами под парковки.
{% endtab %}
{% endtabs %}

#### 05. Экструдер

Смотреть пункт [**Сборка экструдера**](sborka-modulei-i-yunitov.md#sborka-ekstrudera)**.**

#### 06. Печатная голова

Смотреть пункт [**Сборка Печатной головы**](sborka-modulei-i-yunitov.md#sborka-pechatnoi-golovy-ssylka-na-3d-model)**.**

#### 07. Сборка.

Юнит задней стенки (ЮЗС) собираем в конфигурации DUAL с доп. трубкой-каналом справа

Ставим дополнительный датчик филамента c фитингом, проводим его шлейф через ЮЗС в правый тоннель.

Концевик Y перемещаем/устанавливаем сзади. Мелкую детальку-фиксатор проводов можно слегка чикнуть ножичком, чтобы 3х-проводной шлейф концевика в неё хорошо ложился

<figure><img src="../../../.gitbook/assets/DSC_0636 (1).JPG" alt="" width="375"><figcaption><p>Фиксатор проводов концевика Y</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/DSC_0637 (1).JPG" alt="" width="375"><figcaption><p>Концевик Y после модификации</p></figcaption></figure>

Лапку концевика Y подгибаем вверх, чтобы попадали в щель

Берем со столовой полки белый фиксатор проводов и фиксируем обе косы.

<figure><img src="https://lh4.googleusercontent.com/FuT-m0nlH35g6SCfPUm7xY2RFFZC3ldA46xM-e-XUw9JXcAC23s6Awb_R58HP-zkILOKMtkNUmUQtimA5PESFWl7EXmC9itE2wkowRix1zKRYyvcck-Z-OkKhTJdjgOq5Ak1nT98jart52AF_3ZkQco" alt="" width="188"><figcaption><p>Пример фиксации косы к корпусу принтера</p></figcaption></figure>

#### Устанавливаем парковки:

* ослабляем крепление полки передней панели
* парковочные места наживляем в боковинах (так, чтобы винты скользили в прорезях вверх-вниз, но люфт был минимальным) и хорошо прикручиваем к полке
* ставим обе ПГ на парковочные места и двигая вверх-вниз полку “в сборе” с парковочными местами, добиваемся того, чтобы каретка своими рогами заходила в обе ПГ как можно ровнее. Фиксируем переднюю полку.&#x20;
* далее, если каретка заходит в ПГ под углом, нажимаем на торчащий угол парковке, ловим оптимальное положение и фиксируем боковые винты парковки
* проводим в подвал шлейфы датчиков парковки, фиксируя их в детальках-фиксаторах проводов концевика, термистора и камеры.

#### Собираем держатель кос:

* алюминиевая трубка диаметром 6мм, длинной 450мм.
* 3 магнита 12 мм с фаской + М3х8 потай.
* гайку и винт М3x18 ISO 7380 для фиксации алюминиевой трубки.

<figure><img src="../../../.gitbook/assets/DSC_0616.JPG" alt="" width="375"><figcaption></figcaption></figure>

#### Режем/вставлям тефлоновые трубки:

* 750 мм - левая.
* 600 мм - правая.

Берем спиральную оплетку 6 мм длиной 350мм и заворачиваем вместе трубку и косу печатной головы.

<figure><img src="https://lh6.googleusercontent.com/E_1PNf3QJGRGLKlqyMaHsEXrql0W7PB3pQGJWBTQ0PKFVujv_1GQHf-vT1r7F8sqLYcUlDng_vGiIH1O0Kse7T_l1zDCj8ejsZYfyjFt0Y3eurRxGW13zp3GSrg7imq9xZ_jEjsq6GKn7tbJm-8gMZw" alt="" width="375"><figcaption><p>Пример завернутой косы и трубки в оплетку</p></figcaption></figure>

Заднюю стальную крышку крепим на винты М3х6 потай (шляпкой изнутри принтера) и колпачковые гайки снаружи.

Устанавливаем дополнительный держатель катушки.

Проводим все провода через тоннели в подвал, переходим к подключению.

## Подключение

[Подключение косы первой головы](https://www.figma.com/file/X9WwrNKUQqPAKn4cN9oWFJ/Toolchanger-tool0-connection?node-id=0%3A1\&t=2gI6XJn3zCmCmekO-1)

[Подключение косы второй головы](https://www.figma.com/file/GLTka7ZgJhVgqIfHdw7OtF/Toolchanger-tool1-connection?node-id=0%3A1\&t=6xhSHEfXzlOoGdZv-1)

[Подключение остального](https://www.figma.com/file/Zv0JVWCCv5MX4IfRR4hBOG/Toolchanger-other-connections?node-id=0%3A1\&t=LzTC5Ch2ivboOUdk-1)

[Запуск и настройка ](https://docs.google.com/document/d/1JqfKQ9mLFugpRIdRi6iEIp5E9hRSLpBilKQ2wFxqMMo/edit?usp=sharing)
